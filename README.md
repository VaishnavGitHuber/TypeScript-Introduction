## TypeScript-Basics
1. [Variables and Datatypes](#1-variables-and-datatypes)  
2. [Functions](#2-functions)  
3. [Parameters](#3-parameters)  
4. [Class](#4-class)  
5. [Objects](#5-objects)  
6. [This Keyword](#6-this-keyword)  
7. [Super Keyword](#7-super-keyword)  
8. [Extends Keyword](#8-extends-keyword)  
9. [Getters and Setters](#9-getters-and-setters)  
10. [Static Methods](#10-static-methods)


## 1. Variables and Datatypes
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
## 3. Parameters
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
## 4. Class
```
class Employee {
    public empId!:number; // '!' is kept to ignore the warning of initialisation
    private empName!:string;
    protected empNumber!:string;

    // constructors 
    public constructor(empId:number, empName:string, empNumber:string){
        this.empId = empId;
        this.empName = empName;
        this.empNumber = empNumber;
    }

    // print the informations about the employees
    public getInformation(){
        return `${this.empId}  ${this.empName} ${this.empNumber}`;
    }

    // getter and setters method: for the private attribute
    get employeeName():string {
        return this.empName;
    }
    set employeeName(empName:string){
        this.empName = empName;
    }
}

```
## 5. Objects
```
// creating a object for the employee 
let emp1 = new Employee(101, "Vaishnav Krishna P", "+91 9744065221");
let mgr1 = new Manager("Madhu", 102, "Vaishnav", "+91 972635473");
```
## 6. This Keyword
```
// constructors 
    public constructor(empId:number, empName:string, empNumber:string){
        this.empId = empId;
        this.empName = empName;
        this.empNumber = empNumber;
    }
```
## 7. Super Keyword
```
public constructor(mgrName:string, empId:number, empName:string, empNumber:string){
        super(empId, empName, empNumber)
        this.managerName = mgrName;
    }
```
## 8. Extends Keyword
```
class Manager extends Employee{
    public managerName!:string;

    public constructor(mgrName:string, empId:number, empName:string, empNumber:string){
        super(empId, empName, empNumber)
        this.managerName = mgrName;
    }
}
```
## 9. Getters and Setters
```
// getter and setters method: for the private attribute
    get employeeName():string {
        return this.empName;
    }
    set employeeName(empName:string){
        this.empName = empName;
    }
```
## 10. Static Methods
```
// static method 
    public static getCompanyName():string{
        return this.company;
    }
```
