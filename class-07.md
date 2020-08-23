# Read:07 Summary
## Python scope
### Modules: The Global Scope
* There’s only one global Python scope per program execution. This scope remains in existence until the program terminates and all its names are 
forgotten. Otherwise, the next time you were to run the program, the names would remember their values from the previous run.
* You can access or reference the value of any global name from any place in your code. This includes functions and classes
* you can’t assign global names inside functions unless you explicitly declare them as global names using a global statement
* Note: Global names can be updated or modified from any place in your global Python scope. Beyond that, the global statement can 
be used to modify global names from almost any place in your code, as you’ll see in The global Statement.
* Modifying global names is generally considered bad programming practice because it can lead to code that is:

  * Difficult to debug: Almost any statement in the program can change the value of a global name.
  * Hard to understand: You need to be aware of all the statements that access and modify global names.
  * Impossible to reuse: The code is dependent on global names that are specific to a concrete program.
* Good programming practice recommends using local names rather than global names. Here are some tips:

  * Write self-contained functions that rely on local names rather than global ones.
  * Try to use unique objects names, no matter what scope you’re in.
  * Avoid global name modifications throughout your programs.
  * Avoid cross-module name modifications.
  * Use global names as constants that don’t change during your program’s execution.
-----------------------------------------------------------------------------------------------------------
### The global Statement

* `global statement`:  With this statement, you can define a list of names that are going to be treated as global names.
* The statement consists of the global keyword followed by one or more names separated by commas. You can also use 
multiple global statements with a name (or a list of names). All the names that you list in a global statement will be mapped to
the global or module scope in which you define them.
* even though using a global statement at the top level of a module is legal, it doesn’t make much sense because any name 
assigned in the global scope is already a global name by definition

-------------------------------------------------------------------------------------------------------------
### The nonlocal Statement

* `nonlocal names` :  can be accessed from inner functions, but not assigned or updated
* If you want to modify them, then you need to use a `nonlocal statement`.
* `nonlocal statement` : with it  you can define a list of names that are going to be treated as nonlocal.
* The `nonlocal statement` :  consists of the nonlocal keyword followed by one or more names separated by commas
* you can’t use `nonlocal` outside of a nested or enclosed function. To be more precise, you can’t use a `nonlocal statement` in either
the global scope or in a local scope.
-----------------------------------------------------------------------------------------------------------





















