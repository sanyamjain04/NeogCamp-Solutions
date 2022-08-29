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
const array = [10, 4, 5, 2, 5, 6, 9];
const array1 = [10, 14, 5, 2, 15, 6, 9];
 
 const sum = (arr) => {
    let ans = 0; 
    for(let i = 0; i < arr.length; i++){
       ans += arr[i]; 
    }
    return ans;
}

sum(array) + sum(array1);  // 102

```

</details>


<!-- Question 6 -->

 <details>

  <summary>
      6. Find number of constants and vowels in a string.

  </summary>


-  `index.js`

```javascript
let str = "my name is sanyam jain"
const string = (str) => {
  let vowels = 0;
  let consonants = 0;
  for (i = 0; i < str.length; i++) {
    ch = str[i];
    if (ch == 'a' || ch == 'e'
      || ch == 'i' || ch == 'o'
      || ch == 'u' || ch == 'A'
      || ch == 'E' || ch == 'I'
      || ch == 'O' || ch == 'U'){
      vowels++;
     }
    else if (ch == ' ') continue;
    else {
      consonants++;
    }
  }

  return { vowels, consonants };
}
string(str);   // { vowels: 7, consonants: 11 }  

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
const array = [1, 2, 3, 4, 5];
const shift = (array, n) => {
  for (let i = 0; i < n; i++) {
    let num = array[array.length - 1];
    array.pop();
    array.unshift(num);
  }
  return array;
}
shift(array, 2);     // [ 3, 4, 5, 1, 2 ]

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
const array = [[1, 2, 3, 4, 5], [1, 2, 3, 4, 5], [1, 2, 3, 4, 5]];
const array1 = [[1, 2, 3, 4, 5], [1, 2, 3, 4, 5], [1, 2, 3, 4, 5]];
const sum = (array, array1) => {
  if (array.length != array1.length) return "Matrix have different row length"
  if (array[0].length != array1[0].length) return "Matrix have different col length"
  let row = array.length;
  let col = array[0].length;
  for (let r = 0; r < row; r++) {
    for (let c = 0; c < col; c++) {
      array[r][c] += array1[r][c];
    }
  }
  return array;
}
sum(array, array1);     // [ [ 2, 4, 6, 8, 10 ], [ 2, 4, 6, 8, 10 ], [ 2, 4, 6, 8, 10 ] ]  

```

</details>


<!-- Question 2 -->

 <details>

  <summary>
      2. Display transpose of matrix. Explaination https://www.varsitytutors.com/linear_algebra-help/the-transpose 
  </summary>


-  `index.js`

```javascript
const array = [[1, 2, 3, 4, 5], [1, 2, 3, 4, 5], [1, 2, 3, 4, 5]];

const transpose = (A) =>  {
    let result = [];
    
    for(let i= 0; i<A[0].length; i++){
        let currentCol = []
        for(let j=0; j<A.length; j++){
            currentCol.push(A[j][i])
        }
        result.push(currentCol);
    }
    return result
};
transpose(array);   //[ [ 1, 1, 1 ], [ 2, 2, 2 ], [ 3, 3, 3 ], [ 4, 4, 4 ], [ 5, 5, 5 ] ]v

```

</details>


<!-- Question 3 -->

 <details>

  <summary>
      3.Find Identity matrix. Explanation https://www.varsitytutors.com/hotmath/hotmath_help/topics/identity-matrix
  </summary>


-  `index.js`

```javascript
const arr = [
   [1, 0, 0],
   [0, 1, 0],
   [0, 0, 1]
];
const identity = (array) => {
  for (let i = 0; i < array.length; i++) {
    for (let j = 0; j < array.length; j++) {
      if (i === j) {
        if ((array[i][j] === 1)) continue;
        else return false;
      } else {
        if (array[i][j] === 0) {
          continue;
        } else {
          return false;
        }
      }
    }
  }
  return true;
};


identity(arr);  // true

```

</details>
