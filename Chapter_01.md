# Chapter 1

## The main() function

Every C++ program requires a point where execution of code must start.
All C++ programs have `main()`:

```cpp
int main()
{
    return 0;
}
```

The `int` is the return type for the function (we'll get onto types soon!).

`main` is the name of the function and is a special function used as an entry point for every C++ program.

`return 0` returns an `int`. All functions with a return type must return a value of that type.

`main()` is an exception to this rule - we don't have to return a value here. The convention is to return 0 as a succesful termination.
We return -1 or 1 to tell the user "Something was bad". We'll get on to how to deal with errors a bit later on.

Notice the braces `{` and `}`

All code associated with a function goes in between those braces. This code makes the "body" of the function.

------------------------------------------------------------------------------------------------------------------------------------------------
## Printing to the screen

To write stuff onto the Console window, we need to `#include <iostream>` so we can use input and output features

```cpp
#include <iostream>

int main()
{
    std::cout << "My first program\n";
}
```

`#include` is a shorthand way of copying and pasting code written by others into our program.

`<iostream>` contains code written by other programmers that enable us to read and write to the input and output streams.

You can read the writing between the "" marks as indvidual characters flowing into `std::cout` via the `<<` operator.
`cout` is an object and the name is short for 'character output'.

The individual characters between "" marks are, when combined, known as a string literal and is what will be shown in the output when we run the program.

`\n` is special character called a 'format specifier'. when used in conjunction with any string literal, it acts as though the user has pressed the `enter` key
to go to a new line.

**Exercise:** Get this program to run. Change the output to print "Game on!"
