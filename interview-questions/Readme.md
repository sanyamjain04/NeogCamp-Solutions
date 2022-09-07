## Sample Interview Questions and their Answers

 
<!-- Question 1 -->
 
<details>
  <summary>
    1. Create a web app which would take two inputs. It would also have 4 buttons:  +, -, x / . Based on the button clicked perform the operation on the two inputs. 
  </summary>
    
- `index.html`
```html
    <label for="num1">
      First Number: <input type="number" id="num1" />
    </label>
    <label for="num2">
      Second Number: <input type="number" id="num2" />
    </label>
    
    <button id="add"> + </button>
    <button id="sub"> - </button>
    <button id="mul"> * </button>
    <button id="div"> / </button>
    <p id="ans"></p>

```
    
- `index.js`
```javascript
const num1 = document.querySelector("#num1");
const num2 = document.querySelector("#num2");
const add = document.querySelector("#add");
const sub = document.querySelector("#sub");
const mul = document.querySelector("#mul");
const div = document.querySelector("#div");
const ans = document.querySelector("#ans");

const math = (x) => {
  const number1 = Number(num1.value);
  const number2 = Number(num2.value);
  if (x === "+") ans.innerHTML = number1 + number2;
  else if (x === "-") ans.innerHTML = number1 - number2;
  else if (x === "*") ans.innerHTML = number1 * number2;
  else ans.innerHTML = number1 / number2;
};

add.addEventListener("click", () =>  math("+") );
sub.addEventListener("click", () =>  math("-") );
mul.addEventListener("click", () =>  math("*") );
div.addEventListener("click", () =>  math("/") );

```
</details>

<!-- Question 2 -->

<details>
  <summary>
    2. Create a web app where I can input a text. Now create two buttons + and -. On clicking + increase the fontSize by 2px and vice versa.
  </summary>
    
- `index.html`
```html     
    <label for="input">
        Enter Name :  <input type="text" id="input"  />
    </label>
    <p id="output"></p>
    <button id="plus"> + </button>
    <button id="minus"> - </button>

```
    
- `index.js`
```javascript
const text = document.querySelector("#input");
const output = document.querySelector("#output");
const increase = document.querySelector("#plus");
const decrease = document.querySelector("#minus");

increase.addEventListener("click", () => addition(true) );
decrease.addEventListener("click", () => addition(false) );

let sizeFont = 20;
text.style.fontSize = `${sizeFont}px`;

const addition = (add) => {
  output.innerText = text.value;
  if (add) {
    sizeFont += 2;
  } else {
    sizeFont -= 2;
  }
  output.style.fontSize = `${sizeFont}px`;
};
```
</details>

<!-- Question 3 -->


<details>
  <summary>
   3. Create a web app where I can input a text. Now, create three buttons h1, h2, h3. When I click on any of the button, the text should become h1, h2, or h3.
  </summary>
    
- `index.html`
```html     
    <label for="input">
        Enter Name :  <input type="text" id="input" />
    </label>
    <p id="output"></p>
    <button id="h1"> H1 </button>
    <button id="h2"> H2 </button>
    <button id="h3"> H3 </button>

```
    
- `index.js`
```javascript
const inputEl = document.querySelector("#input");
const outputEl = document.querySelector("#output");
const h1 = document.querySelector("#h1");
const h2 = document.querySelector("#h2");
const h3 = document.querySelector("#h3");

const change = (a) => {
  outputEl.outerHTML = `<${a}>` + inputEl.value + `<${a}/>`;
};

h1.addEventListener("click", () => change("h1") );
h2.addEventListener("click", () => change("h2") );
h3.addEventListener("click", () => change("h3") );
```
</details>

<!-- Question 4 -->

<details>
  <summary>
   4. Create a web app where I can input a text. Now, create three buttons: red, green, blue. Clicking on the button should change the text color.
  </summary>
    
- `index.html`
```html     
    <label for="input">
        Enter Name :  <input type="text" id="input" />
    </label>
    <p id="output"></p>
    <button id="red"> Red </button>
    <button id="green"> Green </button>
    <button id="blue"> Blue </button>

```
    
- `index.js`
```javascript
const inputEl = document.querySelector("#input");
const outputEl = document.querySelector("#output");
const red = document.querySelector("#red");
const green = document.querySelector("#green");
const blue = document.querySelector("#blue");

const colorChange = (colour) => {
  outputEl.innerText = inputEl.value;

  outputEl.style.color =
    colour === red ? "red" : colour === green ? "green" : "blue";
};

red.addEventListener("click", () => colorChange(red) );
green.addEventListener("click", () => colorChange(green) );
blue.addEventListener("click", () => colorChange(blue) );
```
</details>

<!-- Question 5 -->


 <details>
  <summary> 
    5. Create a CLI app which takes name, unit test marks, pre final marks, final marks of 5 students. And then print who has the highest marks. What if I ask you to print the average as well?
  </summary>
    
