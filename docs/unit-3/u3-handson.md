# Lets Do Something

### Building First Web Page in PHP

#### Ways to Create PHP Scripts
1. All PHP code should be place only in
    1.1 `(.php, .php3, .php4, php5, .phtml)` typically in `.php` file for simplicity and convention.

2. In PHP file you php code should always be enclosed inside one of the tag
    1.  `<?php ?>`  ( Generally used ) or
    2.  `<?=   ?>`  ( Rarely used, and its called shorttags )or
    3.  `<%    %> ` ( ASP Style Tag, Not generally used, need asp_tags enabled in php.ini)  

##### Note

1. Since PHP Ver. 7.0.0  The ASP tags `<%, %>, <%=,` and the script tag 
`<script language="php">` are removed from PHP.

2. Since PHP Ver 5.4.0 The tag <?= is always available regardless of the short_open_tag ini setting. Prior to 5.4.0 Developer should explicitly do this setting in php.ini `short_open_tag = On`

## Leaderboard 
### Print an ASSOC. ARRAY as a Table / ASCII Table
```
$leaders = array(
    array( 
        'rank' => 1,
        'name' => 'Raj',
        'score' => 100,
    ),
    array( 
        'rank' => 2,
        'name' => 'Kumari',
        'score' => 98,
    ),
    array( 
        'rank' => 3,
        'name' => 'Rangan',
        'score' => 92,
    ),
    array( 
        'rank' => 4,
        'name' => 'Priyanka',
        'score' => 90,
    ),
)

Display them as a Table
+------------+-------+---------+
| Rank       | Name  | Score   |
+------------+-------+---------+
| 1          | Raj   | 100     |
| 2          | Kumari| 98      |
| 3          | Rangan| 92      |
| 4          | Priyanka| 90    |
+------------+-------+---------+
```
