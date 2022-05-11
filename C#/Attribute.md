## 声明特性
``` C#
using System;
public class XxxxAttribute : Attribute
{
    public string Name { get; set; }
}
```
## 使用特性
``` C#
using System;
// 方式 1
[Xxxx(Name="描述")]
public class ClassA
{

}
// 方式 2
[XxxxAttribute(Name="描述")]
public class ClassB
{

}
```
## 声明特性(有构造函数)
``` C#
using System;
public class XxxxAttribute : Attribute
{
    protected string content;
    public XxxxAttribute(string param)
    {
        content = param;
    }
    public string Name { get; set; }
}
```

## 使用特性(有构造函数)
``` C#
using System;
[Xxxx("描述", Name="描述")]
public class ClassA
{

}
```