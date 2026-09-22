---
layout: post
title:  "Java Fundamentals"
date:   2026-09-09 09:18:43 -0400
author: Vincent Tong
team: programming
---

## Table of Contents
1. Variables
    1. Primitives
    2. Reference Objects
    3. Data Collection
    4. Autoboxing & Unboxing
2. Control Structures
    1. Sequential
    2. Selection
    3. Repetition
3. Object-Oriented Programming
    1. Classes
    2. Objects
    3. Methods
    4. Properties

4. Event-Based Programming

5. Encapsulation & Scope

6. Operators

7. Exception Handling
<hr>

## Abstract
In this article, you will learn about the fundamentals of Java and brief explanations about how each topic works in Java. The topics will be more thoroughly explained in future articles, but this article should be an easy introduction towards what you should expect when programming in the Java language using WPILib. 

>[!NOTE]
>This isn't an exhaustive list as Java has a wide variety of features, but these are Java fundamentals that are required to understand for coding FRC robots and have been consistently used throughout my FIRST programming journey. 

>[!TIP]
>It's quite interesting, but once you master Java (or any modern high-level scripting language for that matter), the fundamentals that you learn can typically be applied to other languages too! Programming as a whole becomes so much easier after you master one language. I came from a game design background (Luau, JS) to working on robots (Java, C++)! 
<hr>

## 1. Variables
Variables in Java are just like variables in math. They're used to store data which you can reference to use or modify, and without variables it'd be impossible to reference any data to use; code would be extremely basic! There are a few types of variables that you will need to know about.

### Primitive Variables
In Java, primitives are the **most basic** form of data that the code can store, here's a list of the most common ones that we use! (There are 8 primitives in total, but I only cover 3):

- `int`: **int** represents an integer variable. These are ***numbers without decimal places***. (i.e. 3, 7,  -2)
- `double`: **double** represents ***decimal numbers***. (i.e. 3.14, 6.022, -1337.0)
- `boolean`: **boolean** represents a value of either ***true*** or ***false***. This is arguably the simplest variable type possible. 

### Reference Objects
Variables can also *reference* an object. While this may seem abstract if you're new to *object-oriented programming*, all this means is that a variable allows you to **point to a custom object stored in memory** and use it! We'll explore this more, but it definitely expands our world from being limited to basic values.

### Data Collection
Data Collection refers to **storing values / objects in a list** and being able to retrieve that information from the list. Data collection allows us to keep similar values grouped together in a more organized manner.

### Autoboxing & Unboxing
*This won't make sense for now, which is completely fine!* Autoboxing allows you to convert **primitive values into reference objects**, whereas Unboxing does the opposite: **reference objects into primitive values**. This only applies to the *8 primitive objects and their associated wrapper classes*, so chances are you may rarely use this, but it's still important to understand. 
<hr>

## 2. Control Structures
Control structures allow you to **control how code is ran**, and is the backbone of coding.

### Sequential
Sequential control structures simply means that the code runs from **step by step**, and that **each line of code must finish running before the next line of code is ran.**

### Selection
Selection control structures are where you can make decisions when code runs and **control what code is ran or avoided**. These are typically defined by **if-statements**, where you're saying that ***if something is this case, then we should run a specific code block, otherwise we should ignore that code block.***

### Repetition
Repetition control structures are where you can make **code run a set amount of times or until a condition is true**.
<hr>

## 3. Object-Oriented Programming
Object-Oriented Programming (or **OOP**) is the heart of Java, and essentially allows you to create custom *objects* and *classes* that can have **properties** and **methods** associated with them. ***OOP can be extremely confusing at first, but we'll get to see it work in real code later!***
>[!TIP]
>Imagine a car for example, a car may have **properties** associated with it such as its color, height, and width. A car can also have **methods** which describe how you can interact with the car such as accelerate, open doors, and brake.

### Classes
Classes are like **blueprints**. Classes can be created by you to create a **logical group of methods and properties** of that blueprint. Defining a car for example is very consistent across the board; a car logically has the ability to drive, brake, and steer (its methods), and also has certain properties like its color, number of seats and size. Classes are especially helpful because you can **make multiple related objects from a class** and **provide a logical grouping of data and methods**.

### Objects
Objects are **made from classes**. While classes may define what a car is for example, an object would be like an actual car such as a Honda Civic or Nissan Altima that came from the "car class". 

### Methods
Methods define how you can **interact with the class or object**.

### Properties
Properties are values that **describe what the class or object contains; they hold data about the class or object.**
<hr>

## 4. Event-Based Programming
Event-Based Programming (or **EBP**) is simply **running code when an event has occurred**. When you click on a link with your mouse, the mouse sends an event to the computer that describes "this user clicked on this link", and the computer reacts by opening up that link. 
<hr>

## 5. Encapsulation & Scope
Encapsulation is a practice that **prevents you from accessing or modifying data in ways that aren't defined**. For example, you can give the money that you have to a bank, or take money that you have deposited from a bank, but you can't look at other people's bank accounts or withdraw more money than you can by going through a bank teller. Encapsulation can be very beneficial by preventing subtle programming mistakes or bad practices and strictly ensures that you write code based on how you defined it to work. 

Scope means that **variables within a code block stays within that code block**. It's like a ***secret***; if you only tell a secret to a small group of friends, only that friend group would know about that secret and everyone else wouldn't know. Scope allows for better memory management and is a fundamental encapsulation principle.
<hr>

## 6. Operators
Operators are symbols that describe how you interact with variables. 
`Comparators`: These **compare two variables together**, and return a **boolean** (a ***true*** or ***false***). They're important for selection control structures.

`Assignors`: Assignors can either **set or increment a variable to a specified value.**

`Math Operators`: Math operators simply **do math**; you've likely seen '+' representing addition, '-' representing subtraction, etc. These allow you to perform math calculations in code.
<hr>

## 7. Exception Handling
When you run your code, ***it might not always work!*** There are plenty of errors that can occur with code, and I still make them all the time even though I've been coding for over 8 years. When the code doesn't run properly, it may throw an **error** and likely prevent future code in the program after that point from running to prevent catastrophic errors or if the computer doesn't know how to continue. 

Error handling means that you **define a way for the computer to work around an issue** *when an error does appear*. Imagine that you asked the program to compare whether the number `5` is greater than a variable that is `null` (doesn't contain any information). The program doesn't know how to proceed from here, and throws an error, but you could add an error handler that says **if the variable does not exist or contain a value, then we should skip this comparison and prevent the entire program from stopping on one error**.

<hr>

**That was a ton of information!**... but you will get extensive practice and a deeper understanding of all of these concepts in the near future! This was intended to give you a brief insight on what to expect when coding in Java for the robot. It's actually not all that much once you get in the rhythm, and it becomes second nature to you! Future articles will dive more in-depth into what these concepts really mean and look like in code, and how you can apply it in robot code.

***Thanks for reading, see you in the next article!***