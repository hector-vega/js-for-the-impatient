# Excercises

1.  What happens when you add  `0`  to the values  `NaN`,  `Infinity`,  `false`,  `true`,  `null`, and  `undefined`? What happens when you concatenate the empty string with  `NaN`,  `Infinity`,  `false`,  `true`,  `null`, and  `undefined`? Guess first and then try it out.
    
2.  What are  `[] + []`,  `{} + []`,  `[] + {}`,  `{} + {}`,  `[] - {}`? Compare the results of evaluating the expressions at the command line and assigning them to a variable. Explain your findings.
    
3.  As in Java and C++ (and unlike Python which follows many centuries of mathematical experience),  `n % 2`  is  `-1`  if  `n`  is a negative integer. Explore the behavior of the  `%`  operator for negative operands. Analyze integers and floating-point numbers.
    
4.  Suppose  `angle`  is some angle in degrees that, after adding or subtracting other angles, has assumed an arbitrary value. You want to normalize it so that it is between 0 (inclusive) and 360 (exclusive). How do you do that with the  `%`  operator?
    
5.  List as many different ways as you can to produce the string with two backslash characters  `\\`  in JavaScript, using the mechanisms described in this chapter.
    
6.  List as many different ways as you can to produce the string with the single character  ![Images](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9780136502166/files/graphics/bcircle.jpg)  in JavaScript.
    
7.  Give a realistic example in which a template string has an embedded expression that contains another template string with an embedded expression.
    
8.  Give three ways of producing an array with a “hole” in the index sequence.
    
9.  Declare an array with elements at index positions  `0`,  `0.5`,  `1`,  `1.5`, and  `2`.
    
10.  What happens when an array of arrays is converted to a string?
    
11.  Make a couple of objects representing people and store them in variables  `harry`  and  `sally`. To each person, add a property  `friends`  that contains an array with their best friends. Suppose  `harry`  is a friend of  `sally`  and  `sally`  is a friend of  `harry`. What happens when you log each object? What happens when you call  `JSON.stringify`?

# Answers

 1.  The results are the following:
	 - Additions to zero:
			 - `0 + NaN` -> `0`
			 - `0 + Infinity` -> `Infinity`
			 - `0 + false` -> `0`
			 - `0 + true` -> `1`
			 - `0 + null` -> `0`
			 - `0 + undefined` -> `undefined`
	 - String concatenation:
			 - `'' + NaN` -> `'Nan'`
			 - `'' + Infinity` -> `'Infinity'`
			 - `'' + false` -> `'false'`
			 - `'' + true` -> `'true'`
			 - `'' + null` -> `'null'`
			 - `'' + undefined` -> `'undefined'`
 2. Results:
		 - `[] + []` -> `''`
		 - `{} + []` -> `'[object Object]'`
		 - `[] + {}` -> `'[object Object]'`
		 - `{} + {}` -> `'[object Object][object Object]'`
		 - `[] - {}` -> `'[object Object]'`
3. Module operator (%) with negative numbers:
		- It returns negative numbers such as `-0` as in the operation `-2 % 0`.
		- When there's a different number from zero it is also a negative one just like `-100 % 6 = -4`.
4. PENDING
5. Ways to escape a double backslash `\\`
		- `console.log('\\\\')`
		- `console.log('\\\u{005C}')`
6. Ways to write the emoji 🌐
		- `console.log('🌐')`
		- `console.log('\\\u{1F310}')`
7. Example using nested template strings:
		- ``const classes = `header ${
		  isLargeScreen() ? "" : `icon-${item.isCollapsed ? "expander" : "collapser"}`
		}``
8. 