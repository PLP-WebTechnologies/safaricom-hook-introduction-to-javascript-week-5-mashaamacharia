### **Assignment: Exploring JavaScript Fundamentals and DOM Manipulation** 🌟

---

#### **Objective:**
This assignment aims to test your understanding of JavaScript basics, control structures, and the Document Object Model (DOM). You will demonstrate your skills by creating an interactive webpage that uses variables, data types, operators, control structures, and DOM manipulation.

---

### **Instructions:**

1. **Create a new HTML file** and include an external JavaScript file for your script.  
2. Name your HTML file as `assignment.html` and your JavaScript file as `script.js`.  
3. Follow the tasks below and ensure you structure your code for readability with proper comments.  

---

### **Tasks:**

#### **Part 1: JavaScript Basics**

1. **Variables and Data Types**:
   - Declare variables of different types: string, number, boolean, array, and object.  
   - Use `console.log()` to print their values and types in the browser console.  

   **Example Output**:  
   ```
   Name: John Doe (Type: string)  
   Age: 25 (Type: number)  
   Is student: true (Type: boolean)

   // String
let name = "John Doe";
console.log(`Name: ${name} (Type: ${typeof name})`);

// Number
let age = 25;
console.log(`Age: ${age} (Type: ${typeof age})`);

// Boolean
let isStudent = true;
console.log(`Is student: ${isStudent} (Type: ${typeof isStudent})`);

// Array
let hobbies = ["Reading", "Cycling", "Hiking"];
console.log(`Hobbies: ${hobbies} (Type: ${typeof hobbies})`);

// Object
let person = {
  name: "Jane Smith",
  age: 30,
  isStudent: false
};
console.log(`Person: ${JSON.stringify(person)} (Type: ${typeof person})`);

   ```

2. **Operators**:
   - Write a simple calculator function that performs addition, subtraction, multiplication, and division using two numbers provided by the user (use `prompt()` for input).  
   - Use arithmetic and comparison operators to validate user input and display appropriate messages.

   **Example Output**:  
   ```
   Enter the first number: 10  
   Enter the second number: 2  
   Choose an operation (+, -, *, /): *  
   Result: 20
   ```
function calculator() {
  let num1 = parseFloat(prompt("Enter the first number:"));
  let num2 = parseFloat(prompt("Enter the second number:"));
  let operation = prompt("Choose an operation (+, -, *, /):");

  if (isNaN(num1) || isNaN(num2)) {
    alert("Invalid input. Please enter valid numbers.");
    return;
  }

  let result;
  switch (operation) {
    case "+":
      result = num1 + num2;
      break;
    case "-":
      result = num1 - num2;
      break;
    case "*":
      result = num1 * num2;
      break;
    case "/":
      if (num2 === 0) {
        alert("Division by zero is not allowed.");
        return;
      }
      result = num1 / num2;
      break;
    default:
      alert("Invalid operation. Please choose +, -, *, or /.");
      return;
  }

  alert(`Result: ${result}`);
}

calculator();


3. **Functions**:
   - Create a function named `greetUser` that takes a name as a parameter and returns a greeting message. Display the message in an HTML element.  

---
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Greet User</title>
</head>
<body>
  <div id="greeting"></div>

  <script>
    function greetUser(name) {
      return `Hello, ${name}! Welcome to our website.`;
    }

    let userName = prompt("Enter your name:");
    let message = greetUser(userName);
    document.getElementById("greeting").innerText = message;
  </script>
</body>
</html>


#### **Part 2: JavaScript Control Structures**

4. **If Statements**:
   - Ask the user for their age using `prompt()`. Use an `if` statement to check if they are eligible to vote (age >= 18). Display a message indicating their eligibility in an HTML element.
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Voting Eligibility</title>
</head>
<body>
  <div id="eligibility"></div>

  <script>
    let age = parseInt(prompt("Enter your age:"));

    if (isNaN(age)) {
      document.getElementById("eligibility").innerText = "Invalid input. Please enter a valid age.";
    } else if (age >= 18) {
      document.getElementById("eligibility").innerText = "You are eligible to vote.";
    } else {
      document.getElementById("eligibility").innerText = "You are not eligible to vote yet.";
    }
  </script>
</body>
</html>


5. **Loops**:
   - Write a loop to display numbers from 1 to 10 on the webpage. Use an ordered list (`<ol>`) to present the numbers.  

---
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Number List</title>
</head>
<body>
  <ol id="number-list"></ol>

  <script>
    let list = document.getElementById("number-list");

    for (let i = 1; i <= 10; i++) {
      let listItem = document.createElement("li");
      listItem.innerText = i;
      list.appendChild(listItem);
    }
  </script>
</body>
</html>

#### **Part 3: Introduction to the DOM**

6. **Creating HTML Structure**:
   - Add the following HTML elements to your webpage:
     - A heading (`<h1>`) with the text **"JavaScript Assignment"**.  
     - A paragraph (`<p>`) with the text **"Learning JavaScript is fun!"**.  
     - A `<div>` with an `id` of `dynamic-content`.  
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>JavaScript Assignment</title>
</head>
<body>
  <h1>JavaScript Assignment</h1>
  <p>Learning JavaScript is fun!</p>
  <div id="dynamic-content"></div>
</body>
</html>

7. **Selecting and Modifying HTML Elements**:
   - Use JavaScript to:
     - Change the text of the `<h1>` element to **"JavaScript in Action!"**.  
     - Add a new `<p>` inside the `dynamic-content` `<div>` with the text **"This content was added dynamically using JavaScript."**.  

---<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>JavaScript in Action!</title>
</head>
<body>
 


### **Tips for Success:**

- Test your code frequently to catch errors early.  
- Use meaningful variable names and add comments to explain your logic.  
- Have fun and get creative!  

Happy Coding! 💻✨  
