# Objects and Oops

## Q 01


<!-- Question 1 -->

 <details>

  <summary>
      Given an array of objects of student's marks:

-   Print the name and total marks of each student.
-   Print the name of student whose total marks is highest.
-   Print the name of student whose total marks is lowest.
-   Print the average marks of the class in computer subject.
-   Print the grades of all students:  
     Grade A if total marks is higher than or equal to 75%,  
     Grade B if higher than or equal to 60%,  
     Grade C if higher than or equal to 35%,  
     Grade D if lower than 35%.
-   Print the total number of students passed and their names. Pass when total marks is greater than 35%.

```js script
const studentDetails = [
	{
		roll: "1",
		name: "Rohan Singh",
		maths: 86,
		science: 90,
		english: 75,
		computer: 85
	},
	{
		roll: "2",
		name: "Ritvik Patel",
		maths: 27,
		science: 30,
		english: 35,
		computer: 30
	},
	{
		roll: "3",
		name: "Neha Maurya",
		maths: 75,
		science: 69,
		english: 40,
		computer: 75
	},
	{
		roll: "4",
		name: "Mohit Verma",
		maths: 21,
		science: 31,
		english: 45,
		computer: 40
	},
	{
		roll: "5",
		name: "Karan Trivedi",
		maths: 70,
		science: 80,
		english: 35,
		computer: 60
	}
];
```

  </summary>


-  `index.js`

```javascript

const studentDetails = [
  {
    roll: "1",
    name: "Rohan Singh",
    maths: 86,
    science: 90,
    english: 75,
    computer: 85
  },
  {
    roll: "2",
    name: "Ritvik Patel",
    maths: 27,
    science: 30,
    english: 35,
    computer: 30
  },
  {
    roll: "3",
    name: "Neha Maurya",
    maths: 75,
    science: 69,
    english: 40,
    computer: 75
  },
  {
    roll: "4",
    name: "Mohit Verma",
    maths: 21,
    science: 31,
    english: 45,
    computer: 40
  },
  {
    roll: "5",
    name: "Karan Trivedi",
    maths: 70,
    science: 80,
    english: 35,
    computer: 60
  }
];

const studentTotalMarks = [];
const passList = [];

const prinitDetails = (students) => {
  for (let i = 0; i < students.length; i++) {
    totalMarks = students[i].english + students[i].computer + students[i].maths + students[i].science;
    studentTotalMarks.push(totalMarks)
    const grade = getGrades(totalMarks, students[i].name);
    console.log("Name: " + students[i].name);
    console.log("Total Marks: " + totalMarks);
    console.log("Grade: " + grade);
    console.log("---------")
  }
}

const highestMarks = (data) => {
  let highestMarks = data[0];
  let topper = studentDetails[0].name;
  for (let i = 1; i < data.length; i++) {
    if (data[i] > highestMarks) {
      highestMarks = data[i];
      topper = studentDetails[i].name;
    }
  }
  console.log("Highest Marks: " + topper);
}

const lowestMarks = (data) => {
  let lowestMarks = data[0];
  let name = studentDetails[0].name;
  for (let i = 1; i < data.length; i++) {
    if (data[i] < lowestMarks) {
      lowestMarks = data[i];
      name = studentDetails[i].name;
    }
  }
  console.log("Lowest Marks: " + name);
}

const averageMarksInComputer = (data) => {
  let totalMarksInSubject = 0;
  for (let i = 0; i < data.length; i++) {
    totalMarksInSubject += data[i].computer;
  }
  averageMarks = totalMarksInSubject / data.length;
  console.log("Average Marks in computer: " + averageMarks)
}

const getGrades = (marks, name) => {
  const percentage = marks / 400 * 100;
  if (percentage >= 75) {
    passList.push(name);
    return "A";
  }
  else if (percentage >= 60) {
    passList.push(name);
    return "B";
  }
  else if (percentage >= 35) {
    passList.push(name);
    return "C";
  }
  else return "D";

}

const passFail = () => {
  console.log("Number of Students Pass: " + passList.length);
  console.log("Name of Pass students: ");
  for (let i = 0; i < passList.length; i++) {
    console.log("  " + passList[i]);
  }

}

prinitDetails(studentDetails);
highestMarks(studentTotalMarks);
lowestMarks(studentTotalMarks);
averageMarksInComputer(studentDetails);
passFail();
 

// Name: Rohan Singh
// Total Marks: 336
// Grade: A
// ---------
// Name: Ritvik Patel
// Total Marks: 122
// Grade: D
// ---------
// Name: Neha Maurya
// Total Marks: 259
// Grade: B
// ---------
// Name: Mohit Verma
// Total Marks: 137
// Grade: D
// ---------
// Name: Karan Trivedi
// Total Marks: 245
// Grade: B
// ---------
// Highest Marks: Rohan Singh
// Lowest Marks: Ritvik Patel
// Average Marks in computer: 58
// Number of Students Pass: 3
// Name of Pass students: 
//   Rohan Singh
//   Neha Maurya
//   Karan Trivedi
```

