---
layout: post
title: "obj-c additions + blocks"
category: coding
tags: [obj-c]
---
{% include JB/setup %}

### Uglyjective-C 

*Fact #1*: Most languages evolve. *Fact #2*: Few evolve in such an ugly way as Objective-C does.
It's a mess, but if you manage to ignore the terrible syntax and disgusting constructs what you
get is actually some great features with disgusting syntax and terrible constructs.

Want to extend a class ? Without subclassing ? And no source code access ? No problem, enter **Additions**!
An addition is a set of methods statically stitched to a target class. In some sense they are almost 
like a *trait*, just weaker. They lack the compositional power of traits and you can add only methods.
It's worth mentioning that some languages, like Ruby and C#, offer similar functionality with their
partial classes.

Anyway, here is how you extend a Obj-C class with some methods: <script src="https://gist.github.com/1870564.js"> </script>

Ok that sounds cool and all, but partial classes are so passé. What I really want is some of that clojure
goodness everyone is having. Better yet, I want those fancy functional collection methods, like 
```.map```, ```.filter```and ```.reduce```, all working on my bread & butter ```NSArray*```.
But for that we need a way to pass function pointers (you know, functional languages got this name
after... well functions).

**Blocks** are the answer and, like the name implies, they are just a bunch of code. A block can be tossed
around and assigned to function pointers. By the way I will totally ignore the scoping issues here, 
maybe in another post. Here is how you declare a block:

```( ReturnType (^) (paramType) )```

> Note that apart from that weird "^" it looks like a normal C function declaration.

#### NSArray Map/Filter/Reduce

Interface: <script src="https://gist.github.com/1869534.js"> </script>
Implementation: <script src="https://gist.github.com/1869552.js"> </script>

And even some usage: <script src="https://gist.github.com/1870771.js"> </script>