# Hello World

## Create a new file called HelloWorld.java

This is what all files pretty much look like in Java that have nothing in them.

```java
public class HelloWorld {

}
```

You're probably wondering what all of this means, so let's start from the beginning.

What does ```public``` mean?
> This is an *access modifier*, in simpler terms it identifies how other files can use it.

What about ```class```?
> Every file in Java has a type and for our ```HelloWorld.java``` file the type is a ```class```. There's also other types such as ```enums``` and ```interfaces```, but those are for a later lesson.

What's ```HelloWorld```?
> Since we called our file ```HelloWorld.java``` our class' name **must** be the same name as our file.

Why are there ```{}```'s?
> ```{}```'s tell Java where your class starts and ends. So if you were to put anything into your class, you must put them inbetween the opening curly-brace ( ```{``` ) and closing curly-brace ( ```}``` )

---

## The main method

Copy paste this code inside of your class.

```java
public static void main(String[] args) {
    System.out.println("Hello World!"); // This will make your computer say Hello World!
}
```



## main(String[] args)

What is this? It is called the main method. Every program in existence has a main method. This is the method that is called when the program is ran. You don't have to worry about what ```String[] args``` means yet, we'll learn what that is in a later lesson. 

## System.out.println("Hello World!");

System is Java's built in word for your computer. out means output to your computer. println is shorthand for print line. So we're printing out a line to the output of your computer.