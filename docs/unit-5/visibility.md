# Visibility

### Public 
Class members declared public can be accessed everywhere.
### Protected
Members declared protected can be accessed only within the class itself and by inherited classes.
### Private
Members declared as private may only be accessed by the class that defines the member.

####Note

** variables & functions are public by default **

By default If declared using var, the property will be defined as public. Contrary to the OOPS Pradigms of **Data Hiding**

By default if declared without using `visibility` its declared as `public` function. This is in accordance with OOPS Pradigms `methods are always public`

#### Example:

```php
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

        //Method, by default its public
        function drive(){
            // Accisible only within the class function's code.
            echo 'Engine : ' . $this->engine;
            echo 'driving...';
        }

        // Private method to apply Airbag when accidents happen.
        private function openAirBag(){
            echo 'Openning Airbag for Emergency....';
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

    // Fails
    //echo $car_obj->engine;

    // public prop
    echo 'Color : ' . $car_obj->color;
    echo 'Price : ' . $car_obj->price;

?>
```

