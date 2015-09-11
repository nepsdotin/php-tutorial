# PHP Data Types

## PHP supports eight primitive types.

## Four scalar types:

#### boolean
$a_bool = TRUE;   // a boolean
$a_bool = true;   // a boolean

#### integer
$an_int = 12;     // an integer

#### float (floating-point number, aka double)

#### string
```
$a_str  = "foo";  // a string
$a_str2 = 'foo';  // a string
```
## Two compound types:

#### array
#### object

## And finally two special types:

1. resource
2. NULL

## Find What type

```
echo gettype($a_bool); // prints out:  boolean
echo gettype($a_str);  // prints out:  string

// If this is an integer, increment it by four
if (is_int($an_int)) {
    $an_int += 4;
}

// If $a_bool is a string, print it out
// (does not print out anything)
if (is_string($a_bool)) {
    echo "String: $a_bool";
}
```

## last but not least PHP is loosely typed language.
