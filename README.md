Video Preview
=======================================

[![Alt text](https://img.youtube.com/vi/wT5Q2osNADw/0.jpg)](https://www.youtube.com/watch?v=wT5Q2osNADw)

Thanks for taking a look at my testing code examples. Here is what you will find in the ```tests``` folders above.

array_functions
---------------

I've rewritten of all of JavaScript's baked-in array functions with hand-made versions and tested them. The most challenging one was splice, and the code for it serves as a good example of my highest test writing abilities.

betterToFixed
-------------

I've created a hand-made version of the baked-in JavaScript function ```toFixed```. Due to the way JavaScript stores numbers, it can sometimes make rounding errors. This function I've written fixes that problem, and I've written tests to ensure it works well.

isPrototypeOf
-------------

This inheritance function checks if an object's prototype is the prototype of another object. Assuming that an object and its parent object are compared, the function will return true. The function will also traverse an inheritance hierarchy to check if an object's prototype is the same as a parent object's prototype in scenarios where there is more than one degree of separation in the lineage hierarchy.

librariesOOO
------------

This function loads libraries with dependencies and can accommodate declarations of libraries even if the definitions of their dependencies have yet to be performed. The name of the function ```librariesOOO``` is short for libraries out of order. The tests first declare a library with dependencies that have yet to be defined. But instead of halting with an error, the function makes note of the dependencies that have yet to be defined. When those dependencies are finally defined, the function identifies this event and proceeds to create the library with the one or more previously undefined dependencies.


This is an in-browser JavaScript library I've been using for years. It's so small and simple that it never occured to me to open source it until I saw all the overly complicated alternatives that are out there.

If you're looking for a JavaScript library full of features or install guides that say things like `grunt`, `npm` or `bower`, you've come to the wrong place. Sorry, this probably isn't for you. Move along now.

If you're looking for a quick way to unit-test a JavaScript function/object in a web-page and don't want to get bogged down in frameworks, you've come to the right place. Take a seat... no scratch that, you'll have everything you need in a few seconds so you may as well remain standing.

*   [Download tinytest.js](https://rawgit.com/joewalnes/jstinytest/master/tinytest.js)
*   [Example](https://github.com/joewalnes/jstinytest/tree/master/example)

10 second tutorial
------------------

Download [tinytest.js](https://rawgit.com/joewalnes/jstinytest/master/tinytest.js) and put it somewhere in your web directory.

Let's say you have a function in `adder.js`:

```javascript
function add(a, b) {
  return a + b;
}
```

Create a test page called `adder-test.html` (you can name it anything). This includes your code under test, tinytest.js and defines your tests:

```html
<script src="tinytest.js"></script>
<script src="adder.js"></script>
<script>
 tests({

   'adds numbers': function() {
     eq(6, add(2, 4));
     eq(6.4, add(2.4, 4));
   },

   'subtracts numbers': function() {
     eq(-2, add(2, -4)); 
   },

 });
</script>
```

Open the page in your browser. Green is good. Red is bad. If it's red, look in the JavaScript console for messages.

![](https://github.com/joewalnes/jstinytest/raw/master/screenshots/results-green.png)

**That's it!**

Don't believe me? Here's the [source](https://github.com/joewalnes/jstinytest/tree/master/example) and [result](https://rawgit.com/joewalnes/jstinytest/master/example/adder-test.html).

What else?
==========

If your tests fail, you'll get stack traces:

![](https://github.com/joewalnes/jstinytest/raw/master/screenshots/results-red.png)

Function reference
------------------

```javascript
// Force a failure
fail(reason);

// Assert expression is truthy (fail with reason)
assert(expression, reason);

// Assert expected == actual
assertEquals(expected, actual)
eq(expected, actual) // Alias for assertEquals

// Assert expected === actual
assertStrictEquals(expected, actual)
```

Errm that's it. Now stop wasting time - go test that function.

But, but, but. What about feature X?
------------------------------------

It probably doesn't have it. If you need that, you'll probably findIndex it in one of the many more sophisticated frameworks out there. A more detailed discussion can be found [here](http://www.pinterest.com/pin/61431982391077742/).

Projects using TinyTest
-----------------------

*   [Filtrex](https://github.com/joewalnes/filtrex) - A simple, safe, JavaScript Filter Expression compiler ([Tests](https://github.com/joewalnes/filtrex/blob/master/test/filtrex-test.html)) ([Results](https://rawgit.com/joewalnes/filtrex/master/test/filtrex-test.html))

Other stuff
-----------

I also have [TinyTest for C](https://github.com/joewalnes/tinytest) that follows similar principles of simplicity.

Now check out my other [GitHub projects](https://github.com/joewalnes) and follow [@joewalnes](https://twitter.com/joewalnes) on that Twitter thing.
