---
layout: topic
title: Programming with Python
subtitle: Creating Functions
minutes: 30
---
> ## Learning Objectives {.objectives}
>
> *   Define a function that takes parameters.
> *   Return a value from a function.

If we only had one data set to analyze,
it would probably be faster to load the file into a spreadsheet
and use that to plot some simple statistics.
But we have twelve files to check,
and may have more in future.
In this lesson,
we'll learn how to write a function
so that we can repeat several operations with a single command.

Let's start by defining a function `fahr_to_kelvin` that converts temperatures from Fahrenheit to Kelvin:

~~~ {.python}
def fahr_to_kelvin(temp):
    return ((temp - 32) * (5/9)) + 273.15
~~~

The definition opens with the word `def`,
which is followed by the name of the function
and a parenthesized list of parameter names.
The **body** of the function --- the
statements that are executed when it runs --- is indented below the definition line,
typically by four spaces.

When we call the function,
the values we pass to it are assigned to those variables
so that we can use them inside the function.
Inside the function,
we use a **return statement** to send a result back to whoever asked for it.

Let's try running our function.
Calling our own function is no different from calling any other function:

~~~ {.python}
print 'freezing point of water:', fahr_to_kelvin(32)
print 'boiling point of water:', fahr_to_kelvin(212)
~~~
~~~ {.output}
freezing point of water: 273.15
boiling point of water: 273.15
~~~

We've successfully called the function that we defined,
and we have access to the value that we returned.
Unfortunately, the value returned doesn't look right.
What went wrong?


> ## FIXME {.challenge}
>
> "Adding" two strings produces their concatention:
> `'a' + 'b'` is `'ab'`.
> Write a function called `fence` that takes two parameters called `original` and `wrapper`
> and returns a new string that has the wrapper character at the beginning and end of the original:
>
> ~~~ {.python}
> print fence('name', '*')
> *name*
> ~~~

> ## FIXME {.challenge}
>
> If the variable `s` refers to a string,
> then `s[0]` is the string's first character
> and `s[-1]` is its last.
> Write a function called `outer`
> that returns a string made up of just the first and last characters of its input:
>
> ~~~ {.python}
> print outer('helium')
> hm
> ~~~
