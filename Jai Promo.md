# Jai Promo

Have you ever wanted a language that values your time and doesn't make you do meaningless gruntwork?

Such a language does indeed exist. It's called Jai, and it's being developed by Jonathan Blow, creator of the video games Braid and The Witness, and a bunch of other stuff, including two other languages he made to learn programming language implementation. He has more than 25 years of experience with programming and languages and shipping maintainable and high-quality software, including experience with crappy tools and languages.

This frustration led him to create a language where the build system is integrated right into the language, which greatly simplifies cross-platform development and working with large projects that have to be configurable. This means you can do multiple builds at one time, for different platforms and different feature sets, and also fetch dependencies and install them when they don't exist in the system. You can also send an email when some build fails, no need for a separate monitor program. No more project files, no more Makefiles, just one function written in the same language as the rest of your program. No more depending on specific versions of specific build systems on specific platforms. No more depending on specific package managers.

He also added a way to analyze and modify the code as it compiles, making static analysis, metaprogramming, and macros a lot easier to deal with. You can find out which parts of your program get inlined, and which parts of your program make your binary too big. You can disallow access to a certain struct member outside of whitelisted files. You can find very specific usage of some code and give the user a warning that that usage is deprecated. You can mark a variable with a note and give it special powers or limit what it can do. You can also tell the compiler that you're gonna use it as a library and have complete control over the compilation process. A very powerful tool in the right hands.

He also made the compiler parse 100,000 lines of code and build a full 3D game with an in-game editor in just one second. That's right, one second. There is an LLVM backend and a custom x86 backend, and everything but the parser is multi-threaded. He also focuses on making the error messages simple and informative and not spammy. Even template code is easily debuggable. Only the actual root problem is displayed.

The syntax has very little cruft, it was designed with easy refactoring in mind, and there is no weird template madness, header files, forward declaration, or an embedded declarative language for constraining templates like C++ Concepts. The template mechanics are easy to grasp and the more complex things use the same imperative language as the rest of the program. The procedural syntax itself has defer statements, use blocks (as described in this video at 49:57), short primitive type names ("u64" instead of "unsigned long long"), multiple return values (e.g. for error conditions), named arguments, named return values, optional "then" to separate one-line if statements, and a few other small but burden-reducing syntax features.

When you have to pass a lot of arguments down a long call chain, it can be tedious to repeat every argument and parameter. In this language, you can just push a new Context struct to a reserved register that acts as a switchable global context, giving you the short parameter list of global variables without the dangerous global state manipulation. You can use that Context struct to make a disposable pool allocator, for example. This makes manual memory management a lot easier.

There are proper modules, and you can restrict certain portions of the file to only be accessible from inside that file. That means you can create modules that work like black boxes. Encapsulation at the level of modules, just like Brian Will requested. Of course, you can modify the code during compilation and remove any restrictions you want.

This is not a complete review of the language. I left out quite a lot of features. Still, I hope this convinced you to learn more about this language. The language has been in development since September 2014, and should be released in 2020 the latest. Much to our dismay, you can't start using the language just yet. He wants to make sure that the first public version is good enough for release. There are still a few problems he needs to solve and bugs he needs to fix, even if they are niche corner cases (remember, he has a full 3D game that compiles correctly in one second).

Meanwhile, there are detailed demos of the language here:
https://www.youtube.com/watch?v=UTqZNujQOlA&list=PLmV5I2fxaiCKfxMBrNsU1kgKJXD3PkyxO&index=3

There is a slightly outdated written description of the language here:
https://github.com/BSVino/JaiPrimer/blob/master/JaiPrimer.md

If you're like me and are skeptical because this sounds too good to be true, he streams the development of the compiler and the game engine (stress test for the language) here:
https://www.twitch.tv/naysayer88/videos