- `index.js`
```javascript

const readline = require('readline-sync')

const data = [];
let maximumMarks = 0;
let firstRank;

for (let i = 0; i < 5; i++) {
  const userName = readline.question("what's ypur name ");
  const unitTestMarks = Number(readline.question("Enter your unit marks "));
  const preFinalMarks = Number(readline.question("Enter your pre final marks "));
  const finalMarks = Number(readline.question("Enter your final marks "));
  const totalMarks = unitTestMarks + preFinalMarks + finalMarks;
  console.log("------------")
  
  data.push({ userName, unitTestMarks, preFinalMarks, finalMarks, totalMarks });

}

for (let i = 0; i < data.length; i++) {
  if (data[i].totalMarks > maximumMarks) {
    maximumMarks = data[i].totalMarks;
    firstRank = data[i].userName;
  }
}

let average = 0;
for (let i = 0; i < data.length; i++) {
  average += data[i].totalMarks;
}
average /= data.length;

console.log(firstRank + " has git the first Rank and Highest total mark is : " + maximumMarks + " and the average marks is " + average);

```
</details>

<!-- Question 6 -->


<details>
  <summary>
   6. Create a web app with a button loaded. Show a text `loading...` on a web app. However, hide it if I click on the button loaded.
  </summary>
    
- `index.html`
```html     
<p id="text"> </p>
<button id="loading"> Loading </button>

```
    
- `index.js`
```javascript
const text = document.querySelector("#text");
const loadingBtn = document.querySelector("#loading");

loadingBtn.addEventListener("click", () => text.style.display = "none")
```
</details>

<!-- Question 7 -->

<details>
  <summary>
   7. Here's an API. Create a web app to call this API with your full name and print the response. This could be extended where we ask you to do something with the response. Like add a text, or capitalise etc.
  </summary>
    
- `index.js`
```javascript
let name = "Sanyam Jain";
const url = "https://sanyamapi.sanyam04.repl.co/"
const constructUrl = url + "name" + "?" + "text=" + name; 

fetch(constructUrl)
.then(res => res.json())
.then(data => document.write(data.contents.text));
```
</details>

<!-- Question 8 -->

<details>
  <summary>
   8. Here's an API. It will give an error. Write a web app, call this API and read the error message. Show user the error message.
  </summary>
    
- `index.html`
```html     


```
    
- `index.js`
```javascript

```
</details>

<!-- Question 9 -->

<details>
  <summary>
   9. Here's an API, it can give two errors. Either 404, or 401. If the error is 404, show the user `'page not found'` and if the error is 401, show the user `'you are not logged in'`.
  </summary>
    
- `index.js`
```javascript
const url = "https://mystery-api.kushanksriraj.repl.co/get";  // this url dont work yo can see only one response

fetch(url).then((resp) => {
    if (resp.status = 404) {
        document.write("page not found")
    } else if (resp.status = 401) {
        document.write(" You are not logged in")
    }

});


```
</details>

<!-- Question 10 -->

<details>
  <summary>
   10. Open your Github repo. Make a small change. And create a PR. Explain what you understand by Git, what's PR etc.
  </summary>
    
```
Git is a popular version control system.
 Version control, also known as source control, is the practice of tracking and managing changes to software code. 

It is used for:

- Tracking code changes
- Tracking who made changes
- Coding collaboration
-------------

Pull requests let you tell others about changes you've pushed to a branch in a repository on GitHub. Once a pull request is opened,
you can discuss and review the potential changes with collaborators and add follow-up commits before your changes are merged 
into the base branch.

```
</details>

<!-- Question 11 -->

<details>
  <summary>
   11. Create a password checker web app. If password is lesser than 10 characters then show an error to user otherwise show success. 
Someone can ask to make the submit button disabled. Some can ask to make the input field green or red depending on input.
  </summary>
    
- `index.html`
```html     
<label for="num1">
  Password: <input type="password" id="num1" />
</label>
<label for="num2">
  Confirm Password: <input type="password" id="num2" />
</label>
<p id="error"></p>
<button disabled="true" id="btn"> submit</button>

```
    
- `index.js`
```javascript

const pass1 = document.querySelector("#num1");
const pass2 = document.querySelector("#num2");
const error = document.querySelector("#error");
const btn = document.querySelector("#btn");

const onCheck1 = () => {
  if (pass1.value.length < 10) {
    error.innerText = " you have to enter at least 10 digit!";
    pass1.style.outlineColor = "#ff6666";
    pass1.style.backgroundColor = "#ff666621";
  } else {
    error.innerText = "";
    pass1.style.backgroundColor = "#fff";
    pass1.style.outlineColor = "#66cc66";
  }
};

const onCheck2 = () => {
  if (pass1.value != pass2.value) {
    pass2.style.outlineColor = "#ff6666";
    pass2.style.backgroundColor = "#ff666621";
    error.innerText = "passwords don't match";
    btn.disabled = true
  } else {
    pass2.style.outlineColor = "#66cc66";
    pass2.style.backgroundColor = "#fff";
    error.innerText = "";
    btn.disabled = false
  }
};

pass1.addEventListener("keyup", () => onCheck1());
pass2.addEventListener("keyup", () => onCheck2());
```
</details>

