# What does // mean in Python?

[![Python](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse1.mm.bing.net%2Fth%3Fid%3DOIP.R8GHc7o8W0QH5txy-_0bQgHaCb%26pid%3DApi&f=1&ipt=151fba3b81f7567ede1f8e7c5d480e835cfced8338067bdfdaf82fba73447ecc&ipo=images "Python")](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse1.mm.bing.net%2Fth%3Fid%3DOIP.R8GHc7o8W0QH5txy-_0bQgHaCb%26pid%3DApi&f=1&ipt=151fba3b81f7567ede1f8e7c5d480e835cfced8338067bdfdaf82fba73447ecc&ipo=images "Python")


------------

*Spoiler Alert: It´s not for comments!*

In many programming languages we have become acquainted with the use of these symbols `//` as a way to introduce a comment, which is a very useful and a highly advice habit to develop into your life as a developer, for you and future developers that´ll use your code or to bypass a buggy piece of code. So, if it´s not for commenting a line, what does `//` mean in python?

In Python, the double slash `//` is an Operator, used to perform floor division. But what exactly is a floor division? A floor division is when you divide 2 numbers and then round the result down to the nearest whole number (in our case, we call it "integer").

## What you´ll find in this article:

•	Basic Syntax of the  floor division operator `// `
•	Floor Division Examples
•	What’s the difference between `//` and `Math.floor() `
•	The Double Slash Operator `//` under the hood
•	Conclusion

## Basic Syntax of the floor division operator `//` (How To)

The complete syntax for using this operator it´s just as simple as the normal, usual division with a single slash / but here´s the catch, you use the double slash // instead! 

`numberOne // numberTwo`

## Floor Division Examples

For our example we will be using two numbers which division will not give us an integer (whole number), more precisely we´ll be using 10 and 3 as the result would be, 3.333333333....

    numberOne = 10
    numberTwo = 3
    numberThree = numberOne // numberTwo
    
    print("Floor division of", numberOne, "by", numberTwo, "=", numberThree)
    # Output: floor division of 10 by 3 = 3
    
If we would use the single slash `/` operator instead, we would have that numberThree is 3.3333

    numberOne = 10
    numberTwo = 3
    numberThree = numberOne // numberTwo
    
    print("Division of", numberOne, "by", numberTwo, "=", numberThree)
    # Output: floor division of 10 by 3 = 3.3333

As seen in action, the Floor Division of 2 numbers will round down to the nearest integer (whole number).

Take in consideration, that it won’t matter if the decimal is above 5 (example: 9), the double slash operator `//` will still round it down the nearest integer (whole number).

    numberOne = 15 
    numberTwo = 4 
    numberThree = numberOne / numberTwo
    numberFour = numberOne // numberTwo
    
    print("Normal division: ", num1, "by", num2, "=", num3)
    print("Floor division: ", num1, "by", num2, "=", num4)
    
    """
    Output:
    Normal division of 15 by 4 = 3.75
    Floor division of 15 by 4 = 3
    """

If a value used to perform the double slash // is a negative number, the result would still be rounded down.

Take in consideration, that given the result of a division between a positive number and a negative would result in a negative value, and remember that a number is "smaller" as it gets further away from zero, a "bigger" negative number is actually "smaller" (-40 < -3).

    numberOne = -12
    numberTwo = 5
    numberThree = numberOne // numberTwo
    
    print("Floor division of", numberOne, "by", numberTwo, "=", numberThree)
    # Output: floor division of -12 by 5 = -4
    

## What’s the difference between // and Math.floor():What’s the difference between // and Math.floor():

In Python, as in many other programming languages, we can find Math.floor(), which rounds down a float number to the nearest integer, it doesn´t matter if it´s a positive or negative value.

As they both share this behavior, you could think that they are alternative of one-another but remember the double slash `//` operator does a division before rounding the value. Here is an example for achieving a whole number (integer) from a division with `Math.floor()` and the same example with the double slash `//` operator.

    numberOne = 100
    numberTwo = 45
    numberThree = numberOne // numberTwo
    
    print("Floor division of", numberOne, "by", numberTwo, "=", numberThree)
    # Output: floor division of 100 by 45 = 2
    
    numberFour = numberOne / numberTwo
    numberFive = Math.floor(numberFour)
    
    print("Division of", numberOne, "by", numberTwo, "=", numberFour)
    # Output: floor division of 100 by 45 = 2,22222222
    print("Applying Math.floor() to round to nearest integer. Math.floor(", numberFour, ")=", numberFive)
    # Output: Applying Math.floor() to round to nearest integer. Math.floor(2.22222)= 2
    

As you can see, in both cases we arrived to the same conclusion, but the double slash operator `//` makes it in a more direct way and is most resource effective and time friendly.

Now that we know what does `//` mean in python, it´s time to understand how it works under the hood.

## The double slash Operator // under the hoodThe double slash Operator // under the hood

When we implement the double slash operator `//` with 2 numbers, the method that gets summoned under the hood is no other than: `__floordiv__()` and since we know now what is called, we can use it instead of the double slash if we want to.

    numberOne = 10
    numberTwo = 3
    numberThree = numberOne.__floordiv__(numberTwo)
    
    print("Floor division of", numberOne, "by", numberTwo, "=", numberThree)
    # Output: floor division of 10 by 3 = 3

## Conclusion

In the present article we discussed what does `//` mean in Python, the operator syntax, how to use it and how it works under the hood. 
As well, we made a comparison between `Math.floor()` and how to achieve the same result using this alternative and calling directly the` __floordivision__()` method.

The path, in which one to use, is yours to take although I would strongly recommend using the double slash operator since is easier and there´s less typing involved.

Thanks for reading and keep it Geek!

