# NaiveTicket

The second Objects lab, from the BlueJ book's second chapter.

Look for the [Chapter 2 file](./doc/BlueJ-objects-first-ch2.pdf) you need in the [doc](./doc) folder.
There is 35 pages of reading and exercises in the chapter.

Work through all these exercises. You edit this file with your answers for these exercises.

### Exercise 2.1
* Create a TicketMachine object on the object bench.
* Upon viewing its methods, `getBalance`, `getPrice`, `insertMoney`, `printTicket`.
* Use `getPrice` method to view the value of the price of the tickets that was set when this object was created.
* Use `insertMoney` method to simulate inserting an amount of money into the machine.
* Use `getBalance` to check that the machine has a record of the amount inserted.
	* You can insert several separate amounts of money into the machine, just like you might insert multiple coins or notes into a real machine. Try inserting the exact amount required for a ticket. As this is a simple machine, a ticket will not be issued automatically, so once you have inserted enough money, call the `printTicket` method. A facsimile ticket should be printed in the BlueJ terminal window.

### Exercise 2.2
* What value is returned if you check the machine’s balance after it has printed a ticket?

The value that is passed as an argument when the instance is created.

### Exercise 2.3
* Experiment with inserting different amounts of money before printing tickets.
	* Do you notice anything strange about the machine’s behavior? 
	
	Yes, prints tickets without validation.
	
	* What happens if you insert too much money into the machine – do you receive any refund?
	
	No refund is processed.
	
	* What happens if you do not insert enough and then try to print a ticket?
	
	Still prints a ticket.

### Exercise 2.4
* Try to obtain a good understanding of a ticket machine’s behavior by interacting with it on the object bench before we start looking at how the `TicketMachine` class is implemented in the next section.

### Exercise 2.5
* Create another ticket machine for tickets of a different price.
	* Buy a ticket from that machine.
	* Does the printed ticket look different?
	
	No still looks the same unless the value given to the machine was different.
	
### Exercise 2.6
* Write out what you think the outer wrappers of the `Student` and `LabClass` classes might look like – do not worry about the inner part.

```java
public class Student {
// code
}

public class LabClass {
// code 
}
```

### Exercise 2.7
Does it matter whether we write<br>
`public class TicketMachine`<br>
or<br>
`class public TicketMachine`<br>
in the outer wrapper of a class?

Yes does not compile.
	
* Edit the source of the `TicketMachine` class to make the change and then close the editor window.
	* Do you notice a change in the class diagram?
		Yes does not compile.
	* What error message do you get when you now press the compile button?
		class, interface, enum expected.
	* Do you think this message clearly explains what is wrong?
		Yes needs one of the three things described.

### Exercise 2.8
* Check whether or not it is possible to leave out the word `public` from the outer wrapper of the `TicketMachine` class.

Yes you can.

### Exercise 2.9
* From your earlier experimentation with the ticket machine objects within BlueJ you can probably remember the names of some of the methods – `printTicket`, for instance.
	* Look at the class definition in Code 2.1 and use this knowledge, along with the additional information about ordering we have given you, to try to make a list of the names of the fields, constructors, and methods in the `TicketMachine` class.

```java
// CLASS
public class TicketMachine
{
    // FIELDS	
    private int price;
    private int balance;
    private int total;
    // CONSTRUCTOR
    public TicketMachine(int ticketCost)
    //METHODS
    public int getPrice()
    public int getAmount() 
    public int getTotal() {
    public void insertMoney(int amount)
    public void printTicket()
}
```
	* Hint: There is only one constructor in the class.

### Exercise 2.10
* Do you notice any features of the constructor that make it significantly different from the other methods of the class?
Constructor has the name of the class and does not have a return type.
### Exercise 2.11
* What do you think is the type of each of the following fields?

```java
private int count;
private Student representative;
private Server host;
```
int, Student, Server

### Exercise 2.12
* What are the names of the following fields?

```java
private boolean alive;
private Person tutor;
private Game game;
```
boolean, Person, Game

### Exercise 2.13

In the following field declaration from the TicketMachine class<br>

```java
private int price;
```
does it matter which order the three words appear in?

Yes order matters. 

* Edit the `TicketMachine` class to try different orderings. After each change, close the editor.
	* Does the appearance of the class diagram after each change give you a clue as to whether or not other orderings are possible? 

Yes lines /// doesn't compile.

	* Check by pressing the compile button to see if there is an error message.
	* Make sure that you reinstantiate the original version after your experiments!

### Exercise 2.14
* Is it always necessary to have a semicolon at the end of a field declaration?

Yes

* Once again, experiment via the editor.
* The rule you will learn here is an important one, so be sure to remember it.


### Exercise 2.15
* Write in full the declaration for a field of type `int` whose name is `status`.

```java
private int status
```

### Exercise 2.16
* To what class does the following constructor belong?

```
public Student(String name)
```

Student class

