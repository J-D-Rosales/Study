# How the + operator concatenates strings?
if the binary `+` is applied to strings, it merges (concatenates) them
```javascript
let s = "my" + "string";
alert(s); // mystring
```
it doesn’t matter whether the first operand is a string or the second one.
Just works with sum. 
```javascript
alert( 6 - '2' ); // 4, converts '2' to a number
alert( '6' / '2' ); // 3, converts both operands to numbers
```
Also, the operations goes from left to right.
```javascript
alert('1' + 2 + 2); // "122" and not "14"
```
___
# What is other way to convert string to numbers shorter?
If we want to treat them as numbers, we need to convert and then sum them:
```javascript
let apples = "2";
let oranges = "3";

// both values converted to numbers before the binary plus
alert( +apples + +oranges ); // 5

// the longer variant
// alert( Number(apples) + Number(oranges) ); // 5
```
The unary operator does that.

# How the = operator is handle by repetitions?
```javascript
let a, b, c;

a = b = c = 2 + 2;

alert( a ); // 4
alert( b ); // 4
alert( c ); // 4
```

Chained assignments evaluate from right to left. First, the rightmost expression `2 + 2` is evaluated and then assigned to the variables on the left: `c`, `b` and `a`


___




# References
[[Learn JavaScript Ultimate]]
