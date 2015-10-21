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

Common use is as follows 

### config.php

We Store the config details once in `config.php` and include it whenever we want. In our example we are including in `userdetails.php`

Since PHP provides **global** scope to the included files we enjoy these kinds of patterns.

```php
<?php
//config.php

// We declare the db config info in config.php and whenever we require that
// we include and the values can be accessed in the file it is included.
$db_host = 'localhost';
$db_name = 'students_db';
$db_username = 'prem';
$db_password = 'prem';


?>
```
### userdetails.php
```php
<?php
//Userdetails.php

include 'config.php';

//can use $db_host, $db_username, $db_password 
//Very useful usecase is possible because of the global scope.
$link = mysql_connect( $db_host, $db_username, $db_password )

if( !$link ){
    die('Could not connect: ' . mysql_error());
}

echo 'Connected successfully';
mysql_close($link);
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

