# Data is a Better Interface

CORBA turned into SOAP and REST.
https://www.youtube.com/watch?v=-6BsiVyC1kM&list=PLXsqD83He-e5oUh_DFrHbO3MoNj3tG8Vh&index=4&t=1067

Why is indirection bad?

Because we lose the context, the local data that might change between when the reference was passed, and when it is used.

Even web development, the most hairy, most state-dependant, the biggest and most widespread OOP ecosystem, has been moving towards more functional ideas, like language-level asynchronous value interfaces called [Promises](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Using_promises) and full-blown frameworks like React, which basically implements immutable values and strict side effect rules, and even monads (actions and reducers).
