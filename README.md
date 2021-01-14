# PHP-Syntax-Guide

## Today I will be describing a variety of basic functions that you will frequently come across when using PHP.

### PHP Comments

In PHP a comment is a line of code that will not be executed. It allows the programmer to enter in comments to describe various aspects, or make notes without affecting the functionality of the code.

This can be done in a variety of ways the first and most common is by entering two forward slashes like so "//" everything after on a single line will be a comment.

If you would like to make a multi line comment you will begin it with a forward slash then an asterisks and end it with an asterisks then a forward slash "/* */

```sh
<?php

//This is a single line comment and will not affect the code.

/*This comment
has many
lines
but still won't affect the code*/
?>
``` 

### PHP Variables

Variables are used in almost all forms of code, a variable is a way of storing or holding information to use throughout the code, we will later show a variety of different variable types however creating a variable is one of the first fundamentals you need to know. 

In PHP a variable has some rules when it comes to naming. It must begin with a dollar sign "$" and then the following character must be an underscore "_" or a letter. Variables must use only alpha-numeric characters or underscores, but they cannot start with a number. Variables are also case sensitive. 

After you decide the name of your variable you will use a single space, an equals sign "=" and then another single space. After that you will enter in the information you want held inside the variable. You will end the line with a semicolon.

Below I will show three different variables. 

```sh
<?php

$farFreezeTemp = 32;
$celBoilTemp = 100;
$txt = "The quotes means this whole sentence is in the variable.";

?>
```

### PHP Echo/Print

Echo and Print are both functions that output content to a screen this can be blocks of text in quotes, or variables which will be shown below. The differences between Echo and Print are slight. Echo is a bit faster and can take multiple parameters, where as Print cannont. You can put together many forms of data in one echo or print statement by seperating them with a space, then a period, then another space " . " . 

The echo statement below will output "Hello my name is SalmonBrawl and I hope this lesson in PHP is helpful."

The print statement below will output "Hello my name is Tony Bologna and I hope this meatball sub gets you through the tough times."

```sh
<?php

$nameOne = "SalmonBrawl";
$nameTwo = "Tony Bologna";
$nameOneHelp = "lesson in PHP is helpful.";
$nameTwoHelp = "meatball sub gets you through the tough times.";

echo "Hello my name is " . $nameOne . " and I hope this " . $nameOneHelp;

print "Hello my name is " . $nameTwo . " and I hope this " . $nameTwoHelp;

?>
```

### PHP Data Types

In PHP there is a variety of Data Types that can be used or stored into variables. Here I will give a brief description of each and then after we will dive in to some of them with a bit more depth.

#### Strings

Strings are sets of characters that are placed inside double or single quotes like so "Hey I am a string" or 'guess what buddy? I am a string too.'

#### Intergers

An interger is a number that has no decimal point -2,147,483,648 and 2,147,483,647. It can be positive or negative.

#### Float

A float is any number with a decimal point.

#### Boolean

A Boolean is a representation of either true or false, nothing else.

#### Array

Arrays are variables that can store multiple different values.

#### Objects

An object at it's root is an amalgam of different properties pertaining to a specific item. Like a specific recipe. So if I had a recipe for sticky ribs, the recipe would be the class, the object would be the sticky ribs and the properties would be the ingredients. The properties describe what the object is.

#### NULL

Null is the absence of any form of value in a variable which in itself is a value.

### PHP Strings

As previously mentioned a string is a set of characters set between single or double quotes. Be careful not to add an apostrophe if you are using a single quote.

```sh
<?php

$stringOne = "Howdy Partnah";
$stringTwo = 'This town inna biganuff for da bof of us!';

?>
```

### PHP Numbers

As mentioned before numbers can be displayed as either intergers or floats. The difference is in the decimal.

```sh
<?php

$posNum = 500;
$negNum = -500;
$float = 2.482;

?>
```

### Constants

Constants are similar to variables however they are globally scoped, they are created with the define() function which takes two or three parameters. The first is the name of the constant in quotation marks, it must start with a letter or an underscore. The next paramater is the data inside. The third parameter is whether or not it is case-insensitive. The default is false so if you leave it blank then the constant will be case sensitive but if set to true will enable case insensitivity.

