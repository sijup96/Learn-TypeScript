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
# objects
-> initialize
let employee:{
id: number,
name?:string // ( ? means name is optional. If we putting this then no need to set name: )
} = { id:1, name:'siju'}

-> readonly
let employee:{
readonly id: number,
name:string 
} = { id:1, name:'siju'}
=> New way
type Employee={
readonly id: number,
name: string,
retire: (date:Date) => void
}

# Type aliases
# Unions and intersections

=> union [ OR ]
function kgToLbs(weight: number | string) : number{
// Narrowing
if(typeof weight === 'number')
return weight * 2
else
return parseInt(weight)*2

=> Intersection [ AND ]
type Dragable:{
drag:() => void,
}
type Resizable:{
resize:() => void
}
type UIWidget =Dragable & Resizable
let textBox: UIWidget{
drag:() => {},
resize:() => {}

# Type narrowing
=> Literal (exact, specific)
type Quantity = 50 | 100
let quantity: Quantity = 100

type Metric = 'cm' | 'inch';
 
# Nullable types
=> Handle by union with conditional operator

# The unknown type
=> use optional chaining.
# The never type
