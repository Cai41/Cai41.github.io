---
layout: post
title:  "Chapter 19: Software Trends"
date:   2020-11-12
categories: A philosophy of software design
---
<h1>Object-oriented programming</h1>

1. Interface Inheritance
2. Implementation Inheritance
This creates dependencies between parent and child. Sometimes developer still needs to look at both parent and child classes to avoid break dependencies.
Consider use composition when you want to use this inheritance.
If there is no alternatives, at least try separate the state managed by parent and subclass. One way to do this is for certain instance variables to be managed entriely by
methods in the parent class wth subclass using them only in a read-only fashion. This applies the notion of informatio hiding within the class hierarchy to reduce dependencies.

<h1>Agile development</h1>
Developing incrementally is generally a good idea, but the increments of development should be abstractions, not features. Once you need the abstraction, invest the time to design it cleanly. One of the risk of agile development is that it can lead to tactical programming, encpuraging developers to put off design decisions in order to produce working software as soon as possible.

<h1>Unit tests</h1>
With a good set of tests, developers can be more confident when refactoring because the test suite will find most bugs that are introduced. This encourages developers to make structural improvements to a system, which results in a better design.

<h1>Test-driven development</h1>
The problem with test-driven development is that it focuses attention on getting specific features working, rather than finding the best design.
One place where it makes sense to write the tests first is when fixing bugs. Before fixing a bug, writing a unit test that fails because of the bug. The fix the bug and make sure that unit test now passes. If you fix the bug before writing the test, it's possible that the new uni test does not  actually trigger the bug, in which case it won't tell you whether you really fixed the problem.

<h1>Design patterns</h1>
Rather than designing a new mechanism from scratch, just apply a well-known design pattern. Don't be over-application, don't try to force a problem into a design pattern when acustom approach will be cleaner. The notion that design patterns are good does not neccessarily mean that more design pattterns are better.

<h1>Getters and setters</h1>
It's better not to expose instance variables in the first place. It means the part of the class's implementation is visible externally, which violates the idea of information hiding and increases the complexity of the class's interface. Getters and setters are shallow methods, so they add clutter to the class's interface without providing much functionality. It's better to avoid getters and setters as much as possible.

