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

# Chapter 8 - Boundaries

## Using Third-Party Code
* Providers of third-party packages and frameworks strive for broad applicability so they can work in many environments and appeal to a wide audience. Users, on the other hand, want an interface that is focused on their particular needs. This tension can cause problems at the boundaries of our systems.
*  The use of generics is no longer a big issue because the casting and type management is handled inside the Sensors class.
* If you use a boundary interface like Map, keep it inside the class, or close family of classes, where it is used. Avoid returning it from, or accepting it as an argument to, public APIs.

## Exploring and Learning Boundaries
*  It’s not our job to test the third-party code, but it may be in our best interest to write tests for the third-party code we use.
* Instead of experimenting and trying out the new stuff in our production code, we could write some tests to explore our understanding of the third-party code. Jim Newkirk calls such tests learning tests.
* The tests focus on what we want out of the API.

## Learning Tests Are Better Than Free 
* The learning tests end up costing nothing. We had to learn the API anyway, and writing those tests was an easy and isolated way to get that knowledge. The learning tests were precise experiments that helped increase our understanding.
* When there are new releases of the third-party package, we run the learning tests to see whether there are behavioral differences. 
* Learning tests verify that the third-party packages we are using work the way we expect them to. Once integrated, there are no guarantees that the third-party code will stay compatible with our needs.
* Whether you need the learning provided by the learning tests or not, a clean boundary should be supported by a set of outbound tests that exercise the interface the same way the production code does.

## Using Code That Does Not Yet Exist
* One good thing about writing the interface we wish we had is that it’s under our control. This helps keep client code more readable and focused on what it is trying to accomplish.

## Clean Boundaries 
* Good software designs accommodate change without huge investments and rework. When we use code that is out of our control, special care must be taken to protect our investment and make sure future change is not too costly.

* Code at the boundaries needs clear separation and tests that define expectations. We should avoid letting too much of our code know about the third-party particulars. It’s better to depend on something you control than on something you don’t control, lest it end up controlling you. 

* We manage third-party boundaries by having very few places in the code that refer to them. We may wrap them as we did with Map, or we may use an ADAPTER to convert from our perfect interface to the provided interface. Either way our code speaks to us better, promotes internally consistent usage across the boundary, and has fewer maintenance points when the third-party code changes.

# Chapter 9 - Unit tests
* Our profession has come a long way in the last ten years. In 1997 no one had heard of Test Driven Development. For the vast majority of us, unit tests were short bits of throwaway code that we wrote to make sure our programs “worked.” We would painstakingly write our classes and methods, and then we would concoct some ad hoc code to test them. Typically this would involve some kind of simple driver program that would allow us to manually interact with the program we had written.
* I would write a test that made sure that every nook and cranny of that code worked as I expected it to.
* The Agile and TDD movements have encouraged many programmers to write automated unit tests, and more are joining their ranks every day. But in the mad rush to add testing to our discipline, many programmers have missed some of the more subtle, and important, points of writing good tests.

## The Three Laws of TDD
> First Law You may not write production code until you have written a failing unit test.
>Second Law You may not write more of a unit test than is sufficient to fail, and not compiling is failing.
>Third Law You may not write more production code than is sufficient to pass the currently failing test.

* These three laws lock you into a cycle that is perhaps thirty seconds long. The tests and the production code are written together, with the tests just a few seconds ahead of the production code
* What this team did not realize was that having dirty tests is equivalent to, if not worse than, having no tests. The problem is that tests must change as the production code evolves. The dirtier the tests, the harder they are to change. The more tangled the test code, the more likely it is that you will spend more time cramming new tests into the suite than it takes to write the new production code. As you modify the production code, old tests start to fail, and the mess in the test code makes it hard to get those tests to pass again.

* Test code is just as important as production code. It is not a second-class citizen. It requires thought, design, and care. It must be kept as clean as production code.

### Tests Enable the -ilities 
* If you don’t keep your tests clean, you will lose them. And without them, you lose the very thing that keeps your production code flexible. Yes, you read that correctly. It is unit tests that keep our code flexible, maintainable, and reusable. The reason is simple. If you have tests, you do not fear making changes to the code! Without tests every change is a possible bug.
* So having an automated suite of unit tests that cover the production code is the key to keeping your design and architecture as clean as possible.

## Clean Tests
* What makes tests readable? The same thing that makes all code readable: clarity, simplicity, and density of expression. In a test you want to say a lot with as few expressions as possible.

## A Dual Standard
* That is the nature of the dual standard. There are things that you might never do in a production environment that are perfectly fine in a test environment. Usually they involve issues of memory or CPU efficiency. But they never involve issues of cleanliness.

## Single Concept per Test 
* Perhaps a better rule is that we want to test a single concept in each test function. We don’t want long test functions that go testing one miscellaneous thing after another.
* So it’s not the multiple asserts in each section of Listing 9-8 that causes the problem. Rather it is the fact that there is more than one concept being tested. So probably the best rule is that you should minimize the number of asserts per concept and test just one concept per test function.

## F.I.R.S.T.
> Fast: Tests should be fast.
> Independent: Tests should not depend on each other.
> Repeatable: Tests should be repeatable in any environment.
> Self-Validating: The tests should have a boolean output.
> Timely: The tests need to be written in a timely fashion. 

# Classes
## Class Organization 
* Following the standard Java convention, a class should begin with a list of variables. Public static constants, if any, should come first. Then private static variables, followed by private instance variables. There is seldom a good reason to have a public variable. 
* Public functions should follow the list of variables. We like to put the private utilities called by a public function right after the public function itself.

