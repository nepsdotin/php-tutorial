# PHP 1.0

# Those days Web was 

### Static Pages
### Form To collect User Data
### Signin - UserSpace - Signout

# How PHP was cooked ?

### Rasmus Lerdorf - Proud Creator of PHP
![](images/rasmus.jpg)

1. Follow: [Rasmus](http://twitter.com/rasmus)
2. Blog:   [https://toys.lerdorf.com/](https://toys.lerdorf.com/)
Rasmus Lerdorf was a web developer

[First Post of Rasmus](https://goo.gl/Lf2bGR)

# PHP FI (PHP Form Interpreter) - PHP Ver 2.0

Sample of PHP FI 2.0

```
<html>
<head>
    <title>Welcome To PHP FI 2.0</title>
</head>
<body>
    <form action="process.phtml" method="POST">
        Name:<input type="text" name="username">
        Age:<input type="text" name="age">
    </form>
    <? if($name): ?>
    Hi, <?echo $name; ?>
    <?endif?>
</body>
</html>
```
[http://museum.php.net/](http://museum.php.net/)
# What can PHP be used for ?

## Build Commandline Scripts to do some tiny little job as tiny as

1. delete few files
2. copy a bunch of files
3. CRON Jobs

### Executing a File (Ex.1)
#### Syntax
```
php -f filename.php
```
#### unit-3-ex-1.php
```
<?php
/* unit-3-ex-1.php */
echo "<h1>Hello World</h1>";
?>
```
To run this program

```
php -f unit-3-ex-1.php
```
### Interactive Shell / Mode (Ex.2)

### Interactive Shell

1. You can execute one command at a time
2. Does tab completion for functions, constants, class names, variables, static method calls and class constants.

#### Syntax : `php -a`

```
# Should be the prompt
Interactive Shell
php > 
```

```
php > strp[TAB][TAB]
strpbrk   strpos    strptime  
php > strp
```

### Interactive Mode

1. `php -a` is the same syntax as you use it for interactive shell. 
2. Interactive mode is essentially like running php with what the user types as the file input. 
3. You just type code, and when you're done (Ctrl-D), php executes whatever you typed as if it were a normal PHP file. 
4. You start in interactive mode with `'<?php'` in order to execute code.

### Various Options 
```
php --help
XCache requires Zend Engine API version 220100525.
The Zend Engine API version 220090626 which is installed, is outdated.

Usage: php [options] [-f] <file> [--] [args...]
       php [options] -r <code> [--] [args...]
       php [options] [-B <begin_code>] -R <code> [-E <end_code>] [--] [args...]
       php [options] [-B <begin_code>] -F <file> [-E <end_code>] [--] [args...]
       php [options] -- [args...]
       php [options] -a

  -a               Run as interactive shell
  -c <path>|<file> Look for php.ini file in this directory
  -n               No php.ini file will be used
  -d foo[=bar]     Define INI entry foo with value 'bar'
  -e               Generate extended information for debugger/profiler
  -f <file>        Parse and execute <file>.
  -h               This help
  -i               PHP information
  -l               Syntax check only (lint)
  -m               Show compiled in modules
  -r <code>        Run PHP <code> without using script tags <?..?>
  -B <begin_code>  Run PHP <begin_code> before processing input lines
  -R <code>        Run PHP <code> for every input line
  -F <file>        Parse and execute <file> for every input line
  -E <end_code>    Run PHP <end_code> after processing all input lines
  -H               Hide any passed arguments from external tools.
  -s               Output HTML syntax highlighted source.
  -v               Version number
  -w               Output source with stripped comments and whitespace.
  -z <file>        Load Zend extension <file>.

  args...          Arguments passed to script. Use -- args when first argument
                   starts with - or script is read from stdin

  --ini            Show configuration file names

  --rf <name>      Show information about function <name>.
  --rc <name>      Show information about class <name>.
  --re <name>      Show information about extension <name>.
  --ri <name>      Show configuration for extension <name>.

```

### Lets Try (Ex.3)

```
php -i
php -v
php -m
php --ini
```

## Build Static / Dynamic Websites / web apps

1. as tiny as few couple of pages like leaderboard.
2. as large as Facebook, Yahoo!

## Few Popular Web Applications

1. Wordpress - Blog
2. PHPbb - discussion forum
3. joomla - CMS
4. elgg - social networking engine
5. sugarcrm - Customer Relationship Management
6. etc..

### Can you name some websites / web apps that are built using php ?
