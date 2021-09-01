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

# Chapter 3 - Functions
* Functions should not be 100 lines long.
Functions should hardly ever be 20 lines long.
* Every function in this program was just two, or three, or four lines long. Each was transparently obvious. Each told
a story. And each led you to the next in a compelling order. That’s how short your functions
should be!
* Therefore, the indent level of a function should not be greater than one or two. 
* FUNCTIONS SHOULD DO ONE THING. THEY SHOULD DO IT WELL.
THEY SHOULD DO IT ONLY.
* Another way to know that a function is doing more than “one thing” is if you can
extract another function from it with a name that is not merely a restatement of its implementation 
* Functions that do one thing cannot be reasonably divided into sections.
* In order to make sure our functions are doing “one thing,” we need to make sure that the
statements within our function are all at the same level of abstraction.
* The smaller and more focused a function is, the easier it is to choose a descriptive
name.
* A long descriptive name is better than a short
enigmatic name.
* A long descriptive name is better than a long descriptive comment.
* Be consistent in your names. Use the same phrases, nouns, and verbs in the function
names you choose for your modules.
* The similar phraseology in those names allows the sequence to tell a story.
*  Imagine the difficulty of
writing all the test cases to ensure that all the various combinations of arguments work
properly
* One input argument is the next best thing to no arguments.
* You should choose names that make the distinction clear, and always use the two
forms in a consistent context.
* Even obvious dyadic functions like assertEquals(expected, actual) are problematic.
How many times have you put the actual where the expected should be?
* Anything that forces you to check the function signature is equivalent to a double-take. It’s
a cognitive break and should be avoided.
# Chapter 4 - Comments
* If our programming languages were expressive enough, or if we had the talent to subtly wield those languages to express our intent, we would not need comments very much—perhaps not at all.
* The proper use of comments is to compensate for our failure to express ourself in code.
* Every time you write a comment, you should grimace and feel the failure of your ability of
expression.
* The older a comment is, and the farther away it is from the code it describes, the more likely it is to be just plain wrong. 
* I would rather that energy go toward making the code so clear and expressive that it does not need the comments in the first place.
* Inaccurate comments are far worse than no comments at all.
*  Only the code can truly tell you what
it does. 
* One of the more common motivations for writing comments is bad code.
* Unfortunately,
many programmers have taken this to mean that code is seldom, if ever, a good means for
explanation. 
* In many cases it’s simply a matter of creating a function that says the same thing as the comment you want to write.
* Sometimes our corporate coding standards force us to write certain comments for legal
reasons. 
# Chapter 5 - Formatting
* You should take care that your code is nicely formatted. You should choose a set of simple rules that govern the format of your code, and then you should consistently apply those rules. If you are working on a team, then the team should agree to a single set of formatting rules and all members should comply. It helps to have an automated tool that can apply those formatting rules for you.
## The Purpose of Formatting
* First of all, let’s be clear. Code formatting is important. It is too important to ignore and it is too important to treat religiously. Code formatting is about communication, and communication is the professional developer’s first order of business.
* The functionality that you create today has a good chance of changing in the next release, but the readability of your code will have a profound effect on all the changes that will ever be made. The coding style and readability set precedents that continue to affect maintainability and extensibility long after the original code has been changed beyond recognition. Your style and discipline survives, even though your code does not.
## The Newspaper Metaphor
* We would like a source file to be like a newspaper article. The name should be simple but explanatory. The name, by itself, should be sufficient to tell us whether we are in the right module or not. The topmost parts of the source file should provide the high-level concepts and algorithms. Detail should increase as we move downward, until at the end we find the lowest level functions and details in the source file.
## Vertical Openness Between Concepts 
* Nearly all code is read left to right and top to bottom. Each line represents an expression or a clause, and each group of lines represents a complete thought. Those thoughts should be separated from each other with blank lines.
## Vertical Density 
* If openness separates concepts, then vertical density implies close association. So lines of code that are tightly related should appear vertically dense.

# Chapter 6 - Objects and Data Structures

## Data Abstraction
* there is no way you can tell whether the implementation is in rectangular or polar coordinates. It might be neither! And yet the 
interface still unmistakably represents a data structure.
* Hiding implementation is not just a matter of putting a layer of functions between the variables. Hiding implementation is about abstractions! A class does not simply push its variables out through getters and setters. Rather it exposes abstract interfaces that allow its users to manipulate the essence of the data, without having to know its implementation.
* We do not want to expose the details of our data. Rather we want to express our data in abstract terms. This is not merely accomplished by using interfaces and/or getters and setters. Serious thought needs to be put into the best way to represent the data that an object contains. The worst option is to blithely add getters and setters.

## Data/Object Anti-Symmetry
*  Objects hide their data behind abstractions and expose functions that operate on that data. Data structure expose their data and have no meaningful functions.
> Procedural code (code using data structures) makes it easy to add new functions without changing the existing data structures. OO code, on the other hand, makes it easy to add new classes without changing existing functions. 

>The complement is also true: Procedural code makes it hard to add new data structures because all the functions must change. OO code makes it hard to add new functions because all the classes must change.

* Mature programmers know that the idea that everything is an object is a myth. Sometimes you really do want simple data structures with procedures operating on them.

