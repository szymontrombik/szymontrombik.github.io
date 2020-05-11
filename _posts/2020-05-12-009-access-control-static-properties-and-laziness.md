---
layout: post
title: 009 of 100, access control, static properties, and laziness
---

new day, new post

so, today i have investigated access modifiers and some other things which are usefull when we are speaking about structs.
and for access control in swift, there are 4 modifiers to use:
* public access - the same as we have in c#,
* internal access - also the same as we have in c#, we are able to access this resource across all module elements,
* file private - simmilar to private protected in c#, we we are able to access this resource within declared assembly,
* private - access only inside the struct, cannot be referenced outside of the struct,

next things are initializers, or how do we say in c# - constructors. interesting thing in swift is that by default the memberswise initializer is created and it demand to define all properties inside the struct. you are still able to create custom initializers but you have to be sure that when initializer finish all of the properties are initialized...

or

if you do not need to init all of the properties it is recommended to use 'lazy' operator which postpone the initialization of the property until it has been referenced.

and it was another chapter when i have c# deja vu ;) but i am happy with that, because it should be easier to dive into new language. bye.
