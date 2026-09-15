# Ex04 Simple Calculator - React Project
## Date:15-09-2026
## Name : MAHALAKSSHMI MRIDULA 


## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
### STEP 1
Create a React App.

### STEP 2
Open a terminal and run:
  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

### STEP 5
Create a new file Calculator.css in src/ and add the styling.

### STEP 6
Open src/App.js and modify it.

### STEP 7
Start the development server.
  npm start

### STEP 8
Open http://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM

## app.jsx
```
import { useState } from "react";
import "./App.css";

export default function App() {
  const [input, setInput] = useState("");

  const handleClick = (value) => {
    setInput(input + value);
  };

  const clear = () => setInput("");

  const calculate = () => {
    try {
      setInput(eval(input).toString());
    } catch {
      setInput("Error");
    }
  };

  return (
    <div className="container">
      <div className="calculator">
        <h2>Simple Calculator</h2>

        <input type="text" value={input} readOnly className="display" />

        <div className="buttons">
          <button onClick={clear}>C</button>
          <button onClick={() => handleClick("/")}>/</button>
          <button onClick={() => handleClick("*")}>×</button>
          <button onClick={() => handleClick("-")}>−</button>

          <button onClick={() => handleClick("7")}>7</button>
          <button onClick={() => handleClick("8")}>8</button>
          <button onClick={() => handleClick("9")}>9</button>
          <button onClick={() => handleClick("+")}>+</button>

          <button onClick={() => handleClick("4")}>4</button>
          <button onClick={() => handleClick("5")}>5</button>
          <button onClick={() => handleClick("6")}>6</button>
          <button onClick={calculate} className="equal">=</button>

          <button onClick={() => handleClick("1")}>1</button>
          <button onClick={() => handleClick("2")}>2</button>
          <button onClick={() => handleClick("3")}>3</button>
          <button onClick={() => handleClick("0")} className="zero">0</button>

          <button onClick={() => handleClick(".")}>.</button>
        </div>
      </div>

      <footer>
        <p>Name: SUBIKSHA K</p>
        <p>Register No: 212224040332</p>
      </footer>
    </div>
  );
}
```

## app.css

```
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Arial, sans-serif;
}

body {
  background: linear-gradient(135deg, #4facfe, #00f2fe);
}

.container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
}

.calculator {
  background: white;
  padding: 20px;
  border-radius: 15px;
  box-shadow: 0 8px 20px rgba(0,0,0,0.2);
  width: 320px;
}

h2 {
  text-align: center;
  margin-bottom: 15px;
}

.display {
  width: 100%;
  height: 55px;
  font-size: 22px;
  text-align: right;
  padding: 10px;
  margin-bottom: 15px;
  border: 2px solid #ddd;
  border-radius: 8px;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

button {
  padding: 15px;
  font-size: 18px;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  background: #e3e3e3;
  transition: 0.2s;
}

button:hover {
  background: #cfcfcf;
}

.equal {
  grid-row: span 2;
  background: #4caf50;
  color: white;
}

.zero {
  grid-column: span 2;
}

footer {
  margin-top: 20px;
  color: white;
  text-align: center;
  font-weight: bold;
}
```
## index.html
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>React Calculator</title>
  </head>
  <body>
    <div id="root"></div>
    <script type="module" src="/src/main.jsx"></script>
  </body>
</html>
```


## OUTPUT

<img width="1914" height="1148" alt="Screenshot 2026-08-22 135754" src="https://github.com/user-attachments/assets/639826f9-a16f-47fe-9f69-0b8fb8c2eda6" />

## RESULT
The program for developing a simple calculator in React.js is executed successfully.
