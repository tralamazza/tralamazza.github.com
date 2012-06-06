---
layout: post
title: "vim quicky: shift a line comment"
description: "How-to move a line comment to a specific column"
category: howto
tags: [vim]
---
{% include JB/setup %}

###Problem: How do I move a line comment ```//``` to a specific column ?

Let's say you want to shift a line comment to column *78*, here is what you do:

    qa0/\/\/<Enter>78i<Space><Esc>78|dwjq

Note: The commands between ```< >``` are actual key presses.

To execute just use ```@a``` like any macro (you can also do ```10@a``` to execute it 10x, or call ```@@``` repeatedly).

Here is the macro breakdown:

- ```qa``` Starts a macro named **a**

- ```0``` Move to the beginning of the line

- ```/\/\/<Enter>``` Search for **//**

- ```78i<Space><Esc>``` Insert **78** spaces

- ```78|``` Move to column **78**

- ```dw``` Delete all spaces until the next word

- ```j``` Jump to the next line

- ```q``` Stops recording this marcro

###FUQ (frequently useless questions)

Q: It doesn't work ! (and this is not even a question)

A: Yeah, this quick macro won't work for comments starting after line 78 =D
