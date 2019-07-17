---
layout: default
title: Main Method
category: Java
order: 5
---

The ***main*** method is a function, but it does not have a return type. This method is where all code is executed, when you run your program Java looks for this method in order to run the code you have written. So, all of your code you want to be executed should end up within this method.

Example of a main method:

```java
public static void main(String[] args) {

}
```

You're probably wondering how this method doesn't have a return type. If notice in the definition of the method it says the word **void**. You should know from english class what it means, but if you really don't it means *nothing*, literally **nothing**.

> There's two things in the example that you probably don't recognize which is ***public*** and ***static***, currently we do not need to know what these do ignore them for now. The ***String[] args*** should seem familiar, that's an array of the data type String.

Whenever you hit the run button in your code editor, in the background a command is executed to compile and run your code. The command looks like this

```console
java ProgramName arg1 arg2 arg3
```

Every time there's a space after the program name that String is added to the ***args*** array which you can reference in your program to do certain things based on what's entered into the argument.
