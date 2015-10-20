# Useful ini Settings

All PHP Configurations are Stored in a file called `php.ini`

The configuration file (php.ini) is read when PHP starts up. For the server module versions of PHP, this happens only once when the web server is started. For the CGI and CLI versions, it happens on every invocation.

## 1. display_errors
`display_errors = boolean`

This determines whether errors should be printed to the screen as part of the output or if they should be hidden from the user.

Eg.: To enable `display_errors` we can use one of the following.

1. `display_errors = On` 
3. `display_errors = true`
4. `display_errors = 1` 

**Note:** This is a feature to support your development and should never be used on production systems.

## 2. log_errors
`log_errors = boolean`

Tells whether script error messages should be logged to the error_log

## 3. error_log
`error_log = string`

Name of the file where script errors should be logged. The file should be writable by the web server's user. 

Eg. `error_log = '/var/log/php_errors.log'`

To view error log `less /var/log/php_errors.log`

To do live debugging 

`tail -f /var/log/php_errors.log` To stop `Cntrl + C`

`-f` Option keeps reading for the upcoming inputs. Hence you will see the error as it pops on the `php_errors.log`




