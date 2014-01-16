---

layout: post
date: 2014-01-15 10:53
title: Delphi控制台程序添加图标
tags: [delphi, code]

---



> all console mode applications have the same icon (depends on the Windows version).

- write `1 icon "xxx.ico"` in a file and save this file as `xxx.rc`
- add `xxx.rc` to your console mode project
- Compile


#### Reference

[Change the Default Application Icon for a Console Mode Delphi Application][^1]

[Changing console application window icon at runtime!][^2]

[Change icon for a Delphi console application][^3]


[^1]: http://delphi.about.com/od/delphitips2009/qt/console-mode-delphi-application-specify-icon.htm
[^2]: http://ntcoder.com/bab/2007/07/24/changing-console-application-window-icon-at-runtime/
[^3]: http://stackoverflow.com/questions/1627526/change-icon-for-a-delphi-console-application