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

Hence, `#include <iostream>` is a copy and paste of input and output functionality.

You can read the writing between the "" marks as indvidual characters flowing into `std::cout` via the `<<` operator.
`cout` is an object and the name is short for 'character output'.

The individual characters between "" marks are, when combined, known as a string literal and is what will be shown in the output when we run the program.

`\n` is special character called a 'format specifier'. when used in conjunction with any string literal, it acts as though the user has pressed the `enter` key
to go to a new line.

`std` is a `namespace` where code is written for objects such as `cout`. So we use the scope resolution operator `::` to access `cout` inside the `namespace` `std`.
So `std::cout` can be read as the `cout` that belongs in the `namespace` `std`.

The `;` at the end of the line is a terminating statement - it works in a way so the compiler knows when a statement ends.

**Exercise 1.1:** Get this program to run. Change the output to print "Game on!".

**Exercise 1.2:** Get the program to produce errors. For example, experiment changing the name of `main` to `Main` or `std::cout` to `STd::cout'.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Data Types

C++ has built in data types `int` `double` `char` `bool`, to name a few.

We can store a value inside a 'box' to use for later when needed. These boxes reside in our computer's memory and are called objects.

An object is a region of memory that has a type associated with it. For example, 

`int val = 10;`

is an object in memory of type `int` that contains the value `10`. 

We gave the object a name `val` so that we could refer to that object in memory when needed - how else would we find that value in memory?

`=` is the assignment operator. It puts whatever value is on the right and puts it into the object on the left.

On the left-hand side of the `=` operator is the LValue, an object in memory with a type.

On the right-hand side of the `=` operator is the RValue, the value inside an object in memory.

```cpp
double d = 12.4;
double d2 = d;
```

Try and work out what these two lines do. The main takeaway is the idea of an L and R value.

The line `double d2 = d;` puts the value stored inside `d` (rvalue) into the object in memory named `d2` (lvalue).

We can print the values in these objects by writing:

`std::cout << d << " " << d2 << '\n';`



