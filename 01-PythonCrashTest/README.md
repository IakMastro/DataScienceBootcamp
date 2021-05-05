# Python Crash Test

In this document, the very fundamentals for programming in Python are explored.

## Basic operations

Firstly, the basic operations are going to be analysed.

### Number

To use a number in python, the only thing needed is to type it down like that.


```python
1.0
```




    1.0



The first (blue) column shows the input, while the second (red) column shows the output. 1.0 is a float number. If an
integer was needed, then the .0 part is omitted.

### Addition and Subtraction

To add two numbers together in Python, the symbol '+' is used.


```python
1 + 1
```




    2



In the example above, the input is 1 + 1 while the output is 2. That is logical and really basic arithmetics. If instead
subtraction is needed instead, then instead of the '+' Python uses '-' symbol.

### Multiplication and Division

To multiply two numbers in Python, the symbol '*' is used.


```python
1 * 3
```




    3



Instead, to divide two numbers, the symbol '/' is used.


```python
1 / 2
```




    0.5



**NOTE**: On Python2, this used to return 0, but on Python3, it automatically returns the float point and if for some
reason only the integer part is needed, then a typecast is needed. Typecast is a method that change an entity from one
data type to something different and new all together.

### Power

When a number powered is needed, the symbol '**' is used. In the example below, $$2^4$$ is being calculated.


```python
2 ** 4
```




    16



### Priority of Operations

Like in the real world, Python follows the same rules.


```python
2 + 3 * 5 + 5
```




    22




```python
(2 + 3) * (5 + 5)
```




    50



### Modular

In mathematics, modular arithmetics is a system of arithmetic for integers, where numbers wrap around when reaching a
certain value, called the modulus. In Python, to calculate the modulus the symbol '%' is used. Below, there are a few
examples of how it works.


```python
4 % 2
```




    0




```python
5 % 2
```




    1




```python
8 % 2
```




    0



## Variables

Variables in Python are dynamic. That means, they do not need to be casted, like in other programming languages such as
C, C++ or Java. Simply, just call the assign '=' symbol and give the variable a name. Example:


```python
var = 2
```


```python
var
```




    2



Of course, whatever was valid before, about the operations, so it is here as well.


```python
x = 2
y = 3
```


```python
x + y
```




    5



Also, each variable can do operations with each-self. More than Once


```python
x = x + x
```


```python
x
```




    4




```python
x = x + x
```


```python
x
```




    8



### Rules

There are some rules that the naming of the variables follow. They cannot start with a number or a special character.


```python
12var = 12
```


      File "<ipython-input-20-72e2c0241394>", line 1
        12var = 12
          ^
    SyntaxError: invalid syntax




```python
$var = 12
```


      File "<ipython-input-23-f9cf05844203>", line 1
        $var = 12
        ^
    SyntaxError: invalid syntax



If the variable name is more than one word, then in Python it is used to name them like that:


```python
name_of_var = 12
```

## Comments

Sometimes, the code is not too clear what it does. Sometimes, the programmer needs to leave notes to know what is going
on, because it's not too clear. That's where comments in programming are used. Comments are a special space on the
program that the compiler always skips. To write a comment in python, it is done like that:


```python
# Comment
```

## Strings

A string is a data type used in programming that represents a text. Below are some examples of strings used in Python.


```python
'single quote string'
```




    'single quote string'




```python
"double quote string"
```




    'double quote string'




```python
"I can't go"
```




    "I can't go"



Of course, like any other type, they can be assigned to a variable as well

## Print

In Python, print is a function that sends text, variables or another object to the screen. Firstly, let's assign
a variable a string


```python
x = 'hello'
```

So far, the only way that was used to show the output was like that:


```python
x
```




    'hello'



Note that the single-notation quotes are still shown here. In a real program, the way that output is shown to the end
user is like that:


```python
print(x)
```

    hello


Note that this time, there aren't any quotes there.

### Formatting variables in print

To make life simpler, there is a better way to format the data. That is to use the symbol 'f' before the quotes and
brackets '{}' to write the variable that needs to be outputted. For example:


```python
num = 12
name = 'Sam'
```


```python
print(f'My number is {num} and my name is {name}')
```

    My number is 12 and my name is Sam


## Lists

Lists are used to store multiple items in a single variable. Lists in Python are also dynamic, that means that each
list neither has a fixed length nor a single type.

### String as list

String, essentially, is a list. A string is a big array of characters. Let's analyse this example:


```python
s = 'abcdefghijk'

```

To get an item on the list, it is needed to be accessed. Each item in the list is indexed, that means that each item
has a number attached to it, based on the position it has on the list.

$$0 \leq num\_index \leq length\_of\_list - 1$$

In other words, the index of 'a' is 0, the index of 'b' is 1, etc. To access only 'a' it is done like the example
below:


```python
s[0]
```




    'a'



The programmer can specify a range of indexes by specifying where to start and where to end the range, using the symbol
':'. Below there are 3 examples. Note the output and try to figure out how it works.


```python
s[0:]
```




    'abcdefghijk'




```python
s[:5]
```




    'abcde'




```python
s[1:4]
```




    'bcd'



### List variables

Lists are created using square brackets.


```python
[1, 2, 3]
```




    [1, 2, 3]




```python
['a', 'b', 'c']
```




    ['a', 'b', 'c']




```python
my_list = ['a', 'b', 'c']
```

To add a new element to the list, the embedded function **append** is used.


```python
my_list.append('d')
```


```python
my_list
```




    ['a', 'b', 'c', 'd']



Indexing works the same as in the strings.


```python
my_list[0]
```




    'a'




```python
my_list[1:3]
```




    ['b', 'c']



To change the value of an already assigned index of the list, it is dones like this:


```python
my_list[0] = 'NEW'
```


```python
my_list
```




    ['NEW', 'b', 'c', 'd']



### Nesting lists

Python allows nested lists like the examples below.


```python
nest = [1, 2, [3, 4]]
```


```python
nest
```




    [1, 2, [3, 4]]




```python
nest[2]
```




    [3, 4]




```python
nest[2][1]
```




    4




```python
nest = [1, 2, 3, [4, 5, ['target']]]
```


```python
nest[3]
```




    [4, 5, ['target']]




```python
nest[3][2]
```




    ['target']




```python
print(nest[3][2][0])
```

    target



