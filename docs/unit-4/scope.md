# Variable Scope
The scope of a variable is the context within which it is defined, and its value is available.

## Global Scope
Any variable defined will be having 

1. a global scope in the file it is defined.
2. and in the file included via `include(), require(), include_once(), require_once() `
    

```php
<?php
#tea.php
$v = 100;

include 'sugar.php';

?>
```


```php
<?php
#sugar.php

// Output wil be 100
echo $v
?>
```
## Function Scope

1. Any variable defined inside the function are available only within the function where it defined. 
2. Variable defined **outside the function will NOT be available** within the function scope.

```php
<?php

$person = 'Ramkumar';

sayHelloTo();

function sayHelloTo(){
    echo "Hello !" . $person;
}

?>
```

To use the globally scoped variable you need to use `global` keyword in the function where you wanted to use the variable.

```php
<?php

$person = 'Ramkumar';

sayHelloTo();

function sayHelloTo(){
    //Note I am redclaring the same variable inside the function but now
    //with global keyword before variable $person.
    global $person;

    // output Hello ! Ramkumar
    echo "Hello !" . $person;
}

?>
```

## Static Variable

1. A static variable exists only in a local function scope, 
2. but it does not lose its value when program execution leaves this scope.

Consider the following example: 

```
// Lets make 10 Omlets using Static variable
<?php
exampleStatic( 10 );
exampleStatic( 10 );

function exampleStatic( $a ){
    static $i = 0;
    $i++;
    echo $i;
}

?>
```

