<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rekenmachine</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }
        .calculator {
            width: 300px;
            margin: 0 auto;
            padding: 20px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        .calculator input[type="text"] {
            width: 100%;
            margin-bottom: 10px;
            padding: 10px;
            font-size: 18px;
        }
        .calculator input[type="button"] {
            width: 48%;
            padding: 10px;
            font-size: 18px;
            margin-bottom: 5px;
            cursor: pointer;
        }
        .calculator input[type="button"]:last-child {
            margin-left: 2%;
        }
    </style>
</head>
<body>

<div class="calculator">
    <input type="text" id="display" disabled>
    <input type="button" value="7" onclick="appendToDisplay('7')">
    <input type="button" value="8" onclick="appendToDisplay('8')">
    <input type="button" value="9" onclick="appendToDisplay('9')">
    <input type="button" value="+" onclick="appendToDisplay('+')">
    <br>
    <input type="button" value="4" onclick="appendToDisplay('4')">
    <input type="button" value="5" onclick="appendToDisplay('5')">
    <input type="button" value="6" onclick="appendToDisplay('6')">
    <input type="button" value="-" onclick="appendToDisplay('-')">
    <br>
    <input type="button" value="1" onclick="appendToDisplay('1')">
    <input type="button" value="2" onclick="appendToDisplay('2')">
    <input type="button" value="3" onclick="appendToDisplay('3')">
    <input type="button" value="*" onclick="appendToDisplay('*')">
    <br>
    <input type="button" value="C" onclick="clearDisplay()">
    <input type="button" value="0" onclick="appendToDisplay('0')">
    <input type="button" value="=" onclick="calculate()">
    <input type="button" value="/" onclick="appendToDisplay('/')">
</div>

<script>
    function appendToDisplay(value) {
        document.getElementById("display").value += value;
    }

    function clearDisplay() {
        document.getElementById("display").value = "";
    }

    function calculate() {
        var expression = document.getElementById("display").value;
        var result = eval(expression);
        document.getElementById("display").value = result;
    }
</script>

</body>
</html>