<!-- Question 12 -->


<details>
  <summary>
   12. Show me your portfolio. Okay, I like the button you have made. Can you re create the button without looking at source code? You're free to Google though. 
  </summary>
    

</details>

<!-- Question 13 -->


<details>
  <summary>
   13. Create color variables in CSS. Two colors: primary and secondary. Now make your h1 of primary color, h2 of secondary color. Make two buttons, primary and secondary using the same color. Can you also set a font from Google Font?
  </summary>
    
- `index.html`
```html     
<h1> Hello </h1>
<h2> Devlopers </h2>
<button id="btn1"> Circle </button>
<button id="btn2" > Star </button>



```
    
- `index.css`
```css
@import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');

:root {
  --primary: #1e90ff;
  --secondary: #ff45fff; 
}

h1 {
  color : var(--primary);
  font-family: 'Poppins', sans-serif;
}

h2 {
  color : var(--secondary);
  font-family: 'Poppins', sans-serif;
}

#btn1 {
  background-color : var(--primary);
}

#btn1 {
  background-color : var(--secondary);
}

```
</details>

<!-- Question 14 -->


<details>
  <summary>
   14. Create two objects with name, age, and yuga as `Ram, 25, Treta. Krishna, 31, Dwapar`. 
Write a function which takes two objects and return the person with more age.
  </summary>
        
- `index.js`
```javascript
const object1 = {
  name: "Ram",
  age: 25,
  yuga: "Treta"
}

const object2 = {
  name: "Krishna",
  age: 23,
  yuga: "Dwapar"
}


const powerful = (obj1, obj2) => {

  if (obj1.age > obj2.age) console.log(obj1.name + " is elder.")
  else console.log(obj2.name + " is elder.")

}

powerful(object1, object2);  // Ram is elder.
```
</details>

<!-- Question 15 -->

<details>
  <summary>
   15. Create two objects with name, power, and yuga as Ram, 2500, Treta. Krishna, 2325, Dwapar. Write a function which takes two objects and return the person with more `power`. 
  </summary>
    
- `index.js`
```javascript

const object1 = {
  name: "Ram",
  power: 2500,
  yuga: "Treta"
}

const object2 = {
  name: "Krishna",
  power: 2325,
  yuga: "Dwapar"
}


const powerful = (obj1, obj2) => {

  const powerPoints1 = obj1.power;
  const powerPoints2 = obj2.power;

  if (powerPoints1 > powerPoints2) console.log(obj1.name + " is more powerful with " + powerPoints1 + " points")
  else console.log(obj2.name + " is more powerful with " + powerPoints2 + " points")

}

powerful(object1, object2); // Ram is more powerful with 2500 points
```
</details>

<!-- Question 16 -->

<details>
  <summary>
   16. Create two objects with name, power, and yuga as Ram, 2500, Treta. Krishna, 2325, Dwapar. 
Say if every character in name is worth 35 power points.
Write a function which takes two objects and return the person with more power based on their name and power both.
  </summary>
        
- `index.js`
```javascript

const object1 = {
  name: "Ram",
  power: 2500,
  yuga: "Treta"
}

const object2 = {
  name: "Krishna",
  power: 2325,
  yuga: "Dwapar"
}


const powerful = (obj1, obj2) => {

  const namePoints1 = obj1.name.length * 35 + obj1.power;
  const namePoints2 = obj2.name.length * 35 + obj2.power;

  if (namePoints1 > namePoints2) console.log(obj1.name + " is more powerful with " + namePoints1 + " points")
  else console.log(obj2.name + " is more powerful with " + namePoints2 + " points")

}

powerful(object1, object2);   // Ram is more powerful with 2605 points
```
</details>

<!-- Question 17 -->

<details>
  <summary>
   17. Create a CLI app which would detect fake news. This app will take news as input and then source. If source is Facebook or whatsapp then it will output user saying, `"Don't believe things on FB and Whatsapp"`. Can you extend this to include telegram as well?
  </summary>
    
    
- `index.js`
```javascript
const readline = require('readline-sync');

const input = readline.question('Enter News : ');
const source = readline.question('Enter Source : ').toLowerCase();

if (source == "facebook" || source == "whatsapp" || source == "telegram") {
  console.log("Don't believe things on FB , telegram and Whatsapp");
}
```
</details>








