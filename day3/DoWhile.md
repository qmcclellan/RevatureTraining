## **Lab: Do-While Loops**

**Do-While Loop**

Objectives
Create statements that utilize do-while loops
Background
Much like the while loop, a do-while loop is a block of code used to repeat a group of statements until a condition becomes false.

The syntax for a do-while loop is as follows:

    do {
    ...
    }while (condition)
The main differences between a while loop and a do-while loop are in the syntax (the condition in a do-while loop occurs after the statements) and the fact that a do-while loop will execute its block of statements at least once regardless of the value of the condition.

The keyword do is another one of the reserved words in Java; just like while. In the above example, condition refers to a boolean expression (a variable or statement that can be evaluated as a boolean; it will either be true or false).

Writing Do-While Loops
Together we'll write out a simple do-while loop expression.

Project Setup
Open your IDE (Eclipse), and select File > New > Java Project.
Provide the name, Lab-DoWhile and click Finish. a. If a module dialog appears, click Don't Create.
Right-click on the newly created project and select New > Class.
Provide the class the name, ExampleOne and click Finish.
Now edit the file so that it looks like the following:
public class ExampleOne {

	public static void main(String args[]){
    
	}
}
Now, I want you to create a boolean variable with the name, on. Set its initial value to be false.

public class ExampleOne {

    public static void main(String args[]){
    	boolean on = false;
    }
}
Now create a do-while loop by first specifying the keyword, do. Afterwards type a set of curly braces and place a print statement that says "Inside the do-while loop".

public class ExampleOne {
	public static void main(String args[]){
		boolean on = true;
        
        do{
        	System.out.println("Inside the do-while loop");
        }
    }
}
Next, we need to specify the while condition. Type the keyword while followed by parentheses enclosing the variable on.

public class ExampleOne {

    public static void main(String args[]){
    	boolean on = false;
    	
    	do{
    		System.out.println("Inside the do-while loop");
    	} while (on);
	}
}
Now our code is complete. Run it.

You should get output like the following:



Although we've specified our condition as false, the program will execute the statement associated with our do-while loop. It should be stated again, do-while loops always execute at least once.

This concludes the lab.