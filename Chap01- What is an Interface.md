## What is an Interface?

When programming in Unity, it's easy to overcomplicate your code, which in turn can become harder to maintain the more you add to it. Luckily there are ways to simplify the programming workflow, one of such ways is by implementing C# Interfaces.

C# interface contains definitions of a method(s) or variable(s) that the class which uses it must implement, basically ensuring that any class that uses a certain interface has all its methods implemented. The main advantage of the interface is that it can be used by multiple classes, so instead of calling GetComponent for each script, you can get all the script references by using the interface name. Let’s see how we can implement the interface in the game.
