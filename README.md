<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Quadrado Perfeito e IMC</title>
    <style>
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            font-family: Arial, sans-serif;
            text-align: center;
            padding: 20px;
        }
        h1 { font-size: 1.4rem; margin: 10px; }
    </style>
</head>
<body>

    <h1 id="titulo"></h1>
    <h1 id="imc"></h1>

    <script>
        // ---------- Exercício 1: Quadrado Perfeito (sem função) ----------
        const lado = window.prompt('Qual o lado do quadrado perfeito?');
        const n = Number(lado);

        const area = n * n;
        const perimetro = 4 * n;

        document.getElementById('titulo').textContent = `Exercício 1 — Área: ${area}, Perímetro: ${perimetro}`;

        // ---------- Exercício 2: IMC (sem usar função) ----------
        const altura = window.prompt('Qual a sua altura em m?');
        const peso = window.prompt('Qual o seu peso em kg?');

        const altura1 = Number(altura);
        const peso1 = Number(peso);

        const imc = peso1 / (altura1 * altura1);

        let classificacao = '';

        if (imc < 18.5) {
            classificacao = 'Abaixo do peso';
        } else if (imc >= 18.5 && imc < 25) {
            classificacao = 'Peso normal';
        } else if (imc >= 25 && imc < 30) {
            classificacao = 'Sobrepeso';
        } else {
            classificacao = 'Obesidade';
        }

        document.getElementById('imc').textContent = `Exercício 2 — Seu IMC é: ${imc.toFixed(2)} (${classificacao})`;
    </script>

</body>
</html>