## Classes Should Be Small!
* The first rule of classes is that they should be small. The second rule of classes is that they should be smaller than that.
* With functions we measured size by counting physical lines. With classes we use a different measure. We count responsibilities.
* In fact, naming is probably the first way of helping determine class size. If we cannot derive a concise name for a class, then it’s likely too large. The more ambiguous the class name, the more likely it has too many responsibilities.

### The Single Responsibility Principle 
* The Single Responsibility Principle (SRP)2 states that a class or module should have one, and only one, reason to change. This principle gives us both a definition of responsibility, and a guidelines for class size. Classes should have one responsibility—one reason to change.
* Trying to identify responsibilities (reasons to change) often helps us recognize and create better abstractions in our code.
* The problem is that too many of us think that we are done once the program works. We fail to switch to the other concern of organization and cleanliness. We move on to the next problem rather than going back and breaking the overstuffed classes into decoupled units with single responsibilities.
* However, a system with many small classes has no more moving parts than a system with a few large classes. There is just as much to learn in the system with a few large classes.
* To restate the former points for emphasis: We want our systems to be composed of many small classes, not a few large ones. Each small class encapsulates a single responsibility, has a single reason to change, and collaborates with a few others to achieve the desired system behaviors.

### Cohesion 
* Classes should have a small number of instance variables. Each of the methods of a class should manipulate one or more of those variables. In general the more variables a method manipulates the more cohesive that method is to its class. A class in which each variable is used by each method is maximally cohesive.

### Maintaining Cohesion Results in Many Small Classes
* If we promoted those four variables to instance variables of the class, then we could extract the code without passing any variables at all. It would be easy to break the function up into small pieces.
* But wait! If there are a few functions that want to share certain variables, doesn’t that make them a class in their own right? Of course it does. When classes lose cohesion, split them!
* It went from a little over one page to nearly three pages in length. There are several reasons for this growth. First, the refactored program uses longer, more descriptive variable names. Second, the refactored program uses function and class declarations as a way to add commentary to the code. Third, we used whitespace and formatting techniques to keep the program readable.

## Organizing for Change 
* For most systems, change is continual. Every change subjects us to the risk that the remainder of the system no longer works as intended. In a clean system we organize our classes so as to reduce the risk of change.
* The Sql class must change when we add a new type of statement. It also must change when we alter the details of a single statement type—for example, if we need to modify the select functionality to support subselects. These two reasons to change mean that the Sql class violates the SRP.
* Private method behavior that applies only to a small subset of a class can be a useful heuristic for spotting potential areas for improvement. However, the primary spur for taking action should be system change itself.
* Our restructured Sql logic represents the best of all worlds. It supports the SRP. It also supports another key OO class design principle known as the Open-Closed Principle, or OCP:4 Classes should be open for extension but closed for modification.

### Isolating from Change 
* Needs will change, therefore code will change. We learned in OO 101 that there are concrete classes, which contain implementation details (code), and abstract classes, which represent concepts only. A client class depending upon concrete details is at risk when those details change. We can introduce interfaces and abstract classes to help isolate the impact of those details.
* By minimizing coupling in this way, our classes adhere to another class design principle known as the Dependency Inversion Principle (DIP).5 In essence, the DIP says that our classes should depend upon abstractions, not on concrete details.

# Chapter 10 - Systems
## Separate Constructing a System from Using It
* The separation of concerns is one of the oldest and most important design techniques in our craft.

### Separation of Main 
* One way to separate construction from use is simply to move all aspects of construction to main, or modules called by main, and to design the rest of the system assuming that all objects have been constructed and wired up appropriately.
* The flow of control is easy to follow. The main function builds the objects necessary for the system, then passes them to the application, which simply uses them.

### Factories
* Sometimes, of course, we need to make the application responsible for when an object gets created.

### Dependency Injection 
* A powerful mechanism for separating construction from use is Dependency Injection (DI), the application of Inversion of Control (IoC) to dependency management.3 Inversion of Control moves secondary responsibilities from an object to other objects that are dedicated to the purpose, thereby supporting the Single Responsibility Principle. In the context of dependency management, an object should not take responsibility for instantiating dependencies itself. Instead, it should pass this responsibility to another “authoritative” mechanism, thereby inverting the control.
* True Dependency Injection goes one step further. The class takes no direct steps to resolve its dependencies; it is completely passive. Instead, it provides setter methods or constructor arguments (or both) that are used to inject the dependencies. During the construction process, the DI container instantiates the required objects (usually on demand) and uses the constructor arguments or setter methods provided to wire together the dependencies. Which dependent objects are actually used is specified through a configuration file or programmatically in a special-purpose construction module.

### Scaling Up
* It is a myth that we can get systems “right the first time.” Instead, we should implement only today’s stories, then refactor and expand the system to implement new stories tomorrow. This is the essence of iterative and incremental agility. Test-driven development, refactoring, and the clean code they produce make this work at the code level.
> Software systems are unique compared to physical systems. Their architectures can grow incrementally, if we maintain the proper separation of concerns.

### Cross-Cutting Concerns
* In principle, you can reason about your persistence strategy in a modular, encapsulated way.Yet, in practice, you have to spread essentially the same code that implements the persistence strategy across many objects. We use the term cross-cutting concerns for concerns like these. Again, the persistence framework might be modular and our domain logic, in isolation, might be modular. The problem is the fine-grained intersection of these domains.