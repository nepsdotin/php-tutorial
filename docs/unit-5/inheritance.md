# Inheritance

1. A class can inherit the methods and properties of another class by using the keyword `extends` in the class declaration. 
2. It is not possible to extend multiple classes; a class can only inherit from one base class. 
3. The inherited methods and properties can be overridden by redeclaring them with the same name defined in the parent class.  However, if the parent class has defined a method as final, that method may not be overridden. It is possible to access the overridden methods or static properties by referencing them with parent::.

```
<?php
    class Car{

        //Properties, by default its public
        var $color = 'green';
        // You can declare public prop. like this also
        public  $price  = 1000000;

        // Private
        private $engine = 'blah blah';

        // Protected available to Car Class, and all Sub Classes.
        protected $no_of_wheels = 4 ;

        //Methods
        function drive(){
            
            echo 'driving...';
        }
    }

    class TeslaCar extends Car {

        //Prop has $color, $price, $brand along with manufacturer
        public $manufacturer = 'Elon Musk';

        //Methods has drive() and selfdrive()
        function selfdrive(){
            echo 'Self driving is also available along with driving';
        }
        
    }

    $car_obj = new Car;

    $my_tesla = new TeslaCar();

    // Inherited method is available for the Teslacar
    $my_tesla->drive();

    // Extended or new method for the Tesla Car.
    $my_tesla->selfdrive();

    // public prop
    echo 'Color : ' . $car_obj->color;
    echo 'Price : ' . $car_obj->price;

?>
```

## Method / Function Overriding

```php
<?php
    class Car{

        //Properties, by default its public
        var $color = 'green';

        // Private
        private $engine = 'blah blah';

        // You can declare public prop. like this also
        public  $price  = 1000000;

        // Protected available to Car Class, and all Sub Classes.
        protected $no_of_wheels = 4 ;

        //Methods - public by default
        function drive(){
            // Accisible only within the class function's code.
            echo 'Engine : ' . $engine;
            echo 'driving...';
        }
    }

    class TeslaCar extends Car {

        //Prop has $color, $price, $brand along with manufacturer
        public $manufacturer = 'Elon Musk';

        // The default behaviour drive is being overridden / modified in the subclas
        function drive(){
            echo "Self Checking System.. Power ON <br>";
            echo "Starting Audio <br>";
            echo "driving...";
        }

        //Methods has drive() and selfdrive()
        function selfdrive(){
            echo 'Self driving is also available along with drive method';
        }
    }
?>

```