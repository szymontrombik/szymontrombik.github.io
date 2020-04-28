---
layout: post
title: 005 of 100, functions, parameters, and errors
---

another day, another lesson

a lot of new things in this chapter of tutorial. first of all 'variadic functions'. i do not understand this syntax, much easier will be to use arrays since the method works the same way (and it turned out that compiler will translate those variadic parameters into arrays under the hood, so this is just syntax-sugar which i will not be using):

{% highlight swift %}
// swift
func squareVariadic(numbers: Int...) {
    for number in numbers {
        print(number * number)
    }
}

func squareWithArray(numbers: [Int]) {
    for number in numbers {
        print(number * number)
    }
}

squareVariadic(numbers: 1, 2, 3, 4, 5)
squareWithArray(numbers: [1, 2, 3, 4, 5])
}
{% endhighlight %}

also there is idea to mark with underscore parameter if you want to omit it name when you call the function. and this is directly connected with two names for parameter, which is also crazy/new for me :D 

{% highlight swift %}
// swift
func sayHelloTo(_ name: String) {
  print("hello \(name)")
}

func sayHello(to name: String) {
  print("hello \(name)")
}

sayHelloTo("John")
sayHello(to: "John")
{% endhighlight %}
