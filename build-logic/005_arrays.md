# Arrays

## beginner - intermediate


<!-- Question 1 -->

 <details>

  <summary>
      1. Find sum of an array and display the output . Example [10,4,5,2,5,6,9].

  </summary>


-  `index.js`

```javascript
const array = [10, 4, 5, 2, 5, 6, 9];
 
 const sum = (arr) => {
    let ans = 0; 
    for(let i = 0; i < arr.length; i++){
       ans += arr[i]; 
    }
    return ans;
}

sum(array);  // 41
```

</details>


<!-- Question 2 -->

 <details>

  <summary>
      2. Find average of an array and display the output.

  </summary>


-  `index.js`

```javascript
const array = [10, 4, 5, 2, 5, 6, 9];
 
const average = (arr) => {
    let ans = 0; 
    for(let i = 0; i < arr.length; i++){
       ans += arr[i]; 
    }
    return (ans / arr.length).toFixed(2);
}
                                  
average(array);  // 5.86

```

</details>


<!-- Question 3 -->

 <details>

  <summary>
      3. Find maximum and minimum of an array.

  </summary>


-  `index.js`

```javascript
const array = [10, 4, 5, 2, 5, 6, 9];
 
 const minMax = (arr) => {
    let max = arr[0];
    let min = arr[0];
    for(let i = 1; i < arr.length; i++){
      if(arr[i] > max) {
        max = arr[i];
      }
      if(arr[i] < min){
        min = arr[i];
      }
      
    }
    return {max, min};
}
                       
minMax(array);   // {min: 2, max: 10}

```

</details>


<!-- Question 4 -->

 <details>

  <summary>
      4. Find Median and Mode of an array.
    - Median : (N+1/2)th term.
    - Mode : Most repeating term
  </summary>


-  `index.js`

```javascript
const array = [2, 3, 5, 8, 9, 17, 27, 27, 27,  33, 42, 45, 47, 49];
 
 const mediumMode = (arr) => {
   let medium = arr[parseInt((arr.length + 1) / 2)];
    let bestElem = arr[0] ;
   let bestStreak = 1;
   let currElem = arr[0];
   let currStreak = 1;
  for (let i = 1; i < arr.length; i++) {
    if(arr[i-1] != arr[i] ){
      if(currStreak >  bestStreak){
        bestStreak = currStreak;
        bestElem = currElem; 
      } 
      
        currStreak = 0;
        currElem = arr[i];
      
    }
    currStreak++;
  }
   const mode = currStreak > bestStreak ? currElem : bestElem;
   
    return {medium, mode};
}
  
  mediumMode(array);  // {medium: 27, mode: 27}

```

</details>


<!-- Question 5 -->

 <details>

  <summary>
      5. Find sum of two arrays.
    - [3,5,2,9,4] = 3+5+2+9+4 = 23
    - [6,2,8,1,3] = 6+2+8+1+3 = 20
    - Final Output : 20+23 = 43
  </summary>


-  `index.js`

```javascript
      (add javacript code here if needed)	  

```

</details>


<!-- Question 6 -->

 <details>

  <summary>
      6. Find number of constants and vowels in a string.

  </summary>


-  `index.js`

```javascript
      (add javacript code here if needed)	  

```

</details>


<!-- Question 7 -->

 <details>

  <summary>
      7. Shift an array by X to right.
    - Example [1,2,3,4,5] after shifting to right [5,1,2,3,4]
  </summary>


-  `index.js`

```javascript
      (add javacript code here if needed)	  

```

</details>


## Advanced

<!-- Question 1 -->

 <details>

  <summary>
      1. Find the sum of two matrix.
  </summary>


-  `index.js`

```javascript
      (add javacript code here if needed)	  

```

</details>


<!-- Question 2 -->

 <details>

  <summary>
      2. Display transpose of matrix. Explaination https://www.varsitytutors.com/linear_algebra-help/the-transpose 
  </summary>


-  `index.js`

```javascript
      (add javacript code here if needed)	  

```

</details>


<!-- Question 3 -->

 <details>

  <summary>
      3.Find Identity matrix. Explanation https://www.varsitytutors.com/hotmath/hotmath_help/topics/identity-matrix
  </summary>


-  `index.js`

```javascript
      (add javacript code here if needed)	  

```

</details>
