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

