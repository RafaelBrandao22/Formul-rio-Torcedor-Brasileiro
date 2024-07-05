# Formul-rio-Torcedor-Brasileiro
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Formulário de Torcedor de Futebol</title>
    <style>
        body {
            background-color: #d3d3d3;
            font-family: Arial, sans-serif;
            color: black;
            text-align: center;
        }
        form {
            background-color: #f0f0f0;
            border: 2px solid white;
            border-radius: 10px;
            padding: 20px;
            width: 80%;
            max-width: 600px;
            margin: auto;
        }
        label {
            display: block;
            margin-top: 10px;
        }
        input, select, textarea, button {
            width: 100%;
            margin-top: 5px;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        button {
            background-color: #000;
            color: white;
            border: none;
            cursor: pointer;
        }
        button:hover {
            background-color: #333;
        }
        img {
            max-width: 100px;
            margin-bottom: 20px;
        }
    </style>
</head>
<body>
    <h1>Formulário de Torcedor Brasileiro de Futebol</h1>
    <img src="intertorcedor.jpg" alt="Futebol">
    <form id="torcedorForm">
        <label for="nome">Qual seu nome?</label>
        <input type="text" id="nome" name="nome" required>

        <label for="idade">Idade:</label>
        <select id="idade" name="idade" required>
            <option value="crianca">Criança</option>
            <option value="adolescente">Adolescente</option>
            <option value="adulto">Adulto</option>
        </select>

        <label>Qual seu gênero?</label>
        <input type="radio" id="masculino" name="genero" value="masculino" required>
        <label for="masculino">Masculino</label>
        <input type="radio" id="feminino" name="genero" value="feminino" required>
        <label for="feminino">Feminino</label>

        <label for="time">Qual seu time do coração?</label>
        <input type="text" id="time" name="time" required>

        <label for="segundoTime">Você tem algum segundo time para torcer?</label>
        <input type="text" id="segundoTime" name="segundoTime">

        <label>Você é sócio de algum clube?</label>
        <input type="radio" id="socioSim" name="socio" value="sim" required>
        <label for="socioSim">Sim</label>
        <input type="radio" id="socioNao" name="socio" value="nao" required>
        <label for="socioNao">Não</label>

        <label>Você costuma assistir aos jogos do seu time?</label>
        <input type="radio" id="jogosSim" name="assisteJogos" value="sim" required>
        <label for="jogosSim">Sim</label>
        <input type="radio" id="jogosNao" name="assisteJogos" value="nao" required>
        <label for="jogosNao">Não</label>

        <label>Você costuma assistir aos jogos:</label>
        <input type="radio" id="casa" name="assisteOnde" value="casa" required>
        <label for="casa">Em casa sozinho</label>
        <input type="radio" id="estadio" name="assisteOnde" value="estadio" required>
        <label for="estadio">No estádio</label>
        <input type="radio" id="amigos" name="assisteOnde" value="amigos" required>
        <label for="amigos">Com os amigos</label>

        <label for="sugestao">Como você acha que seu clube poderia conseguir mais associados?</label>
        <textarea id="sugestao" name="sugestao" rows="4" cols="50"></textarea>

        <button type="submit">Enviar</button>
    </form>

    <script>
        document.getElementById('torcedorForm').addEventListener('submit', function(event) {
            event.preventDefault();
            const formData = new FormData(event.target);
            const data = {};
            formData.forEach((value, key) => {
                data[key] = value;
            });
            console.log('Dados do formulário:', data);
            alert('Formulário enviado com sucesso!');
            event.target.reset();
        });
    </script>
</body>
</html>