## The Law of Demeter
* There is a well-known heuristic called the Law of Demeter2 that says a module should not know about the innards of the objects it manipulates. As we saw in the last section, objects hide their data and expose operations. This means that an object should not expose its internal structure through accessors because to do so is to expose, rather than to hide, its internal structure.
* The following code3 appears to violate the Law of Demeter (among other things) because it calls the getScratchDir() function on the return value of getOptions() and then calls getAbsolutePath() on the return value of getScratchDir().
> final String outputDir = ctxt.getOptions().getScratchDir().getAbsolutePath();

## Conclusion
* Objects expose behavior and hide data. This makes it easy to add new kinds of objects without changing existing behaviors. It also makes it hard to add new behaviors to existing objects. Data structures expose data and have no significant behavior. This makes it easy to add new behaviors to existing data structures but makes it hard to add new data structures to existing functions. 
* In any given system we will sometimes want the flexibility to add new data types, and so we prefer objects for that part of the system. Other times we will want the flexibility to add new behaviors, and so in that part of the system we prefer data types and procedures. Good software developers understand these issues without prejudice and choose the approach that is best for the job at hand.

# Chapter 7 - Error Handling

* Error handling is important, but if it obscures logic, it’s wrong.
* The caller must check for errors immediately after the call. Unfortunately, it’s easy to forget. For this reason it is better to throw an exception when you encounter an error. The calling code is cleaner. Its logic is not obscured by error handling.
* The caller must check for errors immediately after the call. Unfortunately, it’s easy to forget. For this reason it is better to throw an exception when you encounter an error. The calling code is cleaner. Its logic is not obscured by error handling.

## Write Your Try-Catch-Finally Statement First 

* One of the most interesting things about exceptions is that they define a scope within your program. When you execute code in the try portion of a try-catch-finally statement, you are stating that execution can abort at any point and then resume at the catch. 
* In a way, try blocks are like transactions. Your catch has to leave your program in a consistent state, no matter what happens in the try. For this reason it is good practice to start with a try-catch-finally statement when you are writing code that could throw exceptions.

## Use Unchecked Exceptions
* Consider the calling hierarchy of a large system. Functions at the top call functions below them, which call more functions below them, ad infinitum. Now let’s say one of the lowest level functions is modified in such a way that it must throw an exception. If that exception is checked, then the function signature must add a throws clause. But this means that every function that calls our modified function must also be modified either to catch the new exception or to append the appropriate throws clause to its signature. Ad infinitum. The net result is a cascade of changes that work their way from the lowest levels of the software to the highest! Encapsulation is broken because all functions in the path of a throw must know about details of that low-level exception. Given that the purpose of exceptions is to allow you to handle errors at a distance, it is a shame that checked exceptions break encapsulation in this way.

## Provide Context with Exceptions 
* Each exception that you throw should provide enough context to determine the source and location of an error. 
* Create informative error messages and pass them along with your exceptions. Mention the operation that failed and the type of failure. If you are logging in your application, pass along enough information to be able to log the error in your catch.

## Define Exception Classes in Terms of a Caller’s Needs
*  when we define exception classes in an application, our most important concern should be how they are caught.
* Wrappers like the one we defined for ACMEPort can be very useful. In fact, wrapping third-party APIs is a best practice. When you wrap a third-party API, you minimize your dependencies upon it: You can choose to move to a different library in the future without much penalty. Wrapping also makes it easier to mock out third-party calls when you are testing your own code.
* Often a single exception class is fine for a particular area of code. The information sent with the exception can distinguish the errors. Use different classes only if there are times when you want to catch one exception and allow the other one to pass through.

## Define the Normal Flow
* The bulk of your code will start to look like a clean unadorned algorithm. However, the process of doing this pushes error detection to the edges of your program. You wrap external APIs so that you can throw your own exceptions, and you define a handler above your code so that you can deal with any aborted computation. Most of the time this is a great approach, but there are some times when you may not want to abort.

## Don't Return Null
* If you work in a code base with code like this, it might not look all that bad to you, but it is bad! When we return null, we are essentially creating work for ourselves and foisting problems upon our callers. All it takes is one missing null check to send an application spinning out of control.
* It’s easy to say that the problem with the code above is that it is missing a null check, but in actuality, the problem is that it has too many. If you are tempted to return null from a method, consider throwing an exception or returning a SPECIAL CASE object instead. If you are calling a null-returning method from a third-party API, consider wrapping that method with a method that either throws an exception or returns a special case object.

## Don’t Pass Null
* Unless you are working with an API which expects you to pass null, you should avoid passing null in your code whenever possible.
* In most programming languages there is no good way to deal with a null that is passed by a caller accidentally. Because this is the case, the rational approach is to forbid passing null by default. When you do, you can code with the knowledge that a null in an argument list is an indication of a problem, and end up with far fewer careless mistakes.

## Conclusion
* Clean code is readable, but it must also be robust. These are not conflicting goals. We can write robust clean code if we see error handling as a separate concern, something that is viewable independently of our main logic. To the degree that we are able to do that, we can reason about it independently, and we can make great strides in the maintainability of our code.