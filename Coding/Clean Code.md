# Chapter 1 - Clean Code
* It never will happen - a machine which build systems as soon as we speak the functionalities.
* The only way to make the deadline—the only way to
go fast—is to keep the code as clean as possible at all times.
*  being able to recognize clean code from dirty code does not mean that we know how to write clean code!
* A programmer without “code-sense” can look at a messy module and recognize the mess but will have no idea what to do about it. 
* In short, a programmer who writes clean code is an artist who can take a blank screen
through a series of transformations until it is an elegantly coded system.
* ur code should be matter-of-fact as opposed to speculative. It should contain only what is necessary. 
*  Clean code is focused. Each
function, each class, each module exposes a single-minded attitude that remains entirely
undistracted, and unpolluted, by the surrounding details.
* Clean code is code that has been taken care of.
* Reduced duplication, high expressiveness, and early building of simple abstractions.
That’s what makes clean code for me.

# Chapter 2 - Meaningful Names
* The name of the variables, methods, attributes, should tell what it represents.
*  The word variable should never appear in a variable name. The word table should never appear in a table name. 
* Distinguish names in such a way that the reader knows what the differences offer.
* Use pronounceable names.
* One difference between a smart programmer and a professional programmer is that
the professional understands that clarity is king.
* Professionals use their powers for good
and write code that others can understand.
* Classes and objects should have noun or noun phrase names like Customer, WikiPage,
Account, and AddressParser.
* Methods should have verb or verb phrase names like postPayment, deletePage, or save.
* When constructors are overloaded, use static factory methods with names that
describe the arguments.
```
Complex fulcrumPoint = Complex.FromRealNumber(23.0);
is generally better than
Complex fulcrumPoint = new Complex(23.0);
``` 
* Choose clarity over entertainment value.
* Say what you mean. Mean what you say. 
* Avoid using the same word for two purposes.
* Remember that the people who read your code will be programmers. So go ahead and use computer science (CS) terms, algorithm names, pattern names, math terms, and so forth.
* Choosing technical names for
those things is usually the most appropriate course.
* Separating solution and problem domain concepts is part of the job of a good programmer and designer. 
* The code that has more to do with problem domain concepts should have names drawn from the problem domain.
* In an imaginary application called “Gas Station Deluxe,” it is a bad idea to prefix every
class with GSD.
* Shorter names are generally better than longer ones, so long as they are clear. Add no
more context to a name than is necessary.