The first echo statement will display "I am a garden of joy"

The second echo statement will display "Water me with love and affection"

```sh
<?php

define("identity", "I am a garden of joy");
define("HoWtOcArEfOr", "Water me with love and affection", true);

echo identity;
echo howToCareFor;
?>
```

### Operators 

There are a variety of different types of operators that can be used. I will give a brief overview of the different styles however you should probably just check out [this](https://www.w3schools.com/php/php_operators.asp) page for all of the examples.

#### Arithmetic Operators 

Arihmetic Operators are Operators that perform common calculations on number variables. These include addition, subtraction, multiplication, division, modulus and exponentian. Anything a standard calculator can do.

#### Assignment Operators 

Assignment operators uses the equals sign together with the arithmetic operators to easily change the value of a variable. The syntax is changing variable, arithmetic operator, equals sign, math variable. For example x += y is the same as saying x = x + y.

#### Comparison Operators

Comparison operators are used to compare two variables to see their relation to one another. Be it greater than, less than, equal to, identical, not equal, or not identical they are the operators that are used to solidify a relationship. The chart can be found [here](https://www.w3schools.com/php/php_operators.asp)

#### Increment Operators

These operators are used to increment or decrement a variables value.

#### Logical Operators

Logical operators are used to combine conditions. These operators are and, or, xor, &&, ||, and !(not).

#### String Operators

As you saw earlier when we were putting together echo statments with " . " the period is a string operator to concatonate the strings. There is also ".=" which appends the second string to the first.

#### Array Operators

Array operators are used to compare arrays be it by union of arrays, checking equality between arrays, or finding discrepencies, these operators are used to compare array contents.

#### Conditional Operators

Conditional operators are used to assign values based on conditions. These are Ternary and NULL coelescing.

### PHP if-else-elseif

If-Else-Elseif statements are used to tell a function to operate during certain conditions. For example if the temperature is cold I want it to tell me to bring a coat. If it's hot I want it to tell me to bring sunscreen, however if its mild I will probably be fine in whatever I'm wearing.

In the example below it would tell me to bring sunscreen.

```sh
<?php

$tempInCel = 30;

if ($tempInCel < 12) {
echo "Bring a coat, it is a bit cold";
} elseif ($tempInCel <26) {
echo "Weather seems alright.";
} else {
echo "It is hot, do not forget your sunscreen";
}
?>
```


### PHP Functions

A function is a grouping of code that can be used multiple times in a variety of places in your code, functions have to be defined (unless they are one of the many predefined PHP functions) and then they have to be called to be utilised. They are defined by entering function, then a space, then your function name with an open and close parenthesis. The code will then sit in between two curly brackets. The function will be called by entering yourfunction(). The function can also have a multitude of parameters that are input into it when called yourfunction(parone, partwo, parthree)

```sh
<?php

function introduction() {
echo "This is a basic function to introduce me, SalmonBrawl";
}

introduction();
?>
```

### PHP Arrays

Arrays are variables that can hold a multitude of different values. Arrays are created by calling the array() function and then inputting the data that you want inside said array.

There are also different types of arrays. Indexed arrays have a numeric index, associated arrays are named with keys, and multidimensional arrays are arrays inside arrays.

For example I'll make a simple array called food with some of my favourite foods within.

```sh
<?php

$food = array("Pesto Pasta", "Chicken Wings", "Burgers", "Salmon", "Tacos")
```

### PHP Loops

PHP loops are functions that will run multiple times as long as the condition remains true, or it has not completed the specified amount of iterations. The different types of loop functions are while loops, which run as long as a certain condition stays true. Do...while, runs the code and then continues to run it as long as the certain condition stays true. For loops allow you to choose a certain amount of iterations and foreach loops will perform the code for each aspect of an array.

Below I will show a basic for loop that will count to five.

```sh
<?php
for ($x = 0; $x <= 5; $x++) {
  echo "$x";
}
?>
```


