<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Прайс-лист и Контакты</title>
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
        .price-list {
            width: 100%;
            border-collapse: collapse;
        }
        .price-list th, .price-list td {
            border: 1px solid #ddd;
            padding: 10px;
            text-align: left;
        }
        .price-list th {
            background-color: #333;
            color: #fff;
        }
        .contacts {
            margin-top: 20px;
        }
        .contacts p {
            margin: 5px 0;
        }
    </style>
</head>
<body>
    <header>
        <h1>Прайс-лист и Контакты</h1>
    </header>
    <main>
        <h2>Прайс-лист</h2>
        <table class="price-list">
            <thead>
                <tr>
                    <th>Комплектация</th>
                    <th>Количество</th>
                    <th>Цена</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>1200 мАч</td>
                    <td>100 шт</td>
                    <td>5500 р</td>
                </tr>
                <tr>
                    <td>1500 мАч</td>
                    <td>100 шт</td>
                    <td>6500 р</td>
                </tr>
                <tr>
                    <td>2000 мАч</td>
                    <td>100 шт</td>
                    <td>7500 р</td>
                </tr>
                <tr>
                    <td>2500 мАч</td>
                    <td>100 шт</td>
                    <td>11000 р</td>
                </tr>
            </tbody>
        </table>
        <div class="contacts">
            <h2>Контакты</h2>
            <p>Email: <a href="mailto:davidzverev@icloud.com">davidzverev@icloud.com</a></p>
            <p>WhatsApp: <a href="tel:+79781714402">+7 978 171 4402</a></p>
        </div>
    </main>
</body>
</html>
