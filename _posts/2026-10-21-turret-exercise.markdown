---
layout: post
title:  "Turret Angle Exercise"
date:   2026-10-21 10:50:00 -0400
author: Vincent Tong
team: programming
---

## Context
For FRC's 2026 season, REBUILT, teams competed by building robots that could launch fuel into a hub. Many design approaches could achieve the same goal, but 7538 Metal Mountain decided to use a **singular omni-directional turret** approach. There are some benefits and negatives of this design. The largest benefit is that the robot could shoot fuel into the hub regardless of where the robot is facing and also shoot on the move at low speeds because the turret homes automatically towards the hub. The largest negative is the complexity of the design and tuning the turret to efficiently and accurately handle targetting and shooting. The full code for this season's robot went well into the region of a few hundreds of lines of code. You won't be asked to handle this full problem, but **you should be able to solve for what angle the turret should turn to (in degrees or radians) in order for the turret to aim towards the hub.**

This exercise will target:
- Understanding of Vectors
- Using, modifying, and creating Java Classes
- Trigonometric functions and geometric functions to find turret angle
    - **arctan** / **atan^-2** are relevant here; you can find their use in the Desmos below. You should search this up for familiarity with how these math functions work as well as their implementation in Java.

<hr>

## Concepts
### Vectors
You've likely heard or seen of vectors before even if you didn't realize it. Vectors are formally defined and extensively used in more advanced courses, such as AP Physics 1 and C:Mechanics, AP Precalculus and Calculus AB/BC, and Linear Algebra. In Robotics, we represent positions as vectors, and that's really all it is. Imagine the point (2,3) on an XY-coordinate plane, that would be the vector expressed as `Vector2(2,3)`. 

- Why do we use vectors to express positions?

2D Vectors hold an X-coordinate and a Y-coordinate much like a coordinate pair, except because vectors are defined as a **quantity with a magnitude (i.e. distance) and a direction** which can allow us to *interpret and use vectors in more meaningful ways*. For the purposes of robotics and this exercise, **2D vectors and coordinate pairs are functionally the same.**

- How do I incorporate vectors into my code?

Don't worry; I've created a custom Vector2 class which you can directly implement to your code and use. When coding in a real WPILib IDE, the library typically provides you with a more robust and versatile Vector class with more features and use cases. In this demo, the provided Vector2 class should be sufficient.

<hr>

## Exercise
### Scenario
- The field is 15 units in length and 5 units in width (x = 15, y = 5, see Desmos for clarification).
- The hub is located at (7.5, 2.5), which is exactly the center of the field.
- The robot will always be facing forward (see Desmos).
    - This case actually makes the math much easier to solve. Don't overcomplicate it.
- Calculations will be done in the 2D plane.
- The turret's angle is **counter-clockwise positive** (see Desmos).
- The robot position does **NOT have to be within field bounds** (also see Exercise->Extensions)

### Conditions
- You should use the provided Vector2 class, or your own implementation that represents a Vector2 or coordinate-pair
- You should create a separate class to contain your math for calculating turret angle given two inputs: **robot position** and **target position**
    - You can alternatively also only give the **robot position** input if you hard-code the **target position** as some sort of constant. 
- All the program needs to do is take an input position and return the turret angle, either in degrees or radians is acceptable, but ideally in degrees.
    - You can input any arbitrary input position, even if it is outside the field, as long as the turret angle it returns is correct.
    - The returned angle does not need to be rounded. Leave as-is. 

### Extensions
- Create a method associated with the Vector2 class that returns the distance between the **robot position** and **target position** and also return this value alongside the turret angle value. There are many ways to do this. 
    - The formula for distance between two points is sqrt((x2 - x1)^2 + (y2 - y1)^2). You should search this formula and how to implement it if you're not familiar with it.
- Modify your calculations such that if a given **robot position** is *invalid* (it's out of field bounds) that the calculation instead uses a position that approximates where the robot position would be on the field by "clamping the position."
    - Imagine if the robot was 5 units above the top wall, you'd calculate the robot as if it were at the top wall instead.
    - Essentially, the approximated position should never be outside of the field bounds and be a simple approximation that clamps the vector from going beyond field limits.
- Some of you may have experimented with user input through personal Java projects. Do you think you could implement something similar here for the robot position input?

### Hints
- You will likely have to search up some documentation and information about certain functions / formulas if you're interested in how it fundamentally works.
    - You can use AI for a starting place or to understand a concept. I won't control the use of AI, but it defeats the purpose of exercises and **AI is often wrong when used in real FRC applications.**
- Java has a `Math` class that you will most definitely use.
    - You will likely need to look at documentation of the Math class and all of its methods.
    - Look at the Desmos and consider what methods of the Math class you will use, there is one method that is most relevant to this application.

## Resources
### Vector2.java
{% highlight java %}
public class Vector2 {
    private double X;
    private double Y;

    public Vector2(double X, double Y) {
        this.X = X;
        this.Y = Y;
    }

    public double getX() {
        return this.X;
    }

    public double getY() {
        return this.Y;
    }
}
{% endhighlight %}

### [Desmos Representation of the Exercise](https://www.desmos.com/calculator/quuireqijl)

## Solution
A solution for this exercise will be released after an indefinite amount of time.