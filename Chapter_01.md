# Chapter 1

## The main() function

Every C++ program requires a point where execution of code must start.
In our programs, it'll be `main()`:

```cpp
int main()
{
    return 0;
}
```

The `int` is the return type for the function (we'll get onto types soon!).

`main` is the name of the function and is a special function in C++ used as an entry point to our program.

`return 0` returns an `int`. All functions with a return type must return a value of that type.

`main()` is an exception to this rule - we don't have to return a value here. The convention is to return 0 as a succesful termination.
We return -1 or 1 to tell the user "Something was bad"
