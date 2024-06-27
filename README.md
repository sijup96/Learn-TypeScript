# Learn-TypeScript
=> JavaScript
-> number - ( we can write a number like 123_456_789 for more readability )
-> string
-> boolean
-> null
-> undefined
-> Object
-> array
=> TypeScript
-> any - ( Don't use any because it is against the typeScript feature )
-> unknown
-> never
-> enum 
--> // PascalCase
const enum Size { Small = 1, Medium, Large }; // use const for more optimize the code.
let mySize:Size = Size.Medium; (output - 2)

-> tuple - mostly used in key-value pairs ( set the datatypes specified values and fixed length of array ) eg: let test:[number,string]=[1,'siju'] 
# function [ don't return undefined ]
-> noUnusedLocals
-> noUnusedParameters
-> noImplicitReturns

function calc( income:number, taxYear = 2022):number{ // 2022 is a default value.
if(( taxYear || 2022 )< 2022) return income*2 // 2022 is a default value. 
return income
}
