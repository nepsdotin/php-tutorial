# Self & this Special Variables

## Self

To refer a property at class level `self` is used.
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

$class = new MyClass();
$class->showConstant();

echo $class::CONSTANT."\n"; // As of PHP 5.3.0
?>
```

## this

To refer a property at object level `this` is used.

```
<?php
class Car
{
    var $color = 'blue';

    function drive() {
       echo 'Computer is driving the car with the color :' . $this->color;
    }
}

$obj = new Car();
$obj->drive();

?>
```

## static

Declaring class properties or methods as static makes them accessible without needing an instantiation of the class

### Static Method
```
<?php
class Foo {
    public static function aStaticMethod() {
        // ...
    }
}

Foo::aStaticMethod();
$classname = 'Foo';
$classname::aStaticMethod(); // As of PHP 5.3.0
?>
```

### Static Properties
Like any other PHP static variable, static properties may only be initialized using a literal or constant before PHP 5.6; expressions are not allowed. 

```
<?php
class Foo
{
    public static $my_static = 'foo';

    public function staticValue() {
        return self::$my_static;
    }
}

print Foo::$my_static . "\n";

$foo = new Foo();
print $foo->staticValue() . "\n";
print $foo->my_static . "\n";      // Undefined "Property" my_static 

?>
```