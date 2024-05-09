<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Israel Calculator</title>
    <style>
        /* Importing a 7-segment style font for the calculator display and buttons */
        @import url('https://fonts.googleapis.com/css2?family=Digital+7:wght@400&display=swap');

        /* Styling the calculator container with a dark background and rounded corners */
        .calculator {
            display: table;
            margin: auto;
            padding: 15px;
            background-color: #333; /* Dark gray body */
            border-radius: 10px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
        }

        /* White display screen with a 7-segment style font */
        input {
            width: 100%;
            height: 50px; /* Taller display for easier reading */
            text-align: right;
            font-size: 1.8em; /* Larger font for the display */
            font-family: 'Digital 7', monospace;
            border: 2px solid #666;
            border-radius: 5px;
            background-color: white; /* White display */
            color: black; /* Black text */
            padding: 0 15px;
            box-shadow: inset 0 2px 3px rgba(0, 0, 0, 0.1);
        }

        /* 3D-style buttons with bold digital font */
        button {
            width: 60px; /* Larger buttons */
            height: 60px; /* Larger buttons */
            font-size: 1.4em; /* Bold and easy-to-read font */
            font-family: 'Digital 7', monospace;
            font-weight: bold; /* Bold font for visibility */
            border-radius: 5px;
            border: 1px solid #ccc;
            background-color: #ddd; /* Light gray buttons */
            cursor: pointer;
            box-shadow: 0 5px #999; /* 3D effect */
            transition: all 0.1s;
        }

        /* Button pressed state for 3D effect */
        button:active {
            box-shadow: 0 2px #666; /* Pressed effect */
            transform: translateY(2px);
        }

        /* Operator button styling with bold symbols */
        button.operator {
            background-color: #ddd; /* Same as other buttons for consistency */
            border: 1px solid #bbb; /* Slightly darker border */
        }

        /* Hover effect for all buttons */
        button:hover {
            background-color: #ccc; /* Slightly darker on hover */
        }
    </style>
</head>
<body>
    <div class="calculator">
        <table>
            <tr>
                <td colspan="4"><input type="text" id="output" readonly></td>
            </tr>
            <tr>
                <td><button onclick="appendValue('7')">7</button></td>
                <td><button onclick="appendValue('8')">8</button></td>
                <td><button onclick="appendValue('9')">9</button></td>
                <td><button class="operator" onclick="appendValue('÷')">÷</button></td>
            </tr>
            <tr>
                <td><button onclick="appendValue('4')">4</button></td>
                <td><button onclick="appendValue('5')">5</button></td>
                <td><button onclick="appendValue('6')">6</button></td>
                <td><button class="operator" onclick="appendValue('×')">×</button></td>
            </tr>
            <tr>
                <td><button onclick="appendValue('1')">1</button></td>
                <td><button onclick="appendValue('2')">2</button></td>
                <td><button onclick="appendValue('3')">3</button></td>
                <td><button class="operator" onclick="appendValue('-')">-</button></td>
            </tr>
            <tr>
                <td><button onclick="appendValue('.')">.</button></td>
                <td><button onclick="appendValue('0')">0</button></td>
                <td><button class="operator" onclick="calculate()">=</button></td>
                <td><button class="operator" onclick="appendValue('+')">+</button></td>
            </tr>
        </table>
    </div>

    <script>
        function appendValue(value) {
            var output = document.getElementById("output");
            output.value += value; /* Appending values to the display */
        }

        function calculate() {
            var output = document.getElementById("output");
            try {
                var expression = output.value.replace('×', '*').replace('÷', '/'); /* Replacing custom operators with JS operators */
                output.value = eval(expression); /* Evaluate the expression */
            } catch (e) {
                output.value = "Error"; /* Error handling */
            }
        }
    </script>
</body>
</html>
