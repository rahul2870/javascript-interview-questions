# javascript-interview-questions

## 1.) What is the object type?
The object type is a fundamental data type that represents a collection of key-value pairs. It is a built-in data type that allows you to create, store, and manipulate complex data structures.<br/>
Objects in JavaScript are considered reference types, meaning that when you assign an object to a variable or pass it as a function parameter, you are actually assigning a reference to the object's location in memory rather than making a direct copy of its values.<br/>
Objects are created using either object literal notation or the Object constructor. Here's an example of creating an object using object literal notation:<br/>
```
javascript
Copy code
const person = {
  name: "John",
  age: 30,
  profession: "Engineer"
};
```
In this example, the person object has properties such as name, age, and profession, which are accessed using dot notation (person.name, person.age, etc.). You can add, modify, or delete properties of an object dynamically.

## 2.) Explain arrays in JavaScript?
An array is an object that holds values (of any type) not particularly in named properties/keys, but rather in numerically indexed positions:<br/>
```
 let arr = ["hello world", 42, true]; 
 
 arr[0]; // "hello world" 
 arr[1]; // 42 
 arr[2]; // true 
 arr.length; // 3 
 
 typeof arr; // "object"       
```

## 3.) What is typeof operator?
JavaScript provides a typeof operator that can examine a value and tell you what type it is:
```
 let a; 
 typeof a; // "undefined" 
 
 a = "hello world"; 
 typeof a; // "string" 
 
 a = 42;  
 typeof a; // "number" 
 
 a = true;  
 typeof a; // "boolean" 
 
 a = null;  
 typeof a; // "object" -- weird, bug 
 
 a = undefined;  
 typeof a; // "undefined" 
 
 a = ["a", "b", "c"]; 
 typeof a; // "object" 
 
 a = { b: "c" }; 
 typeof a; // "object"
```
## 4.) Explain equality in JavaScript?
JavaScript has both strict and type–converting comparisons:<br/>

- Strict comparison (e.g., ===) checks for value equality without allowing coercion<br/>
- Abstract comparison (e.g. ==) checks for value equality with coercion allowed<br/>
```
 let a = "42"; 
 let b = 42; 
 
 a == b; // true 
 a === b; // false 
```       
Some simple equalityrules:<br/>

- If either value (aka side) in a comparison could be the true or false value, avoid == and use ===.<br/>
- If either value in a comparison could be of these specific values (0, "", or [] -- empty array), avoid == and use ===.<br/>
- In all other cases, you're safe to use ==. Not only is it safe, but in many cases it simplifies your code in a way that improves readability.<br/>

