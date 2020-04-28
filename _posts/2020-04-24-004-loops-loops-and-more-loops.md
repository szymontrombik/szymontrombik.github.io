---
layout: post
title: 004 of 100, loops, loops, and more loops
---

inner lazybones defeated!

i wanted to skip today but i gathered my power and here i am after 4th lesson.
loops in this course were pretty raugh. especially the quiz after this part of course.
still, there are a lot of simmilarities with c# but some of the things are new. in for loops you can easily use syntax of range:

{% highlight swift %}
// swift
for i in 1...10 {
  print("value of i is \(i)")
}

//or if you do not need to use counter 'i'
for _ in 1...10 {
  print("new iteration of loop")
}
{% endhighlight %}

also, there is neat idea to break outer loops, just name the loop which you want to break and then use 'break {name}'. that is it ;)

{% highlight swift %}
// swift
outerLoop: for i in 1...10 {
    for j in 1...10 {
        print("i: \(i), j: \(j)")
        if i == 2 && j == 2 {
          print("sorry, we need to break here")
          break outerLoop
        }
    }
}
{% endhighlight %}

in this code we iterate through those loops until 'i' and 'j' are not bot equal to 2.

that is all for today, see you tommorow.
