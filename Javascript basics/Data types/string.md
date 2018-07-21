# Quotes

## Simple Quotes
    Single quotes('') and double quotes("").
## Double Quotes
    Backticks(``). Backticks are used to let strings span multiple lines(replace the use of \n in simple quotes) and to contain expressions.
# Special Characters
## Newline(\n)
    Newline is used to divide a string into multiple lines.
    Example: 
```js
    console.log("Hello\n world!");
```
    Output:
```
     Hello
     world!
```

## Backslash(\\) or "The Escape Character"
    Backslash is used to insert quotes or backslash itself into a string.
    Example: 
```js    
    console.log('I\'m a writer.')
```
    Output:
```
     I'm a writer.  
```
    Otherwise the output would be: 
```
    I
```

    Another solution is to change the enclosing quotes and make the one you are gonna insert different from the enclosing ones.
    Example: 
```js
    console.log("I'm a writer.")
```
    Output: 
```
    I'm a writer.
```
## Others including "\b" "\t"...
# String Length

## Use str.length to get the length of the string, NOT str.length().

# Accessing Characters
## Use str[pos] or str.charAt(pos).
Difference: when the pos is greater than string's actual length, **str[pos]** would return **undefined** while **str.charAt(pos)** would return **''(an empty string)**.

# Change Case
## Use str.toUpperCase() or str.toLowerCase().

# Search For A SubString
## str.indexOf(subStr, startPos)    
Example:
```js
    let str = "Widget with id";
    alert(str.indexOf("Widget"));
```
Output:
```js
    0 // because "Widget" starts from pos 0
```
## str.lastIndexOf(subStr,pos)
same usage as str.indexOf().
## bitwise NOT ~ operator
   ~n means -(n + 1)
### Can be used to indicate whether the subStr is found
remember than if(~str.indexOf(...)) reads as "if found".
## str.includes(subStr),str.startsWith(subStr) or str.endsWith(subStr) 
if you don't want to get the exact position, use these since they simply return true or false.

# Get A Substring
## str.slice(start,end)
Example:
```js
    let str = "This is the case.";
    console.log(str.slice(0,2));
```
Output:
```js
    Th //left inclusive, right exclusive.
```
negative position values can be used.
### Example:
```js
    console.log(str.slice(-3,-1));
```
Output:
```js
    se //last position is -1.
```

## str.substring(start,end)
Example:
```js
    console.log(str.substring(0,3));
    console.log(str.substring(3,0)); //it allows the start to be greater then end.
```
Output:
```js
    Thi
    Thi
```
negative values are not supported and are treated as 0.

## str.substr(start,length)
Example:
```js
    console.log(str.substr(0,3));
```
```js
    Thi
```
the first argument can be negative, to count the starting position from the end
### Example:
```js
    console.log(str.substr(-2,2));
```
Output:
```js
    e.
```
