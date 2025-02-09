<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Number Addition Calculator</title>
     <link rel="stylesheet" href="style.css">
<body>
    <div class="container">
        <div class="title">Number Addition</div>
       
        <div class="input-group">
            <label for="num1">First Number:</label>
            <input type="text" id="num1">
        </div>
       
        <div class="input-group">
            <label for="num2">Second Number:</label>
            <input type="text" id="num2">
        </div>
       
        <div class="input-group">
            <label for="result">Result:</label>
            <input type="text" id="result" readonly>
        </div>

        <div class="button-group">
            <button id="clearBtn">Clear</button>
            <button id="addBtn">Add</button>
            <button id="exitBtn">Exit</button>
        </div>
    </div>

    <script src = "assignjava.js"></script>
</body>
</html>

    document.getElementById('addBtn').addEventListener('click', function() {
    const num1 = parseFloat(document.getElementById('num1').value) || 0;
    const num2 = parseFloat(document.getElementById('num2').value) || 0;
    const result = num1 + num2;
    document.getElementById('result').value = result;
});

// Clear button functionality
document.getElementById('clearBtn').addEventListener('click', function() {
    document.getElementById('num1').value = '';
    document.getElementById('num2').value = '';
    document.getElementById('result').value = '';
});

// Exit button functionality
document.getElementById('exitBtn').addEventListener('click', function() {
    // Note: window.close() typically only works for windows opened by scripts
    try {
        window.close();
    } catch (e) {
        alert('Exit button clicked - this would close the window in a desktop application');
    }
});

body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
  background-color: #f0f0f0;
}

.container {
  border: 1px solid #ccc;
  border-radius: 4px;
  padding: 20px;
  background-color: white;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

.title {
  font-size: 18px;
  font-weight: bold;
  margin-bottom: 15px;
  color: #333;
}

.input-group {
  display: flex;
  align-items: center;
  margin-bottom: 10px;
}

.input-group label {
  width: 120px;
  text-align: right;
  margin-right: 10px;
}

input[type="text"] {
  width: 150px;
  padding: 4px;
  border: 1px solid #ccc;
  border-radius: 3px;
}

.button-group {
  margin-top: 15px;
  display: flex;
  gap: 10px;
  justify-content: flex-end;
}

button {
  padding: 6px 12px;
  border: 1px solid #ccc;
  border-radius: 3px;
  background-color: #f8f8f8;
  cursor: pointer;
}

button:hover {
  background-color: #e8e8e8;
}

