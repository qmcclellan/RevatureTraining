## **Methods and Functions**

### Methods
Note: Funciton and method will be used interchangeably here, but typically you will use one or the other depending on the programming language.

A method or function in programming in its most basic form is just a named set of instructions.

Imagine you had a to-do list. It might look something like this:

do laundry
go grocery shopping
vacumm
Each of these things on the list could be considered a function or method.

On your to-do list, you don't write out every single step involved in "do laundry" or "go grocery shopping".

If you did your list might look more like:

Find all dirty clothes in the house and car.
Sort the dirty clothes into piles.
Put the first pile in the washing machine
Add soap
...
Instead you simply name that particular set of actions as "do laundry".

In some cases your set of actions requires some input that should be given at the time of execution. The input will be finalized when you or you the analogous program starts the task.

Think about grocery shopping for a minute. I might have grocery shopping on my to-do list every week, but I might have to buy a different set of items from the store each week. I might keep a separate list on the fridge just to track what I have run out of. The grocery list in this case would be the input to the "grocery shop" method.

Moreover, methods can also produce some results. Think of it this way I might buy all the stuff at the store, but unless I bring it I won't be able to use it. The bought groceries will just stay at the store.

Information in a method works in much the same way. Often our methods define a particular "scope"- a little bubble that is separate from the outside program. Unless we return information to the rest of the program.

Take this "grocery shop" function. It's outlined in rough psuedo code, but it should be fairly readable.

function groceryShop ( grocery list ):
    create an empty bought items list 

    for each item on the grocery list 
        check if the store has the item 
            if it does buy the item
            add it to the list of bought items

    return bought items list
There are a couple of key components that I want to draw your attention to.

First, all we have done here is outline what the groceryShop method is. If our fake program could actually run, it wouldn't do anything because we haven't actually "called" the method yet. (You might explain to your kids what doing the laundry is, but until you command them "do laundry" - nothing happens.)

Second, "grocery list" is a parameter (just a variable that gets its value in a special way). It's a place holder for the actual grocery list that would be needed when the program runs/calls/executes the "groceryShop" method.

The final key component that is often a source of confusion is the return statement or rather the portion that reads "return bought items list".

Common questions usually run along the lines of - isn't this the same as printing out the list? Where are we returning the items to?

Returning is within the context of the program. Perhaps the next function after grocery shop is make dinner. By returning the grocery items, you ensure that the rest of the program (outside the grocery shop method) gets access to the bought items. Then we can use these bought items for other things such as "make dinner".