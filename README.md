## TypeScript-Basics

## 1. Variables & Datatypes 
```
/* Data types in JavaScript: primitives[number, string, boolean], array */ 
// TypeScript: Main advantage over javascript is type safety 

// string: sequence of charectors 
let stdName:string = "Vaishnav Krishna P";
console.log("Student Name: " + stdName);

//numbers: numerical data's 
let stdMarks:number = 90;
console.log("Student Mark: " + stdMarks);

//boolean: boolean datatype 
let stdIsPass:boolean = true;
console.log("Student pass: " + stdIsPass);

//array: used to store a collection of values which are same datatype 
let studentMarks:number[] = [90, 87, 45, 34, 19];
console.log(studentMarks);

let studentNames:string[];
studentNames = ["Vaishnav", "Abhijith", "Karan"]; // can only store string kind of data 
console.log(studentNames);

//any: can store any datatypes 
let studentGrade:any;
studentGrade = "A";
console.log("Student Grade: " + studentGrade);
studentGrade = 100;
console.log("Student Grade: " + studentGrade); // if variable created with any, can store any datatype 
```

## 2. Functions 
```
/* functions: function is a block of code that can be executed again and again */ 

//1. General function in JS 
// rules: have to sepcify the datatype of the parameters ,also return type(optional)
function add(num1:number, num2:number):number{ 
    return num1+num2;
}
console.log("Sum Calculated in Gen function: " + add(5,9));

//2. Arrow function: function defined using the arrow 
const addArrow = (num1:number, num2:number):number => num1+num2; // if you add brances you have to add the return key word 
console.log("Sum Calculated in arrow function: " + addArrow(4,5));

//3. Anonymous function: function without name 
const addAnonymous = function(num1:number, num2:number):number {
    return num1+num2;
}
console.log("Sum Calculated in Anonymous function: " + addAnonymous(14,5)); 
```
## 3. Parameter types in Type script
```
/* Different types of parameters 
1. optional parameter 
2. required parameter 
3. rest parameter 
*/ 
function add(num1:number, num2:number):number{ // num1,num2 are required parameter 
    return num1+num2;
}
console.log("Sum of 2 numbers(2,3): " + add(2,3));


function sumOfThree(num1:number, num2:number, num3?:number):number{ // num1,num2 are required parameter 
    return num3 ? num1+num2+num3:num1+num2;
}

function sumOfN(num1:number, num2:number, ...num3:number[]){ // rest parameters 
    return num1 + num2 + num3.reduce( (a:number,b:number):number => {
        return a+b;
    })
}
console.log("Sum of 2 numbers(2,3): " + add(2,3));

console.log("Sum of 3 numbers(12,3,5): " + sumOfThree(12,3,5));

console.log("Sum of 2,3,4,5,6,7 is: "+ sumOfN(2,3,4,5,6,7));

```
