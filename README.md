# calculator_project
//The calculator is a web-based tool built using HTML, CSS, and JavaScript. It allows users to perform basic arithmetic operations like addition, subtraction, multiplication, and division by inputting numbers and //clicking corresponding buttons. The display field shows both the input and the result of the calculations.
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Simple Calculator</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="calculator">
    <input type="text" id="display" readonly>
    <div class="keys">
      <button onclick="clearDisplay()">C</button>
      <button onclick="appendToDisplay('7')">7</button>
      <button onclick="appendToDisplay('8')">8</button>
      <button onclick="appendToDisplay('9')">9</button>
      <button onclick="appendToDisplay('+')">+</button>
      <button onclick="appendToDisplay('4')">4</button>
      <button onclick="appendToDisplay('5')">5</button>
      <button onclick="appendToDisplay('6')">6</button>
      <button onclick="appendToDisplay('-')">-</button>
      <button onclick="appendToDisplay('1')">1</button>
      <button onclick="appendToDisplay('2')">2</button>
      <button onclick="appendToDisplay('3')">3</button>
      <button onclick="appendToDisplay('*')">*</button>
      <button onclick="appendToDisplay('0')">0</button>
      <button onclick="appendToDisplay('.')">.</button>
      <button onclick="calculate()">=</button>
      <button onclick="appendToDisplay('/')">/</button>
    </div>
  </div>
  <script src="script.js"></script>
</body>
</html>
.calculator {
  width: 250px;
  margin: 50px auto;
  border: 1px solid #ccc;
  padding: 10px;
}

#display {
  width: 100%;
  margin-bottom: 10px;
  padding: 5px;
}

.keys {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-gap: 5px;
}

button {
  padding: 10px;
  font-size: 20px;
}
function clearDisplay() {
  document.getElementById('display').value = '';
}

function appendToDisplay(value) {
  document.getElementById('display').value += value;
}

function calculate() {
  var result = eval(document.getElementById('display').value);
  document.getElementById('display').value = result;
}
