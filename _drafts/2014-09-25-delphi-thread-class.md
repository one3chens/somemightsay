---

layout: post
title: Delphi thread class
date: 14-09-25 15:39:23
tags: [delphi, thread, code]
categories: [code]

---

### Finished & Terminate

**Finished** 

> `Finished` is `True` when the thread execution is completed or terminated, and `False` otherwise. This property is read-only.

**Terminate** 

> `Terminate` sets the thread's Terminated property to true, signaling that the thread should be terminated as soon as possible.

> For Terminate to work, the thread's Execute method and any methods that Execute calls should check Terminated periodically and exit when it's true.

> Unlike the Windows API TerminateThread MSDN, which forces the thread to terminate immediately, the Terminate method merely requests that the thread terminate. This allows the thread to perform any cleanup before it shuts down.

`Finnished` 属性是当线程执行完成或者被终止过后会被设置为 `True` ， 这里面的完成和终止，可以理解为 `Execute` 函数执行完成后，会把 `Finnished` 属性设为 `True` 在源代码中也确认了这点


```pascal
try
if not Thread.Terminated then
try
  Thread.Execute;
except
  Thread.FFatalException := AcquireExceptionObject;
end;
finally
FreeThread := Thread.FFreeOnTerminate;
Result := Thread.FReturnValue;
Thread.DoTerminate;
Thread.FFinished := True;
```

另外函数 `Terminate` 也只是把内部变量 `FTerminated` 设为 `True` ，需要在执行代码中不断的去检测 `Terminated` 的值，然后进行处理。所以这里的 `Terminate` 并不是马上终止当前的线程；要立马终止线程则可以用 `TerminateThread` 函数强制结束线程，但是可能会造成内存泄漏或者其他的问题。