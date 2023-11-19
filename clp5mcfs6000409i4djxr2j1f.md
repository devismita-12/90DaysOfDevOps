---
title: "Keywords and Variables in Python"
datePublished: Sun Nov 19 2023 15:14:27 GMT+0000 (Coordinated Universal Time)
cuid: clp5mcfs6000409i4djxr2j1f
slug: keywords-and-variables-in-python

---

Keywords are reserved words in Python that have predefined meanings and cannot be used as variable names or identifiers. These words are used to define the structure and logic of the program. They are an integral part of the Python language and are case-sensitive, which means you must use them exactly as specified.

| Keyword | Description |
| --- | --- |
| [and](https://www.w3schools.com/python/ref_keyword_and.asp) | A logical operator |
| [as](https://www.w3schools.com/python/ref_keyword_as.asp) | To create an alias |
| [assert](https://www.w3schools.com/python/ref_keyword_assert.asp) | For debugging |
| [break](https://www.w3schools.com/python/ref_keyword_break.asp) | To break out of a loop |
| [class](https://www.w3schools.com/python/ref_keyword_class.asp) | To define a class |
| [continue](https://www.w3schools.com/python/ref_keyword_continue.asp) | To continue to the next iteration of a loop |
| [def](https://www.w3schools.com/python/ref_keyword_def.asp) | To define a function |
| [del](https://www.w3schools.com/python/ref_keyword_del.asp) | To delete an object |
| [elif](https://www.w3schools.com/python/ref_keyword_elif.asp) | Used in conditional statements, same as else if |
| [else](https://www.w3schools.com/python/ref_keyword_else.asp) | Used in conditional statements |
| [except](https://www.w3schools.com/python/ref_keyword_except.asp) | Used with exceptions, what to do when an exception occurs |
| [False](https://www.w3schools.com/python/ref_keyword_false.asp) | Boolean value, result of comparison operations |
| [finally](https://www.w3schools.com/python/ref_keyword_finally.asp) | Used with exceptions, a block of code that will be executed no matter if there is an exception or not |
| [for](https://www.w3schools.com/python/ref_keyword_for.asp) | To create a for loop |
| [from](https://www.w3schools.com/python/ref_keyword_from.asp) | To import specific parts of a module |
| [global](https://www.w3schools.com/python/ref_keyword_global.asp) | To declare a global variable |
| [if](https://www.w3schools.com/python/ref_keyword_if.asp) | To make a conditional statement |
| [import](https://www.w3schools.com/python/ref_keyword_import.asp) | To import a module |
| [in](https://www.w3schools.com/python/ref_keyword_in.asp) | To check if a value is present in a list, tuple, etc. |
| [is](https://www.w3schools.com/python/ref_keyword_is.asp) | To test if two variables are equal |
| [lambda](https://www.w3schools.com/python/ref_keyword_lambda.asp) | To create an anonymous function |
| [None](https://www.w3schools.com/python/ref_keyword_none.asp) | Represents a null value |
| [nonlocal](https://www.w3schools.com/python/ref_keyword_nonlocal.asp) | To declare a non-local variable |
| [not](https://www.w3schools.com/python/ref_keyword_not.asp) | A logical operator |
| [or](https://www.w3schools.com/python/ref_keyword_or.asp) | A logical operator |
| [pass](https://www.w3schools.com/python/ref_keyword_pass.asp) | A null statement is a statement that will do nothing |
| [raise](https://www.w3schools.com/python/ref_keyword_raise.asp) | To raise an exception |
| [return](https://www.w3schools.com/python/ref_keyword_return.asp) | To exit a function and return a value |
| [True](https://www.w3schools.com/python/ref_keyword_true.asp) | Boolean value, the result of comparison operations |
| [try](https://www.w3schools.com/python/ref_keyword_try.asp) | To make a try...except statement |
| [while](https://www.w3schools.com/python/ref_keyword_while.asp) | To create a while loop |
| with | Used to simplify exception handling |
| yield | To end a function, return a generator |

# Python Variables

A variable is the name given to a memory location. A value-holding Python variable is also known as an identifier. Since Python is an infer language that is smart enough to determine the type of a variable, we do not need to specify its type in Python.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700402187032/5520f664-01d3-45f0-aca9-d32123a6f37c.png align="center")

<mark>Example</mark>

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700402170434/9c2a153e-ef57-4361-9b5e-ed302ee190f1.png align="center")

### Variable Scope and Lifetime:

**Variable Scope:** In Python, variables have different scopes, which determine where in the code the variable can be accessed. There are mainly two types of variable scopes:

1. **Local Scope:** Variables defined within a function have local scope and are only accessible inside that function.
    

def my\_function(): x = 10 # Local variable print(x)

my\_function() print(x) # This will raise an error since 'x' is not defined outside the function.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700406308722/6603381b-3d3b-45d0-b73e-51a127c0f975.png align="center")

1. **Global Scope:** Variables defined outside of any function have a global scope and can be accessed throughout the entire code.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700406414718/1c1f79b4-0941-4997-82a7-061631e011b3.png align="center")