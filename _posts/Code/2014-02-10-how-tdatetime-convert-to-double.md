---

layout: post
title: How TDatetime convert to double
date: 2014-02-10 16:58
tags: [code,delphi]
categories: [code]

---

在Delphi中 `TDatetime` 是 `Double` 类型的

{% highlight delphi %}
OutputDebugString(PChar(FloatToStr(Now)));
{% endhighlight %}
 
会输出 `41680.8075846759` 这样的数字


### Principle

整数部分是代表距[Base Date][^4]的天数，在Object Pascal中，`Base Date` 为December 30, 1899，所以如果你运行下面的代码可以得到为零的浮点数


{% highlight delphi %}
var
Date : TDateTime;
FormatSettings : TFormatSettings;

begin
FormatSettings.DateSeparator := '-';
FormatSettings.TimeSeparator := ':';
FormatSettings.ShortDateFormat := 'yyyy-mm-dd';
FormatSettings.LongTimeFormat := 'hh:nn:ss';
Date := StrToDateTime('1899-12-30 00:00:00', FormatSettings);
OutputDebugString(PChar(FloatToStr(Date)));
end
{% endhighlight %}

而小数部分代表这一天的几分之几，例如 `1899-12-30 12:00:00` 得到的浮点数就为0.5


### Base date
这个 `Base date` 在不同的软件，不同的系统中都是不一样的，具体可以参考[Wiki][^4]

### Reference

[TDateTime Class][^1]

[Dates And Times In Excel][^2]

[What is story behind December 30, 1899 as base date?][^3]

[Epoch (reference date)][^4]


[^1]: http://docs.embarcadero.com/products/rad_studio/delphiAndcpp2009/HelpUpdate2/EN/html/delphivclwin32/System__TDateTime.html
[^2]: http://www.cpearson.com/excel/datetime.htm
[^3]: http://social.msdn.microsoft.com/Forums/en-US/f1eef5fe-ef5e-4ab6-9d92-0998d3fa6e14/what-is-story-behind-december-30-1899-as-base-date
[^4]: http://en.wikipedia.org/wiki/Epoch_(reference_date)#Computing
