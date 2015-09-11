# Arrays in PHP

An array in PHP is actually an ordered map. A map is a type that associates values to keys. This type is optimized for several different uses; it can be treated as an array, list (vector), hash table (an implementation of a map).

### Example of Array

```
<?php
$array = array(
    "foo" => "bar",
    "bar" => "foo",
);
```

### as of PHP 5.4
```
// as of PHP 5.4
$array = [
    "foo" => "bar",
    "bar" => "foo",
];
?>
```

The key can either be an integer or a string. The value can be of any type.

### is this valid ?
```
$array = array(
    "foo" => "bar",
    "bar" => "foo",
    100   => -100,
    -100  => 100,
);
```

### Indexed array
```
<?php
$array = array("foo", "bar", "hello", "world");
var_dump($array);
?>
```

### MultiDimensional array
```
<?php
$array = array(
    "foo" => "bar",
    42    => 24,
    "multi" => array(
         "dimensional" => array(
             "array" => "foo"
         )
    )
);

var_dump($array["foo"]);
var_dump($array[42]);
var_dump($array["multi"]["dimensional"]["array"]);
?>
```

### Array dereferencing
```
<?php
function getArray() {
    return array(1, 2, 3);
}

// on PHP 5.4
$secondElement = getArray()[1];

// previously
$tmp = getArray();
$secondElement = $tmp[1];

// or
list(, $secondElement) = getArray();
?>
```

## Array Functions 
[http://php.net/manual/en/ref.array.php](http://php.net/manual/en/ref.array.php)

bool in_array ( mixed $needle , array $haystack [, bool $strict = FALSE ] )