</details>

## Q 02


<!-- Question 2 -->

 <details>

  <summary>
      Salary calculation using OOPS concept.

-   Create a Class using ES6 in JavaScript named Employee and assign necessary  
    data members and methods such as name, id, basic salary, HRA, Allowances; define getSalary method which will return the net salary.
-   Create two Instances of Employee with all necessary details.
-   Call the getSalary method of each instance and return the net salary based on your computation.

  </summary>


-  `index.js`

```javascript
      (add javacript code here if needed)	  

```

</details>

## Q 03


<!-- Question 3 -->

 <details>

  <summary>
      Bank Account (Object Oriented Programming in JavaScript)

-   Create a class and define data members such as name, bank account number,  
    account balance, account type, ifsc and name it as BankAccount.
-   Create three Instances(three customers) of BankAccount with all necessary details.
-   Print the name of customers and their account balances.
-   Calculate the average account balance from all the instances.
  </summary>


-  `index.js`

```javascript
      (add javacript code here if needed)	  

```

</details>

## Q 04
<!-- Question 4 -->

 <details>

  <summary>
      Given an array of objects of items in cart, print:

-   the total No. of items
-   the total cart value
-   the total discounted value(sum of dicounted values on each item) based on the given discount
-   total tax amount (18% tax, calculated on total cart value)

```js script
const cartItems = [
	{
		id: "101",
		name: "Oreo",
		count: 2,
		price: 30.0,
		discount: 0.18
	},
	{
		id: "102",
		name: "Red Bull",
		count: 1,
		price: 99.0,
		discount: 0.15
	},
	{
		id: "103",
		name: "Dairy Milk Silk",
		count: 3,
		price: 175.0,
		discount: 0.05
	},
	{
		id: "104",
		name: "Pulse Candy Pack",
		count: 1,
		price: 135.0,
		discount: 0.2
	}
];
```
  </summary>


-  `index.js`

```javascript

const cartItems = [
  {
    id: "101",
    name: "Oreo",
    count: 2,
    price: 30.0,
    discount: 0.18
  },
  {
    id: "102",
    name: "Red Bull",
    count: 1,
    price: 99.0,
    discount: 0.15
  },
  {
    id: "103",
    name: "Dairy Milk Silk",
    count: 3,
    price: 175.0,
    discount: 0.05
  },
  {
    id: "104",
    name: "Pulse Candy Pack",
    count: 1,
    price: 135.0,
    discount: 0.2
  }
];

const totalCartItems = (cart) => {
  let totalItems = 0;
  for (let i = 0; i < cart.length; i++) {
    totalItems += cart[i].count;
  }
  return totalItems;
}

const totalCartValue = (cart) => {
  let totalValue = 0;
  for (let i = 0; i < cart.length; i++) {
    totalValue += cart[i].price;
  }
  return totalValue;
}

const discountedValue = (data) => {
  let totalDiscount = 0;
  for (let i = 0; i < data.length; i++) {
    totalDiscount += data[i].count * (data[i].price * data[i].discount).toFixed(2);
  }
  return totalDiscount;
  console.log("Total Discounted Value: " + totalDiscount);
}

const totalTaxAmount = () => {
  return totalCartValue(cartItems) - discountedValue(cartItems);
}

console.log("Total No. of Items in Cart: " + totalCartItems(cartItems));
console.log("Total Value of Items in Cart: " + totalCartValue(cartItems));
console.log("Total Discounted Value: " + discountedValue(cartItems));
console.log("Total Discounted Value: " + totalTaxAmount());

// Total No. of Items in Cart: 7
// Total Value of Items in Cart: 439
// Total Discounted Value: 78.9
// Total Discounted Value: 360.1	  

```

</details>
