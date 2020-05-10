---
layout: post
title: 008 of 100, structs, properties, and methods
---

it has been long time since last post but i have retruned to this cource

first of all i have to mention that last week i had to prepare some presentation and i had no time to learn swift. but now i do not have any excuses so new post is coming right now :D 

swift structs, seems to be very simmilar to c# structs. in both languages we are not able to inherit on them. in swift there is funny mechanism to track every change of property value in struct, it is possible to use 'didSet' and 'willSet' methods. simmilar to c# where we can use properties we are able to track if value has been changed:

{% highlight swift %}
// swift
struct Person {
    var name : String
    {
        didSet{
            print ("old name was: \(oldValue), and new name will be \(name)")
        }
        
        willSet{
            print ("current name id: \(name), new name will be \(newValue)")
        }
    }
}

var person = Person(name: "Simon")
person.name = "John"
{% endhighlight %}

'willSet' method will be triggered before assigning new value for name property (that is why we are able to access current name by refering 'name' and we have special variable 'newValue').

'didSet' method will be triggered after assigning new value for name propert (and in this method we have access to 'oldValue' variable).

next, we are able to define intializers, which are constructors in c# world. and yes, we are able to create multiple initializers and yes, the default on is also generated if we do not define any intilizer:

{% highlight swift %}
// swift
struct Person {
    var name: String

    init(name: String) {
        self.name = name
    }
    
    init() {
        self.name = "unknown player"
    }
}

var person = Person(name: "Simon")
print(person.name)  // we will print 'Simon'

var person2 = Person()
print(person2.name) // we will print 'unknown player'
{% endhighlight %}

i think that more usefull will be clases but maybe i am not aware of some swift-struct specific mechanism, so lets find out in future lessons. see you.
