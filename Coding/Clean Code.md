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
