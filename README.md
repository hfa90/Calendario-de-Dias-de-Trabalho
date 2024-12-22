<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora de Dias Úteis</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        .container {
            background: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            max-width: 400px;
            width: 100%;
            text-align: center;
        }

        h1 {
            font-size: 1.8rem;
            color: #333;
        }

        label {
            font-size: 1rem;
            margin: 10px 0;
            display: block;
        }

        input {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 4px;
            font-size: 1rem;
        }

        button {
            background-color: #007bff;
            color: #fff;
            border: none;
            padding: 10px 20px;
            border-radius: 4px;
            cursor: pointer;
            font-size: 1rem;
        }

        button:hover {
            background-color: #0056b3;
        }

        .result {
            margin-top: 20px;
            font-size: 1.2rem;
            color: #007bff;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Calculadora de Dias Úteis</h1>
        <label for="daily-rate">Valor da Diária (R$):</label>
        <input type="number" id="daily-rate" placeholder="Digite o valor da sua diária">

        <label for="month">Selecione o Mês:</label>
        <select id="month">
            <option value="0">Janeiro</option>
            <option value="1">Fevereiro</option>
            <option value="2">Março</option>
            <option value="3">Abril</option>
            <option value="4">Maio</option>
            <option value="5">Junho</option>
            <option value="6">Julho</option>
            <option value="7">Agosto</option>
            <option value="8">Setembro</option>
            <option value="9">Outubro</option>
            <option value="10">Novembro</option>
            <option value="11">Dezembro</option>
        </select>

        <button onclick="calculateEarnings()">Calcular</button>

        <div class="result" id="result"></div>
    </div>

    <script>
        function calculateEarnings() {
            const dailyRate = parseFloat(document.getElementById('daily-rate').value);
            const month = parseInt(document.getElementById('month').value);
            const year = 2025;

            if (isNaN(dailyRate) || dailyRate <= 0) {
                alert('Por favor, insira um valor válido para a diária.');
                return;
            }

            const workDays = calculateWorkDays(year, month);
            const totalEarnings = workDays * dailyRate;

            document.getElementById('result').innerText = `Você receberá R$ ${totalEarnings.toFixed(2)} no mês selecionado.`;
        }

        function calculateWorkDays(year, month) {
            let workDays = 0;
            const date = new Date(year, month, 1);

            while (date.getMonth() === month) {
                const day = date.getDay();
                if (day !== 0 && day !== 6) { // Exclui domingos (0) e sábados (6)
                    workDays++;
                }
                date.setDate(date.getDate() + 1);
            }

            return workDays;
        }
    </script>
</body>
</html>
