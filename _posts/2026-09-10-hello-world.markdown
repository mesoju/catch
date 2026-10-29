---
layout: post
title:  "Hello World"
date:   2026-09-10 04:00:00 -0400
author: Vincent Tong
team: programming
---

>[!TIP]
>It may be helpful to follow along this article with a code editor that can compile and run Java programs. 
>
>We recommend [OneCompiler - Java](https://onecompiler.com/java) for running simple online Java programs.

<hr>

## Table of Contents

1. "Hello World!"

2. How Java Works

<hr>

## 1. "Hello World!"
You've likely seen this code many times before:

{% highlight java %}
public class Main {
    public static void main() {
        System.out.println("Hello world!");
    }
}

// Output: Hello world!
{% endhighlight %}

A lot of beginner programming tutorials start off with this block of code due to its simplicity. There are three main things to dissect from this block of code;

1. The Class `Main`
2. The Method `main()`
3. The Code `System.out.println("Hello world!");`

<hr>

## 2. How Java Works

Right now, you don't need to worry about some of the unfamiliar keywords in order to get started, and we'll cover these in future articles.

Every line of code that is ran in Java **must be contained inside of a class**. Notice how all of the code that is ran is contained within the brackets of `public class Main {}`. Typically, no code should be located outside of a class.

`public class Main` defines a class with the name **Main**. Keep in mind that when you create a class, **the class's name must match the file's name**: if you had a file named **MyClass.java**, then you would create a class by writing `public class MyClass {}` (it is **case-sensitive**). After creating the class you would add a pair of curly brackets `{}`. In Java, curly brackets defines **a block of code that is ran together under either a class, method, or conditional**. 

>[!NOTE]
>A ***class*** represents a **logical type of object** that can contain its own properties and methods. While this may seem abstract now, classes become very useful in Java later and may become an incredibly powerful tool for you.

{% highlight java %}
public class Main {
    // Okay, now you created the Main class, but now how do you add code?
}
{% endhighlight %}

Well, every program (*not* every class) in Java also requires a **main** method that acts as a starting point to show where code has to start from. Code in the **main** method will be ran as soon as the program is executed. You can create a **main** method by writing `public static void main()`. *Woah*, that's a lot of words, what does `public`, `static`, and `void` mean? Well, for now we don't really need to understand them for our purposes, but they do serve very essential roles later. All you need to know is that those keywords mean that the method is public and can be accessed by other Java classes, the method is static so it is directly associated with the class itself, and the method doesn't return anything. Don't forget the curly brackets to complete your method!

{% highlight java %}
public class Main {
    public static void main() {
        // Cool, we have a class with a method inside of it...
        // but the program doesn't do anything right now.
        // Let's make it do something simple!
    }
}
{% endhighlight %}

Most people start off with the code `System.out.println()`. This code essentially allows you to put data onto a console / output. We can put the ***string*** `"Hello world!"` inside of the parentheses to tell the code what to print.
>[!NOTE]
>A ***string*** is used to represent text, so you can write words, entire sentences and paragraphs. Strings can be formed by putting your text in between quotation marks: "like this!"

{% highlight java %}
public class Main {
    public static void main() {
        System.out.println("Hello world!")
        // Try running this in your code editor to confirm that the program outputs "Hello world!"
    }
}

// Output: Hello world!
{% endhighlight %}

Congrats! You've made your first successful Java program... but let's apply this knowledge!

<hr>

### Exercise

{% highlight java %}
public class Main {
    public static void main() {
        // Write your code below!

    }
}
{% endhighlight %}

Copy and paste the code above into your code editor. How do you write a line of code that prints to the console? Try printing a variety of different of outputs!

Try printing this:
`7538 Metal Mountain`

<hr>

Have any questions or want to discuss exercise answers? Be sure to ask for help on the Discord!

***Thanks for reading, see you in the next article!***