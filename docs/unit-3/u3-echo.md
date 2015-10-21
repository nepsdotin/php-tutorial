# Displaying Content in PHP

## Echo
`void echo ( string $arg1 [, string $... ] )` 

echo is not actually a function (it is a language construct), so you are not required to use parentheses with it.

All the following are valid
```
<?php
echo "Hello World";

echo "This spans
multiple lines. The newlines will be
output as well";

echo "This spans\nmultiple lines. The newlines will be\noutput as well.";

echo "Escaping characters is done \"Like this\".";

// You can use variables inside of an echo statement
$foo = "foobar";
$bar = "barbaz";

echo "foo is $foo"; // foo is foobar

// You can also use arrays
$baz = array("value" => "foo");

echo "this is {$baz['value']} !"; // this is foo !

// Using single quotes will print the variable name, not the value
echo 'foo is $foo'; // foo is $foo

// If you are not using any other characters, you can just echo variables
echo $foo;          // foobar
echo $foo,$bar;     // foobarbarbaz

// Some people prefer passing multiple parameters to echo over concatenation.
echo 'This ', 'string ', 'was ', 'made ', 'with multiple parameters.', chr(10);
echo 'This ' . 'string ' . 'was ' . 'made ' . 'with concatenation.' . "\n";

echo <<<END
This uses the "here document" syntax to output
multiple lines with $variable interpolation. Note
that the here document terminator must appear on a
line with just a semicolon. no extra whitespace!
END;

// Because echo does not behave like a function, the following code is invalid.
($some_var) ? echo 'true' : echo 'false';

// However, the following examples will work:
($some_var) ? print 'true' : print 'false'; // print is also a construct, but
                                            // it behaves like a function, so
                                            // it may be used in this context.
echo $some_var ? 'true': 'false'; // changing the statement around
?>
```

## Print
print — Output a string
```
int print ( string $arg )
```

print is not actually a real function (it is a language construct) so you are not required to use parentheses with its argument list. 


## Print_r
print_r — Prints human-readable information about a variable
```
mixed print_r ( mixed $expression [, bool $return = false ] )
```
##### expression
The expression to be printed.

##### return
If you would like to capture the output of print_r(), use the return parameter. When this parameter is set to TRUE, print_r() will return the information rather than print it.

## Var_dump
Same as print_r() but display along with the data types

```
void var_dump ( mixed $expression [, mixed $... ] )
```

## heredoc
 A third way to delimit strings is the heredoc syntax: <<<. After this operator, an identifier is provided, then a newline. The string itself follows, and then the same identifier again to close the quotation.

The closing identifier must begin in the first column of the line.
```
<?php
echo <<<HELLO
This is a long string A third way to delimit strings is the heredoc syntax: <<<. After this operator, an identifier is provided, then a newline. The string itself follows, and then the same identifier again to close the quotation.
HELLO
?>
```

## nowdoc
A nowdoc is identified with the same <<< sequence used for heredocs, but the identifier which follows is enclosed in single quotes, e.g. <<<'EOT'. All the rules for heredoc identifiers also apply to nowdoc identifiers, especially those regarding the appearance of the closing identifier.

```
<?php
$name = 'Rangarajan';

echo <<<'HELLO'
Hello $name, This is a long string A third way to delimit strings is the heredoc syntax: <<<. After this operator, an identifier is provided, then a newline. The string itself follows, and then the same identifier again to close the quotation.
HELLO
?>
```
