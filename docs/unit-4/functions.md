# Functions 

## 1. Builtin Functions
There are multitudes of functions easy to use for our application development. They can help us to process data

1. String Processing
2. Array Processing

## 2. User Defined Functions

### Syntax

```
function functionName( parameter1, parameter2,...., param_n ){
    /* Any valid php code goes here */
    function_body

    return return_value;
}
```

Functions need not be defined before they are referenced.

### Valid function
```
// The function can be called before the function is defined.
hello();

function hello(){
    
}

// 
```

### Functions within Functions
```
<?php
function makeOmlet(){
    
    echo "Making Omlet";
    function makebreadOmlet(){
        echo "Making Breadomlet";
    }
}

// We can't call makebreadOmlet() till we make omlet
makeOmlet();

makebreadOmlet();

// Trying to call first makebreadOmlet() before calling makeOmlet() won't work.
?>
```

### Recursive Functions
```
// Lets make 10 Omlets
<?php
makeOmlet( 10 );

function makeOmlet( $a ){
    if( $a > 1){
        echo " </br> Making Omlet " . $a;
        makeOmlet( $a - 1 );
    }
}
?>
```

## Function Arguments
 Information may be passed to functions via the argument list, which is a comma-delimited list of expressions. The arguments are evaluated from left to right.

 ### Default Arguments

```
// Let's make a Tea
function makeTea( $type ='lime' ){
    echo "I ll be making " . $type . " Tea in a Min.";
}
```

#### What is the output of the following code
```
function makeyogurt($type = "acidophilus", $flavour)
{
    return "Making a bowl of $type $flavour.\n";
}
 
echo makeyogurt("raspberry");
```
# Important To Note
1. By default, function arguments are **passed by value** (so that if the value of the argument within the function is changed, it does not get changed outside of the function).
2.  **prepend an ampersand (&)** to the argument name in the **function definition**.
3. Don't Need to **prepend an ampersand (&)** when you **call** the function.Try it! You may get error

# Tips

1. PHP does not support function overloading, nor is it possible to undefine or redefine previously-declared functions.

2. Function names are case-insensitive, though it is usually good form to call functions as they appear in their declaration.

3. all array functions ($needle, $haystack). Eg. `in_array($needle, $haystack)`

4. all string functions ($haystack, $needle). Eg. `strstr($haystack, $needle)`

