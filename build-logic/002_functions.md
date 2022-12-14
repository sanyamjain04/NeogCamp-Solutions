# Functions

## Easy

<!-- Question 1 -->

 <details>

  <summary>
       1. Given a and b, your function should return the value of a<sup>b</sup>  
  
  **Example:**
  Input: `power(2,3)` ––> **Output:** `8` 
  </summary>

-  `index.js`

```javascript
const power = (num, pow) => {
    let number = 1;
    for(let i = 0; i < pow; i++){
        number *= num;
    }
    return number;
} 

power( 2 , 3);  // 8

```

</details> 
  
<!-- Question 2 -->

  <details>

<summary>
       2. Given length of a regular hexagon, your function should return area of the hexagon.
  
**Example:**
Input: `areaOfHexagon(10)` ––> **Output:** `259.80`
</summary>

-  `index.js`

```javascript
const areaOfRegularHexagon = (side) => {
    return (3 *  Math.sqrt(3) )/2 * side * side; 
}

areaOfRegularHexagon(10);   // 259.80

```

</details> 


<!-- Question 3 -->

<details>

<summary>
       3. Given a sentence, your functions should return the number of words in the sentence.
  
  **Example:**  
  **Input:** `noOfWords(We are neoGrammers)` ––> **Output:** `3`
</summary>

  -  `index.js`

  ```javascript
const noOfWords = (sentence) => {
    let wordsCount = 0;
    for(let i = 0; i< sentence.length; i++){
        if(sentence[i] ===  " "){
            wordsCount++;
        }
    }   
    return wordsCount + 1;
}   	  

noOfWords("We are neoGrammers");   // 3

  ```

</details> 

<!-- Question 4 -->

<details>

<summary>
       4. Given n numbers, your function should return the minimum of them all. The number of parameters won't be accepted from user.
  
**Example:**  
**Input:** `findMin(3,5)` ––> **Output:** `3`  
**Input:** `findMin(3,5,9,1)` ––> **Output:** `1`  
*(Hint: Lookup rest parameters in JavaScript)
</summary>

  -  `index.js`

  ```javascript

const minNum = (...nums) => {
	let min = nums[0];
  for (let i =1; i< nums.length; i++) {
    if(nums[i] < min){
		min = nums[i];
    }
  }
  return min;
} 
minNum(3,5,9,1)  // 1
  ```

</details> 

<!-- Question 5 -->

<details>

<summary>
      5. Given n numbers, your function should return the maximum of them all. The number of parameters won't be accepted from user.  
  
**Example:**  
**Input:** `findMax(3,5)` ––> **Output:** `5`  
**Input:** `findMax(3,5,9,1)` ––> **Output:** `9`  
*(Hint: Lookup rest parameters in JavaScript)*
</summary>


  -  `index.js`

  ```javascript
const maxNum = (...nums) => {
	let max = nums[0];
  for (let i =1; i< nums.length; i++) {
    if(nums[i] > max){
		max = nums[i]
    }
  }
  return max;
}
maxNum(3,5,9,1);   // 9 
  ```

</details> 

<!-- Question 6 -->

<details>

<summary>
       6. Given three angles of a triange, your function should return if it is a scalene, isosceles, equilateral triangle or not a triangle at all.
  
**Example:**  
**Input:** `typeOfTriangle(30, 60, 90)` ––> **Output:** `Scalene Triangle`
</summary>


  -  `index.js`

  ```javascript
const isTriangle = (a, b, c) => {
    if(a == 0 || b == 0 || c == 0) return false;
    if(a == undefined || b == undefined || c == undefined) return false;
     if (a + b >= c && a + c >= b && b + c >= a)
        return true;
    else
        return false;
}

const nameOfTriangle = (x, y, z) => {
    if(isTriangle(x, y, z)){
            
        if(x === y && y === z ){
            return "Equilateral Triangle";
        }else if(x == y || y == z || z == x){
            return "Isosceles Triangle";
        }else {
            return "Scalane Triangle";
        }
    }else {
        return "Not a Triangle";
    }
}

nameOfTriangle(30, 60, 90);  // Scalane Triangle
  ```

</details> 




## Medium

<!-- Question 1 -->

<details>

<summary>
       1. Given an array, your function should return the length of the array.  
  
**Example:**  
**Input:** `arrayLength([1,5,3,7,8])` ––> **Output:** `5`
</summary>

  -  `index.js`

  ```javascript
const arrayLength = ([...arr]) => {
    return arr.length;
}

arrayLength([0,1,2,3,4,5,6,7,8,9,10]);  // 11

  ```

</details> 

<!-- Question 2 -->

