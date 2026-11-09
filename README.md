[exercise 1.html](https://github.com/user-attachments/files/34573347/exercise.1.html)

<!DOCTYPE html>
<html>
<head>
    <title>JS Exercise 1</title>
</head>
<body>

    <h1>JS Exercise 1</h1>

    Enter First Number:
    <input type="number" id="num1">
    <br>

    Enter Second Number:
    <input type="number" id="num2">
    <br>

    <button onclick="calculate()">Calculate</button>
    <button onclick="clearEntries()">Clear</button>

    <p>Sum: <span id="sum"></span></p>
    <p>Difference: <span id="difference"></span></p>
    <p>Product: <span id="product"></span></p>
    <p>Quotient: <span id="quotient"></span></p>

    <script>
        function calculate() {

            let num1 = document.getElementById("num1").value;
            let num2 = document.getElementById("num2").value;

            if (num1 === "" || num2 === "") {
                alert("Please enter both numbers!");
                return;
            }

            num1 = Number(num1);
            num2 = Number(num2);

            document.getElementById("sum").innerHTML = num1 + num2;

            document.getElementById("difference").innerHTML = num1 - num2;

            document.getElementById("product").innerHTML = num1 * num2;

            if (num2 === 0) {
                document.getElementById("quotient").innerHTML =
                    "Cannot divide by zero";
            } else {
                document.getElementById("quotient").innerHTML = num1 / num2;
            }
        }

        function clearEntries() {
            document.getElementById("num1").value = "";
            document.getElementById("num2").value = "";

            document.getElementById("sum").innerHTML = "";
            document.getElementById("difference").innerHTML = "";
            document.getElementById("product").innerHTML = "";
            document.getElementById("quotient").innerHTML = "";
        }
    </script>

</body>
</html>
