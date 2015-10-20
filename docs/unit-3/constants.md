# Constants in PHP

## User Defined Constants

```
define('LABEL', 'Actual Value')
```

## Magic Constants
| Const       |  The magic it has                                             |
------------- |:-------------------------------------------------------------:|
| `__LINE__`  | The current line number of the file.                          |
| `__FILE__`  | The full path and filename of the file with symlinks resolved |
| `__DIR__`   | The directory of the file. equivalent to `dirname(__FILE__)`.   |
| `__FUNCTION__` | The function name. |
| `__CLASS__` |The class name. The class name includes the namespace it was declared in (e.g. Foo\Bar). 
| `__TRAIT__` | The trait name. The trait name includes the namespace it was declared in (e.g. Foo\Bar). 
| `__METHOD__`  | The class method name. 
| `__NAMESPACE__` | The name of the current namespace. |


**Note** :This directory name does not have a trailing slash unless it is the root directory. 
