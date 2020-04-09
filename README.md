Thanks for taking a look at my testing code examples. Here is what you will find in the ```tests``` folders above.

array_functions
---------------

I've rewritten of all of JavaScript's baked-in array functions with hand-made versions and tested them. The code for these serves as a good example of my test writing abilities.

Video Preview
-------------
[![Alt text](https://img.youtube.com/vi/pEbvg_hazyA/0.jpg)](https://www.youtube.com/watch?v=pEbvg_hazyA)


betterToFixed
-------------

I've created a hand-made version of the baked-in JavaScript function ```toFixed```. Due to the way JavaScript stores numbers, it can sometimes make rounding errors. This function I've written fixes that problem, and I've written tests to ensure it works well.

Video Preview
-------------
[![Alt text](https://img.youtube.com/vi/f9n8tsFh3aE/0.jpg)](https://www.youtube.com/watch?v=f9n8tsFh3aE)

isPrototypeOf
-------------

This inheritance function checks if an object's prototype is the prototype of another object. Assuming that an object and its parent object are compared, the function will return true. The function will also traverse an inheritance hierarchy to check if an object's prototype is the same as a parent object's prototype in scenarios where there is more than one degree of separation in the lineage hierarchy.

Video Preview
-------------
[![Alt text](https://img.youtube.com/vi/f9n8tsFh3aE/0.jpg)](https://www.youtube.com/watch?v=f9n8tsFh3aE)

librariesOOO
------------

This function loads libraries with dependencies and can accommodate declarations of libraries even if the definitions of their dependencies have yet to be performed. The name of the function ```librariesOOO``` is short for libraries out of order. The tests first declare a library with dependencies that have yet to be defined. But instead of halting with an error, the function makes note of the dependencies that have yet to be defined. When those dependencies are finally defined, the function identifies this event and proceeds to create the library with the one or more previously undefined dependencies.

Video Preview
-------------
[![Alt text](https://img.youtube.com/vi/f9n8tsFh3aE/0.jpg)](https://www.youtube.com/watch?v=f9n8tsFh3aE)
