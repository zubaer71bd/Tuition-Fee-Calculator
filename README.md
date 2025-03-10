# Tuition-Fee-Calculator
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tuition Fee Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 50px;
        }
        .container {
            max-width: 400px;
            margin: auto;
            padding: 20px;
            border: 1px solid #ccc;
            border-radius: 10px;
            box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.1);
        }
        input, button {
            margin: 10px;
            padding: 8px;
            width: 80%;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Tuition Fee Calculator</h2>
        <label for="totalFees">Enter Total Tuition Fees:</label>
        <input type="number" id="totalFees" placeholder="Enter amount" required>
        <button onclick="calculateFees()">Calculate Installments</button>
        <h3>Installments:</h3>
        <p>1st Installment (40%): <span id="installment1">0</span></p>
        <p>2nd Installment (30%): <span id="installment2">0</span></p>
        <p>3rd Installment (30%): <span id="installment3">0</span></p>
    </div>
    <script>
        function calculateFees() {
            let totalFees = document.getElementById("totalFees").value;
            if (totalFees > 0) {
                document.getElementById("installment1").innerText = (totalFees * 0.40).toFixed(2);
                document.getElementById("installment2").innerText = (totalFees * 0.30).toFixed(2);
                document.getElementById("installment3").innerText = (totalFees * 0.30).toFixed(2);
            } else {
                alert("Please enter a valid tuition fee amount.");
            }
        }
    </script>
</body>
</html>
