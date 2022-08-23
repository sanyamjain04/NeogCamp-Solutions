# Operators, Branching, Loops

## Easy

<!-- Question 1 -->
 
<details>
  <summary>
   1. Write a program to add 5 numbers. The value of numbers are num1=5, num2=13, num3=7, num4=21 and num5=48.
  </summary>
        
- `index.js`
```javascript
const num1 = 5;
const num2 = 13;
const num3 = 7;
const num4 = 21;
const num5 = 48;
    
const add = (a, b, c, d, e) => {
    return a + b + c + d + e; 
}
add(num1, num2, num3, num4, num5 );  // 94
```
</details>

<!-- Question 2 -->
 
<details>
  <summary>
   2. Write a program to take a number input from user and determine whether the number is odd or even.
  </summary>
    
- `index.html`
```html
   <label for="input">
        Enter number :  <input type="number" id="input" name="input" />
   </label>
    <button id="check"> Check </button>
```
    
- `index.js`
```javascript
    const checkBtn = document.querySelector("#check");
    const input = document.querySelector("#input");
    
    const checkOddEven = (num) => {
        if(num % 2 === 0) console.log("number is Even")
        else console.log("number is Odd")
    }
    
    checkBtn.addEventListener("click", () => checkOddEven(input.value) );
    
```
</details>

<!-- Question 3 -->
 
<details>
  <summary>
   3. Write a program to find the maximum and minimum out of two given numbers. The numbers are num1=129 and num2=251.
  </summary>
    
    
- `index.js`
```javascript
const num1 = 129;
const num2 = 251;
    
const maxMin = (a, b) => {
    if(a > b) console.log("Maximum number is " + a + " Minimum number is " + b)
    else console.log("Maximum number is " + b + " Minimum number is " + a)
}
    
maxMin(num1, num2);   // Maximum number is 251 Minimum number is 129
    
```
</details>

<!-- Question 4 -->
 
<details>
  <summary>
     4. Write a program to find the maximum out of three given numbers. The numbers are num1=8, num2=23 and num3=17.
  </summary>
        
- `index.js`
```javascript
const num1 = 8;
const num2 = 23;
const num3 = 17;
    
const maximumNumber = (a, b, c) => {
    if(a > b){
        if( a > c) console.log( a + " is the maximum number")
        else console.log(c + " is the maximum number")       
    } else {
        if( b > c) console.log(b + " is the maximum number") 
        else  console.log(c + " is the maximum number")   
    }
}
    
maximumNumber(num1, num2, num3);    // 23 is the maximum number
```
</details>

<!-- Question 5 -->
 
<details>
  <summary>
   5. Write a program to find the minimum out of three given numbers. The numbers are num1=35, num2=29 and num3=46.
  </summary>
     
- `index.js`
```javascript
const num1 = 35;
const num2 = 29;
const num3 = 46;
    
const minimumNumber = (a, b, c) => {
    if(a > b){
        if( b < c) console.log( b + " is the minimum number")
        else console.log(c + " is the minimum number")       
    } else {
        if( a > c) console.log(c + " is the minimum number") 
        else  console.log(a + " is the minimum number")   
    }
}
    
minimumNumber(num1, num2, num3);    // 29 is the minimum number
```
</details>

<!-- Question 6 -->
 
<details>
  <summary>
   6. Write program to take a month as an input from the user and find out whether the month has 31 days or not.
  </summary>
    
- `index.html`
```html
   <label for="input">
        Enter number :  <input type="number" id="input" name="input" />
   </label>
   <button id="check"> Check </button>
```
    
- `index.js`
```javascript
    const checkBtn = document.querySelector("#check");
    const input = document.querySelector("#input");
    
    const monthDays = (name) => {
    const monthName = name.toLowerCase();
        if(monthName == "january" || monthName == "march" || monthName == "may" || 
        monthName == "july" || monthName == "august" || 
        monthName == "october" || monthName == "december") console.log("Month has 31 days")
        else console.log("Month has not 31 days")
    }
    monthDays(may)
    checkBtn.addEventListener("click", () => monthDays(input.value) )    
    
```
</details>











## Intermediate

1. Fizzbuzz - Write a program to return an array from 1 to 100. But for every multiple of 3, replace the number with "Fizz", for every multiple of 5, replace the number with "Buzz" and for every multiples of 3 & 5, replace with "FizzBuzz".

    Your output should look something like this `1, 2, Fizz, 4, Buzz, Fizz, 7, 8, Fizz, Buzz, 11, Fizz, 13, 14, FizzBuzz, 16, 17 ..... `

2. Print the following star pattern :-

    \* \
    \* \* \
    \* \* \* \
    \* \* \* \* \
    \* \* \* \* \*

3. Write a program to take a number input from user and print multiplication table 12 times for that number.

4. Write a program to return a Fibonacci series : 0,1,1,2,3,5,8,13,21....

5. Write a program to take an input from a user and find its Factorial.
   `Example: Factorial of 5 is 120`
6. Write a Program to take a number input from user and find if the number is Prime or not.

7. Write a program to take a day as an input and determine whether it is a weekday or weekend.
   `Example: Tuesday is weekday.`
