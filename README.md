<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora de Interações</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            padding: 20px;
            background-color: #f4f4f9;
        }

        .container {
            max-width: 600px;
            margin: 0 auto;
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        input, button {
            padding: 10px;
            margin: 10px 0;
            width: 100%;
            font-size: 16px;
            border-radius: 5px;
            border: 1px solid #ddd;
        }

        button {
            background-color: #4CAF50;
            color: white;
            cursor: pointer;
        }

        button:hover {
            background-color: #45a049;
        }

        .result {
            font-size: 20px;
            font-weight: bold;
            color: #333;
        }
    </style>
</head>
<body>

<div class="container">
    <h2>Calculadora de Interações</h2>

    <label for="curtidas">Número de Curtidas:</label>
    <input type="number" id="curtidas" placeholder="Digite o número de curtidas" min="0">

    <label for="comentarios">Número de Comentários:</label>
    <input type="number" id="comentarios" placeholder="Digite o número de comentários" min="0">

    <label for="compartilhamentos">Número de Compartilhamentos:</label>
    <input type="number" id="compartilhamentos" placeholder="Digite o número de compartilhamentos" min="0">

    <button onclick="calcularTotal()">Calcular Total de Interações</button>

    <div class="result" id="resultado"></div>
</div>

<script>
    function calcularTotal() {
        // Obtém os valores inseridos pelo usuário
        var curtidas = parseInt(document.getElementById('curtidas').value) || 0;
        var comentarios = parseInt(document.getElementById('comentarios').value) || 0;
        var compartilhamentos = parseInt(document.getElementById('compartilhamentos').value) || 0;

        // Calcula o total de interações
        var total = curtidas + comentarios + compartilhamentos;

        // Exibe o resultado
        document.getElementById('resultado').textContent = "Total de Interações: " + total;
    }
</script>

</body>
</html>
