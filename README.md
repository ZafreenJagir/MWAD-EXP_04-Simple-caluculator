# MWAD-EXP_04-Simple-caluculator
## Date: 21-09-2025
###### Name : Zafreen J
###### Register Number : 212223040252

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

.css
```
body {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background: #f4f4f4;
  margin: 0;
  font-family: Arial, sans-serif;
}

.calculator {
  background: #222;
  padding: 20px;
  border-radius: 10px;
  width: 260px;
  box-shadow: 0 4px 10px rgba(0,0,0,0.3);
}

.display {
  background: #000;
  color: #0f0;
  font-size: 2rem;
  text-align: right;
  padding: 15px;
  border-radius: 5px;
  margin-bottom: 10px;
  overflow-x: auto;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

button {
  padding: 20px;
  font-size: 1.2rem;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  background: #444;
  color: #fff;
  transition: 0.2s;
}

button:hover {
  background: #666;
}

button.clear {
  background: #d9534f;
  grid-column: span 2; 
}

button.equals {
  background: #5cb85c;
  grid-column: span 2; 
}

button.zero {
  grid-column: span 2; 

}

```



.jsx
```
import React, { useState } from "react";
import "./App.css";

function App() {
  const [input, setInput] = useState("");

  const handleClick = (value) => {
    setInput((prev) => prev + value);
  };

  const handleClear = () => {
    setInput("");
  };

  const handleCalculate = () => {
    try {
      setInput(eval(input).toString()); // quick solution for demo
    } catch {
      setInput("Error");
    }
  };

  return (
    <div className="calculator">
      <div className="display">{input || "0"}</div>
      <div className="buttons">
        <button onClick={handleClear} className="clear">C</button>
        <button onClick={() => handleClick("/")}>/</button>
        <button onClick={() => handleClick("*")}>*</button>

        <button onClick={() => handleClick("7")}>7</button>
        <button onClick={() => handleClick("8")}>8</button>
        <button onClick={() => handleClick("9")}>9</button>
        <button onClick={() => handleClick("-")}>-</button>

        <button onClick={() => handleClick("4")}>4</button>
        <button onClick={() => handleClick("5")}>5</button>
        <button onClick={() => handleClick("6")}>6</button>
        <button onClick={() => handleClick("+")}>+</button>

        <button onClick={() => handleClick("1")}>1</button>
        <button onClick={() => handleClick("2")}>2</button>
        <button onClick={() => handleClick("3")}>3</button>
        <button onClick={() => handleClick("%")}>%</button>
        <button onClick={handleCalculate} className="equals">=</button>

        <button onClick={() => handleClick("0")} className="zero">0</button>
        <button onClick={() => handleClick("00")} className="zero">00</button>
        <button onClick={() => handleClick(".")}>.</button>

        <button onClick={() => handleClick("^")}>^</button>
      </div>
    </div>
  );
}

export default App;


```

## OUTPUT

<img width="510" height="742" alt="Screenshot 2025-09-21 181529" src="https://github.com/user-attachments/assets/1ab022a0-b96b-4b53-af22-b0003cab1fce" />


<img width="485" height="734" alt="image" src="https://github.com/user-attachments/assets/c576c733-2d58-49b4-aa7d-c7eca28c9445" />


## RESULT
The program for developing a simple calculator in React.js is executed successfully.
