## **Control Flow**

### **Background**
At its core a program is just a series of instructions that execute in a particular order.

The simplest programs run instructions one at a time starting at some specified beginning and finishing at a specified end point. Just like you might do if you were following a manual or recipe.

However, a program that can only do one set of instructions in the exact same way every single time is very limited.

What about when you only want to perform certain instructions in particular cases? Maybe you're simulating getting an ice cream and you want a user to be able to choose their flavor? What if you need to do a certain set of actions repeatedly?

With the style of programming described, it would be tough or impossible to execute certain instructions conditionally. And if you wanted to repeat a certain set of actions you would have to copy and paste the instructions however many times.

How do we solve this?

Control Flow or rather statements that control the flow of the program and allow a program to execute certain instructions conditionally and/or repeat instructions.

### **If statements**
The most fundamental way a program can execute certain instructions based on particular conditions is by using an if statement.

While the exact format depends on the language you use, the general idea follows this format:

    if(some condition){
        the stuff you want to do when the condition is true
    }
This means that you will check for some condition in between the parentheses. If it's true you will do "the stuff you want to do when the condition is true".

So it might be something like

    if (It's going to rain.){
        Wear rainboots and bring an umbrella.
        }

Go about our day. 
So if it is going to rain, we "Wear rainboots and bring an umbrella." and then "Go about our day".

Otherwise we just "Go about our day".

The only difference between what we have above and an actual program is that a program will be written in a way the programming language can make sense of. Remember if I used the above phrasing but you only spoke latin you would probably have no idea what I was saying to do.

Also note that regardless of whether it's going to rain we "Go about our day" because this instruction is after the if statement.

The simple if statement usually has at least two counter parts in most programming languages, if-else and if-else-if.

With the if-else statement, we have a set of instructions that we do when the condition is true and a set we do when the condition is false.

    if (It's going to rain.){
        Wear rainboots and bring an umbrella.
    } else{
        Wear sunscreen and sunglasses.
    }
Here we either "Wear rainboots and bring an umbrella." OR "Wear sunscreen and sunglasses.". We don't do both.

Notice that the else statement didn't have its own condition because it will run whenever the condition, "It's going to rain.", specified with the if, is false.

In the situation where we want to check for another possibility when the first possibility is false we can have an else-if statement.

    if (It's going to rain.){
        Wear rainboots and bring an umbrella.
    } else if(It's going to be sunny){
        Wear sunscreen and sunglasses.
    }else{
        Do cloudy day activities.   
    }
First the program checks if it's going to rain and then, only if the first condition is false, checks if it is going to be sunny.

Depending on which is true it will either have us "Wear rainboots and bring an umbrella.", "Wear sunscreen and sunglasses.", or "Do cloudy day activities.". We will always do one and only one of those options.

By "nesting" or putting if statements inside of if statements we can get even more complex logic, but the simple if statement is still the fundamental building block.

### **Loops**
What if we want to repeat a set of instructions again and again?

This is where loops come into play.

** It's worth noting before we go any further that an if statement is not a loop. While we can place an if statment inside of a loop and we can "loop" based on certain conditions, it is incorrect to describe something as an "if-loop" or "if statement loop".

A loop is section or "block" of code that repeats so long as a certain condition is true.

Imagine if you were explaining how to manually dig a backyard pool.

Would you stand there and say?

"Use the shovel to scoop the dirt and put it in that pile." "Use the shovel to scoop the dirt and put it in that pile." "Use the shovel to scoop the dirt and put it in that pile." "Use the shovel to scoop the dirt and put it in that pile." "Use the shovel to scoop the dirt and put it in that pile." "Use the shovel to scoop the dirt and put it in that pile." "Use the shovel to scoop the dirt and put it in that pile." "Use the shovel to scoop the dirt and put it ...

Probably not.

Instead you would say something more like:

"Use the shovel to scoop out the dirt until the whole is 3 ft deep, 8ft wide and 12 ft long."

And that is the idea of a loop. Perform this set of instructions until this condition is no longer true.

We typically group loops into three kinds while, do-while, and for (though how the loops are structured depends heavily on the programming language being used).

**While loops** *(and do while loops)*
A while loop might follow this general format:

    while (some condition){
     instructions
        }
So let's break down this psuedo-code example: (Psuedo-code is just *"fake"* code. It follows the general format that you might see in any given programming language, but it's not written following the rules of a particular programming language.)

We can write the following as a loop instead.

    number = 0 

    print(number) //Prints 0 
    number = number + 1

    print(number) //Prints 1
    number = number + 1

    print(number) //Prints 2
    number = number + 1
This program prints the numbers 0, 1, 2. It would be the same as saying: (Note here // is meant to indicate a comment)

    number = 0
    while (number is less than 3){
        print(number)
         number = number + 1
    }
You can think of the steps of the loop as going

Check the condition. Is it true?
Run the instructions.
Get to the end of the loop.
Check the condition again. (likely this time with an updated value.)
So then how is this different from a do-while loop?

A *do- while* follows this format

    do {
        instructions
    }while(some condition)
In other words the condition is checked at the end. This means that a do-while loop will always execute at least once- even if the condition was never true.

## For Loops
For loops are a little tricky because they are probably most different from one language to another.

That being said for loops are typically chosen when a developer knows going in that a loop should execute a set number of times or "iterate over" a particular collection.


 ** Note to iterate over a particular collection simply means if you have something like a list of items. You first get the first item in the list, then the next, then the next and so on until you have gone through the whole list.

A traditional for loop tends to follow this format:

    for ( intialization statement; condition; update statement){

    instructions
    }
Initialization statement runs once at the beginning of the loop.
Condition is checked at the beginning of each iteration (an iteration is just a particular time the instructions run.)
Assuming the condition is true the instructions run.
The program gets to the bottom of the loop and then runs the update statement.
The update statement finishes and the condition is checked. If it's true the instructions run again and the cycle continues.

    for (x = 0 ; x < 3; x=x+1){
        print(x)
    }
This loop above would do the same thing as the while loop in the previous section. It prints *0 , 1, 2*.

While there are many more loops and nuances depending on the language, this covers the basics.

