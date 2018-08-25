### Valid Number

Validate if a given string is numeric.

#### Some examples:
- "0" => true
- " 0.1 " => true
- "abc" => false
- "1 a" => false
- "2e10" => true

#### Note: 
It is intended for the problem statement to be ambiguous. You should gather all requirements up front before implementing one.

##### JavaScript

```JavaScript

/**
 * @param {string} s
 * @return {boolean}
 */
var isNumber = function(s) {
        return s.trim().length === 0 ? false : !isNaN(+s);

};
```

##### PHP

```PHP
<?php
        //Enter your code here, enjoy!

var_dump(is_numeric(trim("0")));
var_dump(is_numeric(trim(" 0.1 ")));
var_dump(is_numeric(trim("abc")));
var_dump(is_numeric(trim("1 a")));
var_dump(is_numeric(trim("2e10")));
```