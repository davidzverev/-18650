<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Расчет стоимости батарей</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f5f5f5;
            color: #333;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        header {
            background-color: #333;
            color: #fff;
            padding: 20px;
            width: 100%;
            text-align: center;
        }
        main {
            max-width: 800px;
            width: 100%;
            padding: 20px;
        }
        .form-group {
            margin-bottom: 20px;
        }
        .form-group label {
            display: block;
            margin-bottom: 5px;
        }
        .form-group input, .form-group select {
            width: 100%;
            padding: 8px;
            box-sizing: border-box;
        }
        .form-group button {
            padding: 10px 20px;
            background-color: #333;
            color: #fff;
            border: none;
            cursor: pointer;
        }
        .result {
            margin-top: 20px;
            font-size: 18px;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <header>
        <h1>Расчет стоимости батарей</h1>
    </header>
    <main>
        <div class="form-group">
            <label for="quantity">Количество (шт):</label>
            <input type="number" id="quantity" min="1" required>
        </div>
        <div class="form-group">
            <label for="capacity">Выберите емкость (мАч):</label>
            <select id="capacity" required>
                <option value="5500">1200 мАч - 5500 р</option>
                <option value="6500">1500 мАч - 6500 р</option>
                <option value="7500">2000 мАч - 7500 р</option>
                <option value="11000">2500 мАч - 11000 р</option>
            </select>
        </div>
        <div class="form-group">
            <button type="button" onclick="calculatePrice()">Рассчитать стоимость</button>
        </div>
        <div class="result" id="result"></div>
    </main>

    <script>
        function calculatePrice() {
            const quantity = document.getElementById('quantity').value;
            const pricePer100 = document.getElementById('capacity').value;

            if (quantity && pricePer100) {
                const price = (pricePer100 / 100) * quantity;
                const totalPrice = price; // Без учета доставки

                document.getElementById('result').innerText = `Общая стоимость: ${totalPrice.toFixed(2)} р`;
            } else {
                document.getElementById('result').innerText = 'Пожалуйста, введите количество и выберите емкость.';
            }
        }
    </script>
</body>
</html>
