---
layout: default
title: Functions
category: Java
order: 3
---
If you remember from algebra 2, graphs are made by plugging in values into functions. For example a parabola has a function of f(x) = x^2. So any x value that you plug into f(x) will be squared. Functions are the same thing in programming, but they don't only return numbers they can return any data type.

Here's an example of what the function of a parabola would look like in Java:
{% highlight java %}
int parabola(int x) {
    return x * x;
}
{% endhighlight %}

Let's evaluate each line of the function:
{% highlight java %}
int parabola(int x) {
{% endhighlight %}
This first line is the definition of the function. Our function is called *parabola* and it has a data or return type of **int**. The parenthesis are where you pass in **arguments** a.k.a. **parameters**. The *{}* are the block of code for the function. So whatever is in between the *{}* is part of the function.

{% highlight java %}
return x*x;
{% endhighlight %}
The second line has the **return value** of the function. The return value is what is the value given back. Since this is a parabola multiplying the **argument** *x* by itself gives us the *y* value of the parabola.
> Whenever you use a function it must always return a value or else it'll error.

Here's an example of using the **parabola** function:
{% highlight java %}
int x = 3;
int y = parabola(x);
// the value of y is 9.
{% endhighlight %}
> Since the data type of *parabola* is an int we can assign the value of the function to an int variable.