### Exercise 2.17
* How many parameters does the following constructor have and what are their types?

```
public Book(String title, double price)
```

Two paramaters - String and double

### Exercise 2.18
* Can you guess what types some of the `Book` class’s fields might be?

```java
private String author;
private int pages;
private String publisher;
private String genre;
private boolean read;
```

* Can you assume anything about the names of its fields?

You can assume their types.

Work all Exercises from 2.19 to 2.58 that are **NOT** marked *Challenge exercise*.
READ upto and INCLUDING section 2.15 of this chapter.

### Exercise 2.19 
Suppose that the class Pet has a field called name that is of type
String. Write an assignment statement in the body of the following constructor so
that the name field will be initialized with the value of the constructor’s parameter.

```java
public Pet(String petsName)
{
this.petsName = petsName;
}
```

### Exercise 2.21
Compare the getBalance method with the getPrice method.
What are the differences between them?

```java
getBalance() 
returns balance

getPrice()
returns price
```
### Exercise 2.22
If a call to getPrice can be characterized as ‘What do tickets
cost?’, how would you characterize a call to getBalance?

What amount of money was inserted.

### Exercise 2.23
If the name of getBalance is changed to getAmount, does the
return statement in the body of the method need to be changed, too? Try it out within
BlueJ.

No it does not need to be changed

### Exercise 2.24
Define an accessor method, getTotal, that returns the value of
the total field.

```java 
public int getTotal() {

returns total;

}
```
### Exercise 2.25
Try removing the return statement from the body of getPrice.
What error message do you see now when you try compiling the class?

Not a statement

### Exercise 2.26
Compare the method signatures of getPrice and printTicket
in Code 2.1. Apart from their names, what is the main difference between them?

```java
int getPrice() returns an int
void printTicket() has no return
```

### Exercise 2.27
Do the insertMoney and printTicket methods have return
statements? Why do you think this might be? Do you notice anything about their
headers that might suggest why they do not require return statements?

No both do not have return statements since they are both void.

### Exercise 2.28
Create a ticket machine with a ticket price of your choosing. Before
doing anything else, call the getBalance method on it. Now call the insertMoney
method (Code 2.6) and give a non-zero positive amount of money as the actual
parameter. Now call getBalance again. The two calls to getBalance should show
different output because the call to insertMoney had the effect of changing the
machine’s state via its balance field.

Reflects the new balance.

### Exercise 2.29
How can we tell from just its header that setPrice is a method
and not a constructor?
public void setPrice(int ticketCost)

The return type is void and it does not have the same name as the class.

### Exercise 2.30
Complete the body of the setPrice method so that it assigns the
value of its parameter to the price field.

```java
public void setPrice(int price) {
        this.price = price;
    }
```

### Exercise 2.31
Complete the body of the following method, whose purpose is to
add the value of its parameter to a field named score.
```java
/**
* Increase score by the given number of points.
*/
public void increase(int points)
{
this.score += points;
}
```
### Exercise 2.32
Can you complete the following method, whose purpose is to subtract
the value of its parameter from a field named price?

```java
/**
* Reduce price by the given amount.
*/

public void discount(int amount)
{
this.price -= amount
}
```

### Exercise 2.33
Add a method called prompt to the TicketMachine class. This
should have a void return type and take no parameters. The body of the method
should print something like:

Please insert the correct amount of money.

### Exercise 2.34
Add a showPrice method to the TicketMachine class. This
should have a void return type and take no parameters. The body of the method
should print something like:

The price of a ticket is xyz cents.

where xyz should be replaced by the value held in the price field when the method
is called.

```java
public void showPrice() {
    	System.out.printf("The price of a ticket is %s cents.", this.price)
    }
```

### Exercise 2.35
Create two ticket machines with differently priced tickets. Do calls
to their showPrice methods show the same output, or different? How do you explain
this effect?

Each instance has own state in this case their price fields are different.

### Exercise 2.36
What do you think would be printed if you altered the fourth statement
of printTicket so that price also has quotes around it, as follows?
```java
System.out.println("# " + "price" + " cents.");
```

# price cents.

### Exercise 2.37
What about the following version?
```java
System.out.println("# price cents.");
```
# price cents.

### Exercise 2.38
Could either of the previous two versions be used to show the
price of tickets in different ticket machines? Explain your answer.

Yes if the price of the different ticket machines are given the same price arguments.

### Exercise 2.39
Modify the constructor of TicketMachine so that it no longer has
a parameter. Instead, the price of tickets should be fixed at 1000 cents. What effect
does this have when you construct ticket machine objects within BlueJ?

Each created instance has a price value of 1000

### Exercise 2.40
Implement a method, empty, that simulates the effect of removing
all money from the machine. This method should have a void return type, and its
body should simply set the total field to zero. Does this method need to take any
parameters? Test your method by creating a machine, inserting some money, printing
some tickets, checking the total, and then emptying the machine. Is this method a
mutator or an accessor?

