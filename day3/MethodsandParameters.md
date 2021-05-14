## **Lab: Methods with Parameters**

**Methods and Parameters**
## Objectives

Explore how to write simple methods with parameters
Background
In this exercise, you'll practice writing a method that declares parameters.

Recall that a method has several parts:

modifier
return_type
methodName
parameters
exceptions
method body
The following is the syntax of a method:

modifier return_type methodName(parameters) exceptions {
    //method body
}
Parameters
Parameters are input values that your method can accept. You can have any number of parameters that you like.

You probably shouldn't write methods that declare very long lists of parameters as it'll get very difficult to manage.

Guided Practice
Now that you have some background on the basics of methods, let's write a few together. 

Project Setup
Open your IDE (Eclipse), and select File > New > Java Project.
Provide the name, Lab-MethodParameters and click Finish. a. If a module dialog appears asking to create a module, then click Don't Create.
Right-click on the newly created project and select New > Class.
Provide the class the name, MethodParams and click OK.
Now edit the file so that it looks like the following:
public class MethodParams{

    public static void main(String[] args) {
        //create a class instance
        MethodParams mp = new MethodParams();

        //call your method here
    }

    //create your first method here 
}
With the above code, we have create a main method and declared a new instance of our class MethodParams and assigned it to the variable mp.

Method with a Parameter
You can create methods that accept arguments (values). All you need to do is specify a parameter (a variable) for each input that you need.

Let's create a method that will accept one int type and return it as a double to the user. The name of the method will be convertIntToDouble. So our method should look like the following.

//create your first method here
public double convertIntToDouble(int num){
    return (double)num;
} 
In the above code, we specified an int parameter named num. We could've named it anything that we wanted, as long as it followed the same rules for variables. We also declared the method public with no exceptions, and specified the return type as double. 

Putting it together in our class, we'll declare the method outside of main but still inside our class MethodParams. Your class should look like the following:

public class MethodParams{

    public static void main(String[] args) {
        //create a class instance 
        MethodParams mp = new MethodParams();

        //call your method here
    }

    //create your first method here
    public double convertIntToDouble(int num){
        return (double)num;
    } 
}
Invoking Your Methods
You can only call methods by using the dot-operator on a variable that refers to the class type. In this case, our variable mp needs to call convertIntToDouble(..).

Edit the file so that it calls our method from an instance of MethodParams and prints the value to the console:

public class MethodParams{

    public static void main(String[] args) {
        //create a class instance
        MethodParams mp = new MethodParams();

        //call your method here and assign the returned value to a new variable `d`
        double d = mp.convertIntToDouble(44);

        //print the value to the console
        System.out.println(d);
    }

    //create your first method here
    public double convertIntToDouble(int num){
        return (double)num;
    } 
}
In the above we added two lines of code with comments. The first will invoke the method convertIntToDouble through the mp variable and then stores the returned value in a new variable d of type double. The next line then prints the returned value to the console.

Use your IDE to now run the program. You'll see output on the console displaying the value that you passed to your method.



You see that we invoked the method with an argument (44), cast the value to be a double (which made it 44.0) and returned it and later printed it to the console.

Using Multiple Parameters
We'll now create a method that accepts multiple parameters. All we need to do is separate each argument with a comma.

Edit the file to create a new method sum() that defines three parameters. One should be a double and two can be an int. It should return a double that is a result of adding each parameter together.

//new sum method here
public double sum(double num1, int num2, int num3){
    return num1 + num2 + num3;  
} 
Your class file should now look like the following:

public class MethodParams{

    public static void main(String[] args) {
        //create a class instance
        MethodParams mp = new MethodParams();

        //call your method here
        double d = mp.convertIntToDouble(44);

        //print the value to the console
        System.out.println(d);
    }

    //create your first method here
    public double convertIntToDouble(int num){
        return (double)num;
    }

    //new sum method here
    public double sum(double num1, int num2, int num3){
        return num1 + num2 + num3;
    } 
}
Now invoke this method from the main() method and print the result to the console. You should pass in the arguments 1.0, 2, and 3.

Your class file should look like the following.

public class MethodParams{

    public static void main(String[] args) {
        //create a class instance
        MethodParams mp = new MethodParams();

        //call your method here
        double d = mp.convertIntToDouble(44);

        //print the value to the console
        System.out.println(d);

        //call the 2nd method here
        System.out.println(mp.sum(1.0, 2, 3));
    }

    //create your first method here
    public double convertIntToDouble(int num){
        return (double)num;
    }

    //new sum method here
    public double sum(double num1, int num2, int num3){
        return num1 + num2 + num3;
    } 
}
In the above code, notice that we didn't store the returned value from our sum method into a variable. We simply invoked the method as an argument to the println() method. This is valid because the return type of the method is a valid argument to the println() method. If the method specified a non-valid type, say void, for example, then the compiler would display an error.

Run the program. You'll see the value of the returned result on the console.



In this case, the value 6.0 is displayed on the console. This is the correct sum of the arguments that were provided.

Congratulations. You can create methods with parameters now.

This concludes the lab.

