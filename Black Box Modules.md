# Black Box Modules

There are many ways to structure a program and organize the development process. One way is to keep the structure simple and easy to understand as a whole, but require that the developer thinks about the whole structure of the program and other components, as they add or change code. Another way is to not care about structure at all, and only require that the programmer thinks about a small set of things, different for each component.

I call these different methods System-based thinking and Component-based thinking.

Component-based thinking can make programmers miss obvious solutions, because the method demands that we encapsulate our thoughts, and forces us to think only inside the box. The solution can be seen only when thoughts from different boxes can interact, and because that's not allowed, we will never see it.

Component-based thinking means we can't trust or know a lot about the environment, so we have to write out a lot more assumptions and expectations that could've been left implicit if we used System-based thinking. This means we use more code.

If a system was built using Component-based thinking, then the bigger it is, and the harder it is to understand, because there is a lot more code, with a lot of repetitions, and complex interfaces that explicitly demand that the connections between the components have to remain the same.