Doesn't need any parameters and this method would be a mutator method since it changes the state of the object

### Exercise 2.41
Implement a method, setPrice, that is able to set the price of
tickets to a new value. The new price is passed in as a parameter value to the
method. Test your method by creating a machine, showing the price of tickets,
changing the price, and then showing the new price. Is this method a mutator?

Yes this method is a mutator since the state is changed.

### Exercise 2.42
Give the class two constructors. One should take a single parameter
that specifies the price, and the other should take no parameter and set the price
to be a default value of your choosing. Test your implementation by creating machines
via the two different constructors.

### Exercise 2.43
Check that the behavior we have discussed here is accurate by
creating a TicketMachine instance and calling insertMoney with various actual
parameter values. Check the balance both before and after calling insertMoney.
Does the balance ever change in the cases when an error message is printed? Try to
predict what will happen if you enter the value zero as the parameter, and then see if
you are right.

It will only accept integer values even negative ones.

### Exercise 2.44
Predict what you think will happen if you change the test in
insertMoney to use the greater-than or equal-to operator:
if(amount >= 0)
Check your predictions by running some tests. What difference does it make to the
behavior of the method?

Does not accept negative values.

### Exercise 2.45
In the shapes project we looked at in Chapter 1 we used a
boolean field to control a feature of the circle objects. What was that feature? Was it well suited to being controlled by a type with only two different values?

The feature was to show the object on the canvas and it was a valid function for that feature.

### Exercise 2.46
In this version of printTicket we also do something slightly
different with the total and balance fields. Compare the implementation of the
method in Code 2.1 with that in Code 2.8 to see whether you can tell what those
differences are. Then check your understanding by experimenting within BlueJ.

There is validation to check the balance and price before printing a ticket.

### Exercise 2.47
After a ticket has been printed, could the value in the balance
field ever be set to a negative value by subtracting price from it? Justify your answer.

The balance should never be negative since the ticket will not print unless the balance is >= price

### Exercise 2.48
So far we have introduced you to two arithmetic operators, + and –,
that can be used in arithmetic expressions in Java. Take a look at Appendix D to find
out what other operators are available.
```java
% /
```
### Exercise 2.49
Write an assignment statement that will store the result of multiplying
two variables, price and discount, into a third variable, saving.
```java
int product = price * discount;
```
### Exercise 2.50
Write an assignment statement that will divide the value in total
by the value in count and store the result in mean.
```java
int mean = total / count;
```
### Exercise 2.51
Write an if statement that will compare the value in price against
the value in budget. If price is greater than budget then print the message ‘Too
expensive’, otherwise print the message ‘Just right’.
```java
if(price > budget) {
System.out.println("Too expensive");
} else {
System.out.println("Just right");
}
```
### Exercise 2.52
Modify your answer to the previous exercise so that the message if
the price is too high includes the value of your budget.
```java
if(price > budget) {
System.out.printf("Too expensive price is %d", price);
} else {
System.out.println("Just right");
}
```
### Exercise 2.53
Why does the following version of refundBalance not give the
same results as the original?
public int refundBalance()
{
balance = 0;
return balance;
}
What tests can you run to demonstrate that it does not?

You can call insertMoney() and call refundBalance() to show that it will always return zero.

### Exercise 2.54
What happens if you try to compile the TicketMachine class with
the following version of refundBalance?
public int refundBalance()
{
return balance;
balance = 0;
}

Unreachable statement.

What do you know about return statements that helps to explain why this version
does not compile?

return statments will exit the code block when executed.

### Exercise 2.55
Add a new method, emptyMachine, that is designed to simulate
emptying the machine of money. It should both return the value in total and reset
total to be zero.
```java
public int emptyMachine() {
        int machineTotal = this.total;
        this.total = 0;
        return machineTotal; 
    }
```
### Exercise 2.56
Is emptyMachine an accessor, a mutator, or both?

Both gets the total and resets it to 0

### Exercise 2.57
Rewrite the printTicket method so that it declares a local
variable, amountLeftToPay. This should then be initialized to contain the difference
between price and balance. Rewrite the test in the conditional statement to check
the value of amountLeftToPay. If its value is less than or equal to zero, a ticket
should be printed, otherwise an error message should be printed stating the amount
still required. Test your version to ensure that it behaves in exactly the same way as
the original version.

```java
public void printTicket()
    {
        int amountLeftToPay = price - balance;
        if(amountLeftToPay <= 0) {
        // Simulate the printing of a ticket.
        System.out.println("##################");
        System.out.println("# The BlueJ Line");
        System.out.println("# Ticket");
        System.out.println("# " + price + " cents.");
        System.out.println("##################");
        System.out.println();
        // Update the total collected with the price.
        total = total + price;
        // Reduce the balance by the price.
        balance -= price;
        } else {
            System.out.printf("Sorry not enough you need %d cents.", amountLeftToPay);
        }
    }
```

