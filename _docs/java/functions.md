---
layout: default
title: Functions
category: Java
order: 3
---
If you remember from algebra 2, graphs are made by plugging in values into functions. For example a parabola has a function of ***f(x) = x^2***. So any *x* value that you plug into ***f(x)*** will be squared. Functions are the same thing in programming, but they don't only return numbers they can return any data type.

Here's an example of what the function of a parabola would look like in Java:

```java
int parabola(int x) {
    return x * x;
}
```

Let's evaluate each line of the function:

```java
int parabola(int x) {
```

This first line is the definition of the function. Our function is called *parabola* and it has a data or return type of **int**. The parenthesis are where you pass in **arguments** a.k.a. **parameters**. The *{}* are the block of code for the function. So whatever is in between the *{}* is part of the function.

```java
return x*x;
```

The second line has the **return value** of the function. The return value is what is the value given back. Since this is a parabola multiplying the **argument** *x* by itself gives us the *y* value of the parabola.
> Whenever you use a function it must always return a value or else it'll error.

Here's an example of using the **parabola** function:

```java
int x = 3;
int y = parabola(x);
// the value of y is 9.
```

> Since the data type of *parabola* is an int we can assign the value of the function to an int variable.

In math there's a concept called **function composition**, basically it's where a function is equal to the value of a function that has the value of another function in it.
> In math speak it looks like this ***h(x) = f(g(x))***
> ![yo dawg](http://www.quickmeme.com/img/a2/a259c0fd97091dcfb96399f54c4bde40e99a88bd071232715033a8d7d1b45fcc.jpg "Yo dawg, I heard you like functions.")

Let's look at an example of how to do that in Java:

```java
int f(int x) {
    return x * x;
}

int g(int x) {
    return x + 2;
}

int h(int x) {
    return f(g(x));
}

int x = 5;
int y = h(x);
// The value of y is 49.
```

Let's look at what goes on beind the scenes of the function ***h***. First, *5* is plugged into the **argument** *x*. Then *5* is plugged into the function ***g*** which returns a value of *x + 2* which gives us *7*. Finally, it plugs the value of ***g(5)*** into the function ***f*** and returns the square of the argument *x*. So, the ending result is *7\*7* which is *49*.

The purpose of showing you **function composition** is to show that you can use functions within a function. Since at the end of the day, functions are just the data type you specified that just takes in an **argument**.
