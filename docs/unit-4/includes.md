# includes, requires

require is identical to include except upon failure it will also produce a fatal E_COMPILE_ERROR level error. In other words, it will halt the script whereas include only emits a warning (E_WARNING) which allows the script to continue. 

**Note:** 
require is not a function is a statement

`require 'somefile.php';` is better `require('somefile.php');`

