# Numbers

<!-- Question 1 -->

 <details>

  <summary>
       1. Write a program to input 2 numbers and display the sum of the numbers to the console.

    
    Input Number 1: 20
    Input Number 2: 40
    Sum : 60
    
  </summary>


-  `index.js`

```javascript
const num1 = 20;
const num2 = 40;

const sum = (a, b) => {
       return a + b;
} 

console.log(sum(num1, num2) );	  

```

</details>

<!-- Question 2 -->

 <details>

  <summary>
       2. Write a JavaScript program to calculate the simple interest given P,R,T with the given formula.
      
   Formula:
      
   `SI = (P * T * R) / 100`
   Where:
      
   P = principal amount 
      
   T = time 
      
   R = rate 
      
   SI = simple interest

    
    Input: P=100, R=6%, T=2
    Output: 12
    
  </summary>


-  `index.js`

```javascript

const SI = (principal, rate, time) => {

    return  ( principal * rate * time ) / 100 ;
    
}

SI(100, 6, 2);  //   12

```

</details>

<!-- Question 3 -->

 <details>

  <summary>
      3. Write a program to calculate the kinetic energy of a body with mass 'm' and volume 'v'.

    Formula :  0.5 * m * v * v
  </summary>


-  `index.js`

```javascript
const kineticEnergy = (mass, volume) => {
    return .5 * mass * volume * volume;
}

kineticEnergy(5, 10);   // 250  

```

</details>

<!-- Question 4 -->

 <details>

  <summary>
       4. Write a program to convert Fahrenheit to Celsius. For Fahrenheit to Celsius conversion use:
      
   `C = (F - 32) * 5/9`
   'F' and 'C' are the temperatures on the Fahrenheit scale and Celsius scale respectively.

    
    Input: 56
    Output: 13.33333
    
  </summary>


-  `index.js`

```javascript
const celcius = (fahrenheit ) => {
    return ( fahrenheit - 32 ) * 5/9;
}

celcius(56);   //  13.33333333 

```

</details>

<!-- Question 5 -->

 <details>

  <summary>
       5. Calculate the area, perimeter of a square of side 'a'. Also, calculate the surface area and the volume of a cube of side 'a'.

    Formula :

    Area: a*a

    Perimeter: 4*a

    Surface Area: 6*a*a

    Volume: a*a*a
  </summary>


-  `index.js`

```javascript
const areaOfSquare = (side) => {
    return side * side;
}

const perimeterOfSquare = (side) => {
    return 4 * side;
}

const surfaceAreaOfCube = (side) => {
    return 6 * side * side;
}

const volumeOfCube = (side) => {
    return side * side * side;
}
areaOfSquare(3);              // 9
perimeterOfSquare(3);         // 12
surfaceAreaOfCube(3);         // 54
volumeOfCube(3);              // 27


```

</details>

<!-- Question 6 -->

 <details>

  <summary>
       6. Given the Cost Price(CP) and Selling Price(SP) of a product. Write a Program to Calculate the Profit or Loss.

    
    Input: CP = 1500, SP = 2000
    Output: 500 Profit

    Input: CP = 3125, SP = 1125
    Output: 2000 Loss
    
  </summary>


-  `index.js`

```javascript
const profitLoss = (cp, sp) => {
    const diff = sp - cp;
    if(diff > 0) return "Profit: " + diff;
    else if (diff < 0) return "Loss: " + diff;
    else return "No Profit No Loss";
}

profitLoss(1500, 2000)  // Profit: 2000

```

</details>

<!-- Question 7 -->

 <details>

  <summary>
       7. Write a program to calculate sum of N natural digits, as input by the users?

    
    Enter a positive integer: 100
    Sum = 5050
    
  </summary>


-  `index.js`

```javascript
const sum = (n) => {
    let mul = 0;
    for(let i = 1; i<= n; i++){
        mul += i ;
    }
    return mul;
}

sum(100);    //  5050

```

</details>

<!-- Question 8 -->

 <details>

  <summary>
       8. Write a Program to Print N Odd Number in Descending Order.

    
    Input : 4
    Output : 7
    5
    3
    1
    
  </summary>


-  `index.js`

```javascript
const oddNumber = (n) => {
    if(n % 2 == 0) n -= 1; 
    for(let i = n; i > 0; i -= 2){
        console.log(i);
    }
}

oddNumber(9);  // 9, 7, 5, 3, 1

```

</details>

<!-- Question 9 -->

 <details>

  <summary>
       9. Write a JavaScript program to compute the sum of all digits that occur in a given string.

    
    Input: 1234
    Output: 1+2+3+4 = 10
    
  </summary>


-  `index.js`

```javascript
const stringSum = (n) => {
    let length = n.toString().length;
    let sum = 0;
    for(let i =0; i< length; i++){
        let rem = n % 10;
        sum += rem;
        n = parseInt(n /10);
    }
    return sum;
}

stringSum(4321);

```

</details>

<!-- Question 10 -->

 <details>

  <summary>
       10. Write a JavaScript program that reverses a number.

    Example:

    
    Input:  32243;
    Output:  34223
    
  </summary>


-  `index.js`

```javascript
      const reverse = (n) => {
  
    let length = n.toString().length;
    let sum = 0;
    for(let i =0; i< length; i++){
        let rem = n % 10;
        sum = sum * 10 + rem; 
        n = parseInt(n /10);
    }
    return sum;
}

reverse(1234);   // 4321

```

</details>

<!-- Question 11 -->

 <details>

  <summary>
       11. Write a Program to cyclically Rotate a Number by X positions in the left direction, as provided by the user.

    Example-

    
    Enter a Number : 1234
    Enter the Number of Rotations : 2
    Output : 3412
    
  </summary>


-  `index.js`

```javascript
const rotate = ( num, n) => {
    let length = num.toString().length -1;
    for(let i =0; i< n; i++){
        let rem = num % 10;
         num = parseInt(num /10);
        num = (rem * Math.pow(10, length)) + num;
        
    }

    return num;
}
	  
rotate(1234, 2);   // 4312

```

</details>

<!-- Question 12 -->

 <details>

  <summary>
       12. Write a Program to convert Decimal to Binary.

    
    Enter the number to convert: 5
    Binary of Given Number is=101
    

    Follow up Question : Write a Program to Convert Octal to Decimal.

    
    Enter an octal number: 116
    Octal of Given Number = 78 in decimal
    
  </summary>


-  `index.js`

```javascript
      const deciToBinary = (num) => {
    let ans = 0; let i = 1;
    while(num != 0){
        let rem = num % 2;
        ans =  rem * i + ans;
        num = parseInt( num / 2);
        i = i *10;
    }
    return ans;
}

deciToBinary(5);

```

</details>

