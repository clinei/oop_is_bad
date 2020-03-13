# Design Methodology from Scratch

This is a work in progress. Only the basic ideas are shown, and some of them are not intuitive or easy to prove. Still, these ideas should be a good starting point to develop a wholesome understanding of programming, and how to do it better than current methods.

We are going to develop a design methodology from the raw, basic facts that everyone agrees with.
Forget everything you know about programming, and let your mind go blank.
If something seems confusing, read the entire list again until you understand.

1.  Humans have problems.
2.  We create programs to solve problems because they can do it faster, better, and on a larger scale than our brains ever could.
3.  We use hardware to run those programs as highly controlled physical processes.
4.  Problems have a beginning state that we don't like and an end state that we do like.
5.  We represent state as answers to a series of yes/no questions called bits in computer memory, that we call data.
6.  We call the beginning state "input data" and the end state "output data".
7.  Data is not the state, only a representation of it, and there are many ways to represent the same state.
8.  State can be explicit, that means stored in memory, or implicit, that means able to be inferred from other data.

9.  We solve problems by taking the input data and doing operations on it until it turns into more useful output data.
10. The operations we use to turn data into more useful data is called code.
11. Code gives data meaning in the context of a program currently solving a problem.
12. Data can be more easily managed, reused, and reinterpreted, than code, because it lacks inherent meaning.
13. Data and code have no meaning outside the context of a program that is currently solving a problem.
14. When the problem changes, the data has to change, so the code has to change.
15. The less code and data we have, the easier it is to change it.
16. What the code can do and how depends on what data is available.
17. The more domain knowledge, context, and data the code can use, the easier it is to write it, and the more efficient it will be.

18. An interface is an agreement between two pieces of code, to share information in a specific way.
19. When an interface has to change, everything that uses that interface also has to change.
20. When the interface is based on data instead of code, it is easier to change the interface and whatever uses it.
21. The simpler our interfaces and the less of them we have, the less code and intermediate state our program will need, and the easier our program will be to understand.

22. A collection of operations that has a well-defined interface based on data is called a function, and the input data is called parameters and the output data is called return values.
23. When the result of the function depends only on its parameters and not any external state, we call it a pure function.
24. Pure functions are easier to understand than a group of functions that depend on external state, because all the dependencies are in one place, and the code and state is smaller.
25. For the same reasons, it is easier to change the implementation of pure functions, and to combine, refactor, and reuse them.

26. Proving that the program works correctly, that is, it returns the correct output data when given some specific input data, is called testing.
27. The less code we have, the less we have to test.
28. Proving the correctness of a group of pure functions is easier than doing the same for a group of functions that depend on external state, for the same reasons that it is easier to understand them.
29. Testing pure functions that take and return structured data can be as simple as a bitwise comparison, and the input data can be a simple array of bytes.


30. Problems are easier to solve when we use a mental model that best fits our purposes and capabilities.
31. We often don't have a good mental model or problem formulation before we start writing the program.
32. The problem formulation may change, and often does, because we want to solve more problems better.
33. The hardware may change, so we have to change the way we solve our problem.
34. Because of that, we need to be able to change the way we solve the problem as easily as possible.
35. We need to be able to change the input and output data, and the transformations and interfaces in between, as easily as possible.

