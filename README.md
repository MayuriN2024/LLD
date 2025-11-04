
<font size="3">  
# LLD
<h1>1. Solid Principle</h1>

s:  	Single Responsibility Principle	---A class should have only one reason to change (only one responsibility).
O : 	Open/Closed Principle---	Software entities should be open for extension but closed for modification.
L : 	Liskov Substitution Principle	----Subclasses should be replaceable for their base classes without breaking functionality.
I : 	Interface Segregation Principle---	No client should be forced to depend on interfaces it doesn’t use.
D : 	Dependency Inversion Principle----	Depend on abstractions, not on concrete implementations.






<h2>1. Single Responsibility Principle</h2>
 “Hey guys! Today I want to explain something very simple but super important in programming: ‘A class should have only one reason to change’.
Don’t worry, I’ll explain it with a real-life example.”

[Story – Small Shop Example]
 “Imagine there’s a person who wants to open a small shop. At first, he does everything himself—he buys the stock, cleans the shop, serves the customers, and manages money.
Now, what happens if suddenly lots of customers start coming? He can’t do everything alone anymore. He needs help!
So he hires a helper to manage the customers. Now, only the customer management part changes—the rest stays the same.
See? Only one responsibility changed. That’s exactly what we mean by ‘a class should have only one reason to change’ in programming. If a class tries to do too many things, every small change can break other parts of the code.”

[Explanation – Visual/Draw]
 (Here you can draw simple boxes on your notepad: one for Stock, one for Customers, one for Cleaning)
“So instead of one person doing everything, we divide responsibilities:
Stock management → One person


Customer service → Helper


Cleaning → Another helper


Now, if customer flow increases, only the Customer Service helper changes. Nothing else breaks.
In programming, each class should focus on one responsibility. That makes your code clean, maintainable, and easy to understand.”

Advantage: Easy to maintain 
          Better Readability 
          Reuseability







<h2>2.Open / Closed principle: </h2>

“Hey guys! Today I’m going to explain another important programming principle called Open/Closed Principle, or OCP.
It says: ‘A class should be open for extension but closed for modification.’ Sounds tricky? Don’t worry, I’ll explain with a simple example!”

[Story – Small Shop Example]
 “Remember our small shop? Initially, the shop only sells products in-store.
Now, the owner wants to increase sales, so he decides to sell products online.
Instead of changing the existing in-store sales system (closed for modification),


He adds a new online shopping feature (open for extension).


This way, the old shop system works perfectly, and we have new functionality without breaking anything!”

[Visual / Drawing Cue]
 (Draw a small shop labeled ‘In-store Sales’, then draw an arrow pointing to a new section labeled ‘Online Sales’)
“See here? The in-store section stays the same, and we just extend the shop to sell online.
In programming, this principle helps make software scalable, safe, and easy to maintain.”




<h2>3. Liskov Substitution Principle (LSP)</h2>
If a child class is used in place of a parent class, the program should still work correctly.

“Imagine the shop owner has a son. The father is running the shop now, but sometimes the son works in place of the father.
According to Liskov Substitution Principle, if the son takes over, the shop should still function correctly, and there should be no loss in profits.


The shop operations and growth remain consistent, whether the father or the son is running it.


In programming terms, this means:
A child class (son) can replace the parent class (father) anywhere,


And the program (shop) still works correctly without any unexpected issue



<h2>4. Interface Seggregation Principle:</h2>
The goal of the Interface Segregation Principle is to avoid “large” interfaces that force classes to implement unnecessary methods.
Don’t force a class to depend on interfaces it doesn’t use.

Segregation means splitting or separating something into smaller, focused parts.


Imagine a big clothing shop.
In that shop, there are different sections —
Kids’ clothes, Women’s clothes, and Winter wear.

Now suppose, the shopkeeper is asked to handle all sections together —
so whenever a customer asks for kids’ clothes,
the shopkeeper still has to go through women’s and winter sections to find what they need.

That’s a lot of extra, unnecessary work, right?

The shopkeeper is being forced to deal with sections that he doesn’t need —
just like in programming, when a class is forced to depend on interfaces it doesn’t use.



<h2>5 Dependency inversion Principle:</h2>
DIP is about depending on abstractions, not on specific details. This makes code flexible, scalable, and easier to maintain.
“High-level modules should not depend on low-level modules. Both should depend on abstractions.”

👉 High-level code = Main decision-maker / Boss logic
It decides what should happen, not how it happens.





👉 Low-level code = Worker logic / Implementation details
It knows how to perform the actual task.

Example:
Imagine I own a clothing shop.

In my shop, I have different sections — Kids, Women, and Men.
Now, I also need a payment system to complete sales.

At first, I directly connected my shop’s billing system to a Cash Payment machine.
So whenever someone bought something, the system worked only with cash.

But then, customers started asking for UPI and Credit Card options.
Now, I had to go into my billing system code and change it every time I added a new payment type.
That’s a mess 😩

This is where the Dependency Inversion Principle (DIP) helps.

According to DIP:

“High-level modules should not depend on low-level modules; both should depend on abstractions.”

So instead of directly depending on the CashPayment class,
I create an interface called PaymentMethod.

Now, my Shop (high-level code) depends on that interface — not on the actual payment type.
Each payment method (cash, UPI, card) implements that same interface.

If tomorrow I want to add Paytm or Google Pay,
I don’t need to touch the main shop code — I just add a new class.

</font>

