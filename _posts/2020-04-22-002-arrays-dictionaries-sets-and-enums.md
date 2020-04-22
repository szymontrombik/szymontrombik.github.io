---
layout: post
title: 002 of 100, arrays, dictionaries, sets, and enums
---

second day, not bad, keep it up

there are so many ways to create dictionaries in swift that it makes me dizzy. 

{% highlight swift %}
// swift
var dict1: Dictionary<String, Double> = [:]
var dict2 = Dictionary<String, Double>()
var dict3: [String:Double] = [:]
var dict4 = [String:Double]()
{% endhighlight %}

i think that i will stick to the 2nd option, it is simmilar to c# initialization of dictionary. 
tuples :D i was never a big fan of it in c# so in swift i still want to avoid them. using variable in which i have to remember property names is too dangerous. 

and enum with associated values, it is new approach for me but i am not sure if it is not the same idea as we have in c# - enum attributes (i need to investigate this part further or see real world usages)

{% highlight csharp %}
// c#
public enum SampleEnum
    {
        [Description("This is 1st value")]
        FirstValue = 1,
        [Description("This is 2nd value")]
        SecondValue = 2,
        [Description("This is 3rd value")]
        ThirdValue = 3,
    }
{% endhighlight %}
