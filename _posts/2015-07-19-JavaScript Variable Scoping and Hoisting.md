I recently had a memory jog regarding variable hoisting. So I decided to verify my existing knowledge about this area and consolidate it. Finally put it down into words such that I do not forget it.

*Scope*
JavaScript has two distinct scopes when it comes to variables. A variable that is declared outside the scope of a function is in the global scope. A variable that is declared within a function is accessible within the scope of the function and any nested functions declared within. It is important to note, however, that JavaScript does not support block level scoping i.e. if a variable is defined within a for loop, the scope of the variable does not just the loop, but the whole function. [Fiddle](http://jsfiddle.net/PGfgv/1503/)

*Hoisting*
The definition variable hoisting comes about via the scope of a variable. 
There are 4 ways that a variable can enter a scope

 1. Language defined
 2. Function parameters
 3. Function declarations
 4. Variable declarations

In other words hoisting refers to moving declarations to the top.

> Function and variable declarations (functions first, then variables)
> are hoisted to the top of their respective scope by the JavaScript
> interpreter with function parameters and language defined variables
> being there by default.
> The following [fiddle](http://jsfiddle.net/vcjL9xyd/7/) illustrates how this works.

Seeing as I'm not that brilliant, I pulled information from a few places and they are listed below.

References : 

 1. http://www.sitepoint.com/demystifying-javascript-variable-scope-hoisting
 2. http://www.adequatelygood.com/JavaScript-Scoping-and-Hoisting.html