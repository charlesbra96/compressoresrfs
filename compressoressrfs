<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Controle de Horas Corridas - Compressors</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: left;
            margin-left: 50px;
            background-color: #333; /* Cor de fundo cinza escuro */
            color: white; /* Cor do texto branca para contraste */
        }
        input, button {
            font-size: 16px;
            margin: 10px;
            padding: 10px;
        }
        #horas {
            font-size: 24px;
            font-weight: bold;
            margin-top: 20px;
        }
        h1 {
            color: #007bff;
        }
        .zerar, .alterar-senha {
            background-color: red;
            color: white;
        }
        .manutencao {
            margin-top: 20px;
        }
        .historico-item {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 10px;
            margin-top: 5px;
        }
        .delete-btn {
            background-color: red;
            color: white;
            border: none;
            padding: 5px;
            cursor: pointer;
        }
        .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .right-side {
            text-align: right;
        }
    </style>
</head>
<body>

    <h1>COMPRESSOR DE NITROGÊNIO 1</h1>
    <div class="container">
        <div>
            <label for="horasIniciais1">Digite as horas iniciais:</label>
            <input type="number" id="horasIniciais1" placeholder="Ex: 1000">
            <button onclick="iniciarContagem(1)">Iniciar</button>
            <button class="zerar" onclick="zerarHoras(1)">Zerar Horas</button>
        </div>
        <div class="right-side">
            <label for="senhaAtual">Alterar Senha:</label>
            <input type="password" id="senhaAtual" placeholder="Senha atual">
            <input type="password" id="novaSenha" placeholder="Nova Senha">
            <button class="alterar-senha" onclick="alterarSenha()">Alterar Senha</button>
        </div>
    </div>

    <h2 id="horas1">Horas Corridas: 0h 0m 0s</h2>

    <div class="manutencao">
        <h3>Último Overhaul:</h3>
        <label for="dataOverhaul1">Data:</label>
        <input type="date" id="dataOverhaul1">
        <label for="ordemServico1">Ordem de Serviço:</label>
        <input type="text" id="ordemServico1" placeholder="Ex: OS-12345">
        <button onclick="salvarOverhaul(1)">Salvar Overhaul</button>
        <p id="ultimoOverhaul1">Nenhuma data registrada.</p>

        <h3>Histórico de Overhauls:</h3>
        <ul id="historicoOverhauls1"></ul>
    </div>

    <hr>

    <h1>COMPRESSOR DE NITROGÊNIO 2</h1>
    <div>
        <label for="horasIniciais2">Digite as horas iniciais:</label>
        <input type="number" id="horasIniciais2" placeholder="Ex: 1000">
        <button onclick="iniciarContagem(2)">Iniciar</button>
        <button class="zerar" onclick="zerarHoras(2)">Zerar Horas</button>
    </div>

    <h2 id="horas2">Horas Corridas: 0h 0m 0s</h2>

    <div class="manutencao">
        <h3>Último Overhaul:</h3>
        <label for="dataOverhaul2">Data:</label>
        <input type="date" id="dataOverhaul2">
        <label for="ordemServico2">Ordem de Serviço:</label>
        <input type="text" id="ordemServico2" placeholder="Ex: OS-12345">
        <button onclick="salvarOverhaul(2)">Salvar Overhaul</button>
        <p id="ultimoOverhaul2">Nenhuma data registrada.</p>

        <h3>Histórico de Overhauls:</h3>
        <ul id="historicoOverhauls2"></ul>
    </div>

    <hr>

    <h1>COMPRESSOR DE NITROGÊNIO 3</h1>
    <div>
        <label for="horasIniciais3">Digite as horas iniciais:</label>
        <input type="number" id="horasIniciais3" placeholder="Ex: 1000">
        <button onclick="iniciarContagem(3)">Iniciar</button>
        <button class="zerar" onclick="zerarHoras(3)">Zerar Horas</button>
    </div>

    <h2 id="horas3">Horas Corridas: 0h 0m 0s</h2>

    <div class="manutencao">
        <h3>Último Overhaul:</h3>
        <label for="dataOverhaul3">Data:</label>
        <input type="date" id="dataOverhaul3">
        <label for="ordemServico3">Ordem de Serviço:</label>
        <input type="text" id="ordemServico3" placeholder="Ex: OS-12345">
        <button onclick="salvarOverhaul(3)">Salvar Overhaul</button>
        <p id="ultimoOverhaul3">Nenhuma data registrada.</p>

        <h3>Histórico de Overhauls:</h3>
        <ul id="historicoOverhauls3"></ul>
    </div>

    <hr>

    <h1>COMPRESSOR DE NITROGÊNIO 4</h1>
    <div>
        <label for="horasIniciais4">Digite as horas iniciais:</label>
        <input type="number" id="horasIniciais4" placeholder="Ex: 1000">
        <button onclick="iniciarContagem(4)">Iniciar</button>
        <button class="zerar" onclick="zerarHoras(4)">Zerar Horas</button>
    </div>

    <h2 id="horas4">Horas Corridas: 0h 0m 0s</h2>

    <div class="manutencao">
        <h3>Último Overhaul:</h3>
        <label for="dataOverhaul4">Data:</label>
        <input type="date" id="dataOverhaul4">
        <label for="ordemServico4">Ordem de Serviço:</label>
        <input type="text" id="ordemServico4" placeholder="Ex: OS-12345">
        <button onclick="salvarOverhaul(4)">Salvar Overhaul</button>
        <p id="ultimoOverhaul4">Nenhuma data registrada.</p>

        <h3>Histórico de Overhauls:</h3>
        <ul id="historicoOverhauls4"></ul>
    </div>

    <script>
        let senha = localStorage.getItem("senha") || "12345"; // Senha inicial

        function iniciarContagem(compressor) {
            let senhaDigitada = prompt("Digite a senha para iniciar:");
            if (senhaDigitada === senha) {
                let horasIniciais = parseFloat(document.getElementById(`horasIniciais${compressor}`).value);
                if (isNaN(horasIniciais) || horasIniciais < 0) {
                    alert("Por favor, insira um valor válido.");
                    return;
                }

                localStorage.setItem(`horasIniciais${compressor}`, horasIniciais);
                localStorage.setItem(`dataInicio${compressor}`, new Date().getTime());

                atualizarHoras(compressor);
            } else {
                alert("Senha incorreta.");
            }
        }

        function atualizarHoras(compressor) {
            let horasIniciais = parseFloat(localStorage.getItem(`horasIniciais${compressor}`)) || 0;
            let dataInicio = parseFloat(localStorage.getItem(`dataInicio${compressor}`));

            if (!dataInicio) return;

            let agora = new Date().getTime();
            let segundosDecorridos = (agora - dataInicio) / 1000;
            let totalSegundos = Math.floor(horasIniciais * 3600 + segundosDecorridos);

            let horas = Math.floor(totalSegundos / 3600);
            let minutos = Math.floor((totalSegundos % 3600) / 60);
            let segundos = totalSegundos % 60;

            document.getElementById(`horas${compressor}`).innerText = `Horas Corridas: ${horas}h ${minutos}m ${segundos}s`;

            setTimeout(() => atualizarHoras(compressor), 1000);
        }

        function zerarHoras(compressor) {
            let senhaDigitada = prompt("Digite a senha para zerar as horas:");
            if (senhaDigitada === senha) {
                if (confirm("Tem certeza que deseja zerar as horas?")) {
                    localStorage.removeItem(`horasIniciais${compressor}`);
                    localStorage.removeItem(`dataInicio${compressor}`);
                    document.getElementById(`horas${compressor}`).innerText = "Horas Corridas: 0h 0m 0s";
                }
            } else {
                alert("Senha incorreta. Não foi possível zerar as horas.");
            }
        }

        function alterarSenha() {
            let senhaAtual = document.getElementById(`senhaAtual`).value;
            let novaSenha = document.getElementById(`novaSenha`).value;

            if (senhaAtual === senha) {
                if (novaSenha.length === 5) {
                    senha = novaSenha; // Atualiza a senha global
                    localStorage.setItem("senha", senha); // Salva a nova senha no localStorage
                    alert("Senha alterada com sucesso!");
                } else {
                    alert("A nova senha deve ter 5 dígitos.");
                }
            } else {
                alert("Senha incorreta.");
            }
        }

        function salvarOverhaul(compressor) {
            let senhaDigitada = prompt("Digite a senha para salvar o overhaul:");
            if (senhaDigitada === senha) {
                let dataOverhaul = document.getElementById(`dataOverhaul${compressor}`).value;
                let ordemServico = document.getElementById(`ordemServico${compressor}`).value.trim();

                if (!dataOverhaul || !ordemServico) {
                    alert("Por favor, preencha a data e a Ordem de Serviço.");
                    return;
                }

                let historico = JSON.parse(localStorage.getItem(`historicoOverhauls${compressor}`)) || [];
                historico.push({ data: dataOverhaul, ordem: ordemServico });
                localStorage.setItem(`historicoOverhauls${compressor}`, JSON.stringify(historico));

                localStorage.setItem(`ultimoOverhaul${compressor}`, JSON.stringify({ data: dataOverhaul, ordem: ordemServico }));

                carregarOverhaul(compressor);
            } else {
                alert("Senha incorreta.");
            }
        }

        function carregarOverhaul(compressor) {
            let ultimoOverhaul = JSON.parse(localStorage.getItem(`ultimoOverhaul${compressor}`));
            let historico = JSON.parse(localStorage.getItem(`historicoOverhauls${compressor}`)) || [];

            if (ultimoOverhaul) {
                document.getElementById(`ultimoOverhaul${compressor}`).innerText = `Último Overhaul: ${ultimoOverhaul.data} - Ordem: ${ultimoOverhaul.ordem}`;
            }

            let historicoUl = document.getElementById(`historicoOverhauls${compressor}`);
            historicoUl.innerHTML = "";
            historico.forEach(item => {
                let li = document.createElement("li");
                li.innerHTML = `${item.data} - Ordem: ${item.ordem} <button class="delete-btn" onclick="apagarOverhaul(${compressor}, '${item.data}')">Apagar</button>`;
                historicoUl.appendChild(li);
            });
        }

        function apagarOverhaul(compressor, data) {
            let senhaDigitada = prompt("Digite a senha para apagar a data:");
            if (senhaDigitada === senha) {
                let historico = JSON.parse(localStorage.getItem(`historicoOverhauls${compressor}`)) || [];
                historico = historico.filter(item => item.data !== data);
                localStorage.setItem(`historicoOverhauls${compressor}`, JSON.stringify(historico));
                carregarOverhaul(compressor);
            } else {
                alert("Senha incorreta.");
            }
        }

        // Carrega os dados ao inicializar a página
        window.onload = function () {
            for (let i = 1; i <= 4; i++) {
                atualizarHoras(i);
                carregarOverhaul(i);
            }
        }

    </script>
</body>
</html>
