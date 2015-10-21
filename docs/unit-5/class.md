# Object Oriented Programming

## How To Create Objects.

### To make a Cake you need a mould, To make Objects You need Class
![Template](images/cake_mould.jpg)

1. How many ever cakes can be produced from the same mould. Similarly anynumber of objects can be made from the class.

2. Cakes will be have same properties like `size, shape, weight` Similary Objects will have the same properties of the class.

### Class

A Class has

1. Properties or Attributes 

    Which describes/defines something or some aspect about the Class like `color`,
`measurement`.

2. Methods / Member functions

    Which describes or holds the instructions of a specific operation about the class.

### Creating Class

```
<?php
    class Car{

    //Properties
    var    $color = 'green';
    var    $price = 1000000 ;
    var    $brand = 'Honda City';

        //Methods
        function drive(){
            echo 'driving...';
        }
    }

    //Creating Object mycar New keyword is mandate
    $mycar = new Car;

    // Class Name with () and without () both are same.
    $yourcar = new Car();
?>
```

### Constants in class can be defined using `const` not `define`

1. It is possible to define constant values on a per-class basis remaining the same and unchangeable. 

2. Constants differ from normal variables in that you don't use the **$** symbol to declare or use them.

3. The value must be a constant expression, not (for example) a variable, a property, or a function call.

4. It's also possible for interfaces to have constants. Look at the interface documentation for examples.



```
define('MIN_VALUE', '0.0');   // RIGHT - Works OUTSIDE of a class definition.
define('MAX_VALUE', '1.0');   // RIGHT - Works OUTSIDE of a class definition.

//const MIN_VALUE = 0.0;         WRONG - Works INSIDE of a class definition.
//const MAX_VALUE = 1.0;         WRONG - Works INSIDE of a class definition.

class Constants
{
  //define('MIN_VALUE', '0.0');  WRONG - Works OUTSIDE of a class definition.
  //define('MAX_VALUE', '1.0');  WRONG - Works OUTSIDE of a class definition.

  const MIN_VALUE = 0.0;      // RIGHT - Works INSIDE of a class definition.
  const MAX_VALUE = 1.0;      // RIGHT - Works INSIDE of a class definition.

  const SEC_PER_DAY = 60 * 60 * 24; // as of PHP 5.6 expressions allowed.
  public static function getMinValue()
  {
    return self::MIN_VALUE;
  }
}
```

### Example of Class with Constant and different ways it can be accessed

```
<?php
class MyClass
{
    const CONSTANT = 'constant value';

    function showConstant() {
        echo  self::CONSTANT . "\n";
    }
}

echo MyClass::CONSTANT . "\n";

$classname = "MyClass";
echo $classname::CONSTANT . "\n"; // As of PHP 5.3.0

$class = new MyClass();
$class->showConstant();

echo $class::CONSTANT."\n"; // As of PHP 5.3.0
?>
```