---
layout: post
title:  "Introduction to Variables"
date:   2026-09-11 04:00:00 -0400
author: Vincent Tong
team: programming
---

>[!TIP]
>It may be helpful to follow along this article with a code editor that can compile and run Java programs. 
>
>The best way to learn code is by analyzing example code, modifying the code and seeing what changes, and also completing exercises.
>
>We recommend [OneCompiler - Java](https://onecompiler.com/java) for running simple online Java programs.

<hr>

## Table of Contents


1. Introduction to Variables
2. Primitive Types
3. Reference Types
4. Variable Formatting
5. Using Variables
6. [CATCH] - 'int' inside of 'double' variable
7. Modifying Variables


<hr>

## 1. Introduction to Variables


***Variables*** are another staple of programming across all common modern languages, and in fact without variables it'd be extremely difficult to have complex meaningful programs.


*Well*, why is that? You've likely heard the term ***variable*** before in courses such as math, where for example the variable '**X**' typically represents a number on the *X-axis* while the variable '**Y**' typically represents a number on the *Y-axis*. A variable operates in a similar premise in programming where it can hold a **value** such as a number, but it can also hold a lot more! We can use variables for our **programs to store, retrieve, and modify data to our needs**, sort of like short-term memory.

Another analogy would be that a variable is like a *box* with a *label*. The box can hold what you choose to put in it, and the label is a way to say that "this is what has to go in the box, and this is the name of the box." Whenever you need to retrieve an object from the box you would know the specific box you're looking for as well as an idea of its contents.

You will be using variables a lot during your time programming, so it's helpful to be comfortable with them. Let's get started!

<hr>

## 2. Primitive Types


We're going to begin with understanding what exactly is a ***variable type***. A variable type defines what type of data the variable must hold, and every variable in Java *should* explicitly have a type. This means that when you create a variable you would have to tell Java what type of data that variable must hold. There are two types of variable types, a ***primitive type*** and a ***reference type***.

>[!NOTE]
>The introduction of the keyword `var` in Java 10+ allows for implicit types. I personally don't use implicit types because of type-safety benefits and semantics.

Java has eight (8) total primitive types:

1. `byte` - A number between -128 to 127 (1 byte)
2. `short` - A number between -32,768 to 32,767 (2 bytes)
3. `long` - A number between ~ -9.22 quintillion to ~ 9.22 quintillion (8 bytes)
4. `float` - A number with 6-7 decimal digits of precision (4 bytes)
5. `char` - A character (2 bytes)
6. `int` - An integer number between ~ -2.14 billion to ~ 2.14 billion (4 bytes)
    1. i.e. `3`, `-8`, `0`, `392`, `18`, `-182`
7. `double` - A number with 15-17 decimal digits of precision (8 bytes)
    1. i.e. `3.1415`, `2.718`, `2.0`, `-56.19`
8. `boolean` - Represents only `true` or `false` (binary)

*Nooo! But that's so many variable types!* Luckily for you, you really only need to know about the last three primitives: `int`, `double`, and `boolean`. In my experience when coding the robot I've used those three primitives 99.99% of the time, but you may find niche use cases for the other primitives. 

Why are they called *primitives*? I'm sure you've watched YouTube videos of people building those crazy mud-hut mansions out of 'primitive tools' like sticks and rocks (... ignoring the fact that these videos were staged), and you could probably guess that *primitive* means **the most basic**. You can't get more basic than a number or a value of `true` or `false`. Variables that utilize primitive types are the most **performant yet limited** types of variables.

<hr>

## 3. Reference Types

We'll explore more about reference types in later articles when we start to work with *classes* and *object-oriented programming*, but ***reference-types*** are types of data that fall under a *class* and are often custom *objects* that contain *properties* and *methods*. Understanding how to utilize reference types can make your program much more concise and powerful.

>[!NOTE]
>It is called a **reference type** because when you create a variable of this type, the variable doesn't actually contain the physical data itself in memory, but rather the variable is a 'reference' that points to where the data is located in memory for the program to access. This technical property isn't necessary to understand for you to code **EXCEPT** for one scenario which we'll explore later.

For now, the most familiar reference type to you would likely be the `String` type. If you recall what a `String` does, it represents text data.

{% highlight java %}
String myText = "Hello world!";
// This line creates a variable called 'myText'
// and it has the text data of "Hello world!"
{% endhighlight %}

There is virtually an unlimited number of reference types you could have because reference types are made through custom *classes* and *interfaces* that your program uses. If you're using a *code library* with a wide array of classes, then you are bound to see some variables with reference types based on the custom classes.

<hr>

## 4. Variable Formatting

When you want to create and use a variable in your program, there is quite a simple format:

`[type] yourVariableName = [value];`

You simply declare the variable by defining its type, naming the variable, and then assigning it a value of the same type.

>[!CAUTION]
>Make sure your variable names are unique. You can't have multiple variables with the same name in the same scope.
>
>The `=` symbol in Java does **not** mean equality, but rather assignment. The symbol tells the variable to take on the value of what is to the right.

>[!TIP]
>Notice the variable name's capitalization where the first letter is lowercase but the other words are capitalized.
>
>This practice is called **camelCase**, and while you could name your variables how you'd like to (given that it uses valid characters), using *camelCase* is a standard convention practice that most programmers use to make variables more readable for others and themselves.
>
>Also, a good practice is to **name your variables based on what they're used for**.

<hr>

## 5. Using Variables

Let's start with some familiar code if you've read about the **Main** class and **main** method in the last article:


{% highlight java %}
public class Main {
    public static void main() {

        int myInt = 7;
        // We made a variable called 'myInt' and assigned it the value of 7
        System.out.println(myInt);
        // We can print this variable out to the console!
        // What do you think it might print to the console?

    }
}
{% endhighlight %}
Output:
{% highlight plaintext %}
7
{% endhighlight %}

What do you notice? We have two lines of code here within the `main` method that you should be familiar with. `int myInt = 7` essentially tells the program to create a new variable of the type `int` and to assign it the value of `7`. This works out because `int` represents integer numbers (whole numbers) and `7` is in fact a whole number. Then the second line of code prints out the value of `myInt`. You can use variables in your programs simply by typing out the variable's name after you declare the variable.

However, if you tried to place a different type of value such as a `double` which is a decimal number inside of `myInt` and create a conflict of types, you'll be met with an error.

{% highlight java %}
public class Main {
    public static void main() {

        int myInt = 9.4;
        // We made a variable called 'myInt' with the type 'int'
        // but we assigned 'myInt' with a 'double' of '9.4'
        // What do you expect?
        System.out.println(myInt);

    }
}
{% endhighlight %}
Output:
{% highlight plaintext %}
Error (incompatible types)
{% endhighlight %}

The program errors because Java is a **strictly-typed** language that forces variables to **explicitly have a type but also a value that matches that type**.

>[!TIP]
>If you explore different languages, a lot of common languages like Python do not force strict-typing like you see here in Java, but rather give you an opportunity to strictly type your variables. You may think that strict-typing is restrictive and an annoyance, but I actually ended up preferring strict-typing even beyond Java because **it can prevent you from making minor mistakes about your variables and provides you with more control over your program**.

>[!WARNING]
>Intuitively, you might expect `7.0` to also be usable as an integer value because it is a whole number, but Java actually considers that number as the type `double` because of the decimal point. 

<hr>

## [`CATCH`] >> `int` inside of `double` variable

>[!IMPORTANT]
>For future articles, you might see a brief section like this one that says 'CATCH'. These are quick interruptions in articles that I will use to further discuss topics that I believe are important to highlight for you to *catch* on. Sometimes they can be tricky, so if you're still unsure you should discuss in the Discord or do further research!

**"I got it, never use values of different types in a variable."** - *you, probably*

I wish it were that easy, but just like many things in life there always has to be a caveat. 

There are a few scenarios where you actually **CAN** use a value of a different type inside of a variable. We'll explore this more when we discuss *auto-boxing*, *un-boxing*, and *interfaces*. Do note that these few scenarios are kind of niche, but nonetheless I've ran into them while coding the robot occasionally.

Consider the following code:

{% highlight java %}
public class Main {
    public static void main() {

        double myDouble = 9;
        // We made a variable called 'myDouble' with the type 'double'
        // but we assigned 'myDouble' with an 'int' of '9'
        // What do you expect?
        System.out.println(myInt);

    }
}
{% endhighlight %}
Output:
{% highlight plaintext %}
9.0
{% endhighlight %}

Notice how Java prints out `9.0` instead of `9`.

When you first approach that code, you'd likely believe it would error, right? After all, you shouldn't be able to put an `int` inside of a `double` variable, they don't match! 

*Well, sort of . . .* Consider the idea that it'd be an untrue statement to say that a number with decimals (i.e. `9.4`) is a whole number, but wouldn't it be a true statement to say that a whole number (i.e. `9`) could be also a decimal number? After all, `9` could just be represented as `9.0` and still be both a whole and a decimal number. Java handles these conversions by itself because it'd always be the case that if you pass in an `int` value to a `double` variable that the variable has a way to convert the `int` value to be a `double`, but not vice-versa.

You *shouldn't* assume that something that can be converted to another type will always work, but here's an example of one that *does* work. You'll likely find other examples that do work.

<hr>

## 7. Modifying Variables

It'd be quite limiting if you could only assign a variable one value at the start and never be able to change it. In Java and many programming languages, **you can modify the variable later in the code after declaring it!**

You can simply assign your variable with another value by writing: 

{% highlight java %}
// Assume that you've already made a variable called 'myVariable' 
// and it has the type 'int'
myVariable = 3
// Now the variable 'myVariable' has a value of '3'!
myVariable = 4
// Now the variable 'myVariable' has a value of '4'!
{% endhighlight %}

It's similar to creating a variable, but because you're modifying an existing variable you don't have to tell Java what that variable's type was again, so you can just write the variable to be equal to a value of the same type. Remember, you can't put a value of a different type into a variable (with a few exceptions).

<hr>

### Exercise 1

{% highlight java %}
public class Main {
    public static void main() {

        int a = 1;
        String b = "FIRST";
        boolean c = true;

        System.out.println(a);
        System.out.println(b);
        System.out.println(c);

    }
}
{% endhighlight %}

Take a look at the code above. What do you think will be output to the console if you print `a`, `b`, and `c`?

<hr>

### Exercise 2

{% highlight java %}
public class Main {
    public static void main() {

        int a = 3;
        a = 6;
        System.out.println(a);

    }
}
{% endhighlight %}

What do you think will be printed by the code?

<hr>

This was quite the long article, but hopefully it was helpful in learning what variables are and how to use them in your program. There's more to learn about variables!

Have any questions or want to discuss exercise answers? Be sure to ask for help on the Discord!

***Thanks for reading, see you in the next article!***