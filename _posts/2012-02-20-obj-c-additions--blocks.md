---
layout: post
title: "obj-c additions + blocks"
category: coding
tags: [obj-c]
---
{% include JB/setup %}

### Uglyjective-C 

*Fact #1*: Most languages evolve. *Fact #2*: Few evolve in such an ugly way as Objective-C does.
It's a mess, but if you manage to ignore the terrible syntax and ugly constructs what you
get is actually some great features with terrible syntax and ugly constructs.

Want to extend a class ? Without subclassing ? And no source code access ? No problem, enter **Additions**:
An addition is a set of methods statically stitched to a target class. They are almost like a *trait*,
just weaker. Just methods, not attributes.

That sounds cool and all, but partial classes are so passé. What I really want is some of that clojure
goodness everyone is having. Better yet, I want those fancy functional collection methods, like 
```.map```, ```.filter```and ```.reduce```, and of course I want them to work on my bread & butter ```NSArray*```.

**Blocks** are (like the name implies) a block of code, that can be assigned to a function pointer.
Now the thing to know about blocks is that they have tricky scope rules.




#### Source code

Interface: <script src="https://gist.github.com/1869534.js"> </script>
Implementation: <script src="https://gist.github.com/1869552.js"> </script>