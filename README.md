# repo1
#this is my first repo 
#<br>i am dikshakri
<!DOCTYPE html>
<html>

<head>
    <title>JavaScript Calculator</title>
    <style>
        body{
            background-color: rgb(178, 88, 28);
        }
            #calculator {
            width: 300px;
            margin: auto;
            border: 1px solid #290a70;
            border-radius: 5px;
            padding: 20px;
			background-color: rgb(212, 185, 194);
        }

        input[type="button"] {
            width: 60px;
            height: 60px;
            margin: 5px;
            font-size: 24px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
			background-color: aquamarine;
        }

        input[type="text"] {
            width: 100%;
            height: 60px;
            font-size: 24px;
            border: 1px solid #a41c2c;
            border-radius: 5px;
            text-align: right;
            padding-right: 0px;
        }
    </style>
</head>

<body>
<div id="calculator">
        <input type="text" id="result" readonly>
        <input type="button" value="1" onclick="addToDisplay('1')">
        <input type="button" value="2" onclick="addToDisplay('2')">
        <input type="button" value="3" onclick="addToDisplay('3')">
        <input type="button" value="+" onclick="addToDisplay('+')">
        <input type="button" value="4" onclick="addToDisplay('4')">
        <input type="button" value="5" onclick="addToDisplay('5')">
        <input type="button" value="6" onclick="addToDisplay('6')">
        <input type="button" value="-" onclick="addToDisplay('-')">
        <input type="button" value="7" onclick="addToDisplay('7')">
        <input type="button" value="8" onclick="addToDisplay('8')">
        <input type="button" value="9" onclick="addToDisplay('9')">
        <input type="button" value="*" onclick="addToDisplay('*')">

        <input type="button" value="C" onclick="clearDisplay()">
        <input type="button" value="0" onclick="addToDisplay('0')">
        <input type="button" value="=" onclick="calculate()">
        <input type="button" value="/" onclick="addToDisplay('/')">
    </div>

    <script>
        function addToDisplay(val) {
            document.getElementById('result').value += val;
        }
        function clearDisplay() {
            document.getElementById('result').value = '';
        }
                function calculate() {
            try {
                let result = eval(document.getElementById('result').value);
                document.getElementById('result').value = result;
            } catch (error) {
                document.getElementById('result').value = 'Error';
            }
        }
    </script>

</body>

</html>


