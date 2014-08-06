编写可读代码的艺术
=================
*The Art of Readable Code*

#### 译者序
> 在《Clean Code》一书中Bob大叔认为在代码阅读过程中人们说的脏话频率是衡量代码质量的唯一标准。

#### P2 前言
> **代码应该写得容易理解**

<!-- -->
> 我们希望大部分读者在一两周内读完全书.

<!-- -->
全书加上附录才178页

#### Chapter 1
> 代码的写法应当使别人理解它所需的时间最小化

<!-- -->
这里的其他人很有可能是6个月后的自己，其实有时候都用不到6个月，一周没有去摸代码的话说不定也会生疏

#### Chapter 2
> **把信息装入名字中**

<!-- -->
> 选择专业的词

<!-- -->
作者认为`Get`这个词非常不专业，但是在我平常的使用中经常使用到，书中举的例子是`GetPage()`，但就这个函数名来说，是没有表达出更多的信息，但是`DownloadPage()`，也没有表达出完整的意思，觉得用`GetDownloadPage()`更好，如果嫌名字太长，可以进一步简化为`GetDwnldPage()`，总的来说，以后命名函数名称还是要避免使用意义泛泛的词。


*这是书中的一个表格，作为参考*


Word | More Choose 
--- | --- 
send | deliver , dispatch , announce , distribute , route
find | serach , extract , locate , recover 
start | launch , create , begin , open
make | create , set up , build , generate , compose , add , new



##### 循环迭代器
例子更能表达出这个意思：
```
for (int i = 0; i < club.size(); , i++)
  for (int j = 0; j < club[i].members.size(); j++)
    for (int k = 0; k < user.size(); k++)
      if (club[i].members[k] == user[j])
        // bla , bla , bla
```

```
if (club[ci].members[mi] == user[ui])
```

#### Chapter 3

> **一致的风格比"正确"的风格更重要**

<!-- -->
这句话应该是针对团队开发而言的。