# Exp-02---React-Lab-Exercise-Using-Props
## NAME : Paladugu Venkata Balaji
## REG NO: 2305001024
## Aim
To create a React application that demonstrates passing data from a parent component to a child component using props.

## Objectives
1. To create a React project using Vite.
2. To understand the concept of Props in React.
3. To create a reusable Student component.
4. To pass student details such as name, department, and year using props.
5. To display multiple students using the same component.
6. To understand parent-child component communication in React.
# Program
## Step 1: Create a React Project
Open the terminal and run:
~~~
npm create vite@latest props-demo -- --template react
cd props-demo
npm install
npm run dev
~~~
Open the URL shown in the terminal.

Step 2: Understand Props
Props = Properties.

Props are used to pass data from a parent component to a child component.
~~~
Parent Component
       |
       | props
       ↓
Child Component
~~~
Example:
~~~
<Student name="Ajith" />
~~~
Here:

Student → Child component
name → Prop
"Ajith" → Prop value
Step 3: Create Student.jsx

Create a file: src/Student.jsx
~~~
function Student(props) {
  return (
    <div>
      <h2>Student Details</h2>
      <p>Name: {props.name}</p>
      <p>Department: {props.department}</p>
      <p>Year: {props.year}</p>
    </div>
  );
}
export default Student;
~~~
## Explanation
props.name gets the value of the name prop.
props.department gets the department value.
props.year gets the year value.
## Step 4: Use the Child Component
Open src/App.jsx.

Write:
~~~
import Student from "./Student";

function App() {
  return (
    <div>
      <h1>React Props Example</h1>

      <Student
        name="PALADUGU VENKATA BALAJI"
        department="CSE"
        year="IV Year"
      />
    </div>
  );
}

export default App;
~~~
Step 5: Run the Application
Run:
~~~
npm run dev
~~~
## Output
React Props Example

Student Details

Name: PALADUGU VENKATA BALAJI

Department: CSE

Year: IV Year

## Step 6: Try Multiple Students
Modify App.jsx:
~~~
import Student from "./Student";

function App() {
  return (
    <div>
      <h1>Student Information</h1>

      <Student
        name="PALADUGU VENKATA BALAJI"
        department="CSE"
        year="IV Year"
      />

      <Student
        name="BASHA"
        department="AIML"
        year="IV Year"
      />

      <Student
        name="GAGAN"
        department="AIDS"
        year="IV Year"
      />
    </div>
  );
}

export default App;
~~~
## Output
<img width="1191" height="651" alt="image" src="https://github.com/user-attachments/assets/6840ca81-2387-42ba-b274-740bac21b12a" />

## Result
Thus, a React application was successfully created and executed to demonstrate passing student information from a parent component to a child component using props.