<details>

<summary>
       2. Given an array and an item, your function should return the index at which the item is present.  
  
**Example:**  
**Input:** `indexOf([1,6,3,5,8,9], 3)` ––> **Output:** `2`
</summary>


  -  `index.js`

  ```javascript
const indexOf = ([...arr], item) => {
    for(let i =0; i< arr.length; i++){
        if(arr[i] == item) return i;
    }
    return "Item not found";
}

indexOf([0,5,1,9,3,5,8,10], 3);    // 4

  ```

</details> 


<!-- Question 3 -->

<details>

<summary>
       3. Given an array and two numbers, your function should replace all entries of first number in an array with the second number. 
  
**Example:**  
**Input:** `replace([1,5,3,5,6,8], 5, 10)` ––> **Output:** `[1,10,3,10,6,8]`
</summary>

  -  `index.js`

  ```javascript
const replace = ([...arr], item, item2) => {
    for(let i =0; i< arr.length; i++){
        if(arr[i] == item) arr[i] = item2;
         
    }
    return arr;
}
replace([0,5,1,9,3,5,8,10], 5, 99);    //  [0, 99, 1, 9, 3, 99, 8, 10]

  ```

</details> 

<!-- Question 4 -->

<details>

<summary>
       4. Given two arrays, your function should return single merged array. 
  
**Example:**  
**Input:** `mergeArray([1,3,5], [2,4,6])` ––> **Output:** `[1,3,5,2,4,6]`
</summary>


  -  `index.js`

  ```javascript
const mergeArray = ([...arr1],[...arr2]) => {
    for(let i =0; i< arr2.length; i++){
       arr1.push(arr2[i]);         
    }
    return arr1;
}
mergeArray([1,3,5], [2,4,6]);   // [1, 3, 5, 2, 4, 6]

  ```

</details> 

<!-- Question 5 -->

<details>

<summary>
      5. Given a string and an index, your function should return the character present at that index in the string.  
  
**Example:**  
**Input:** `charAt("neoGcamp", 4)` ––> **Output:** `c`
</summary>


  -  `index.js`

  ```javascript
const charAt = (string , index ) => {
    return string.charAt(index);
}

charAt("neoGcamp", 4);  // 'c'
	  

  ```

</details> 

<!-- Question 6 -->

<details>

<summary>
       6. Given two dates, your function should return which one comes before the other. 
  
**Example:**  
**Input:** `minDate('02/05/2021', '24/01/2021')` ––> **Output:** `24/01/2021`
</summary>

  - `index.html`

  ```html
        (add html code here if needed)

  ```

  -  `index.js`

  ```javascript
        (add javacript code here if needed)	  

  ```

</details> 


## Advanced

<!-- Question 1 -->

<details>

<summary>
      1. Write a function which generates a secret code from a given string, by shifting characters of alphabet by N places.
  
**Example:**  
**Input:** `encodeString("neogcamp", 2)` ––> **Output:** `pgqiecor`  
Explanation: 2 represents shifting alphabets by 2 places. a –> c, b –> d, c –> e and so on.
</summary>

  - `index.html`

  ```html
        (add html code here if needed)

  ```

  -  `index.js`

  ```javascript
        (add javacript code here if needed)	  

  ```

</details> 

<!-- Question 2 -->

<details>

<summary>
       2. Given a sentence, return a sentence with first letter of all words as capital.  
  
**Example:**  
**Input:** `toSentenceCase('we are neoGrammers')` ––> **Output:** `We Are NeoGrammers`
</summary>

  - `index.html`

  ```html
        (add html code here if needed)

  ```

  -  `index.js`

  ```javascript
        (add javacript code here if needed)	  

  ```

</details> 


<!-- Question 3 -->

<details>

<summary>
       3. Given an array of numbers, your function should return an array in the ascending order.  
  
**Example:**  
**Input:** `sortArray([100,83,32,9,45,61])` ––> **Output:** `[9,32,45,61,83,100]`
</summary>

  - `index.html`

  ```html
        (add html code here if needed)

  ```

  -  `index.js`

  ```javascript
        (add javacript code here if needed)	  

  ```

</details> 

<!-- Question 4 -->

<details>

<summary>
       4. Given a sentence, your function should reverse the order of characters in each word, keeping same sequence of words.  
  
**Example:**  
**Input:** `reverseCharactersOfWord('we are neoGrammers')` –––> **Output:** `ew era sremmarGoen`
</summary>

  - `index.html`

  ```html
        (add html code here if needed)

  ```

  -  `index.js`

  ```javascript
        (add javacript code here if needed)	  

  ```

</details> 








