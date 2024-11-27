<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Valorant - Gerenciar Dados</title>
    <link href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
<div class="container mt-5">
    <h1>Gerenciar Agentes e Mapas</h1>

    <!-- Menu de Busca -->
    <form id="formBusca" class="mb-4">
        <input type="text" id="campoBusca" class="form-control mb-2" placeholder="Buscar agentes ou mapas...">
        <button type="submit" class="btn btn-primary">Buscar</button>
    </form>

    <!-- Navegação -->
    <a href="#mapas" class="btn btn-info mb-4">Ir para Mapas</a>

    <!-- Botão para importar dados -->
    <button id="botaoImportar" class="btn btn-primary mb-4">Importar Dados</button>

    <!-- Botão para limpar dados -->
    <button id="botaoLimpar" class="btn btn-danger mb-4">Limpar Banco de Dados</button>

    <!-- Exibição de Agentes -->
    <h2>Agentes</h2>
    <div id="agentes" class="row"></div>

    <!-- Exibição de Mapas -->
    <h2 id="mapas">Mapas</h2>
    <div id="mapasContainer" class="row"></div>
</div>

<script>
document.addEventListener('DOMContentLoaded', function () {
    const containerAgentes = document.getElementById('agentes');
    const containerMapas = document.getElementById('mapasContainer');
    const formularioBusca = document.getElementById('formBusca');
    const campoBusca = document.getElementById('campoBusca');
    const botaoImportar = document.getElementById('botaoImportar');
    const botaoLimpar = document.getElementById('botaoLimpar');

    let dadosAgentes = [];
    let dadosMapas = [];

    // Carregar dados de agentes e mapas
    async function carregarDados() {
        try {
            const respostaAgentes = await fetch('https://valorant-api.com/v1/agents');
            const respostaMapas = await fetch('https://valorant-api.com/v1/maps');

            const jsonAgentes = await respostaAgentes.json();
            const jsonMapas = await respostaMapas.json();

            dadosAgentes = jsonAgentes.data;
            dadosMapas = jsonMapas.data;

            renderizarAgentes();
            renderizarMapas();
        } catch (erro) {
            console.error("Erro ao carregar dados: ", erro);
        }
    }

    // Exibir agentes
    function renderizarAgentes() {
        containerAgentes.innerHTML = '';
        dadosAgentes.forEach(agente => {
            const cartaoAgente = `
                <div class="col-md-4 mb-4">
                    <div class="card">
                        <img src="${agente.fullPortrait || ''}" class="card-img-top" alt="${agente.displayName}">
                        <div class="card-body">
                            <h5 class="card-title">${agente.displayName}</h5>
                            <p class="card-text">${agente.description}</p>
                            <input type="text" placeholder="Novo Nome" class="form-control mb-2" id="novoNome-${agente.uuid}">
                            <button class="btn btn-warning btn-sm" onclick="atualizarNomeAgente('${agente.uuid}')">Atualizar Nome</button>
                            <button class="btn btn-danger btn-sm" onclick="excluirAgente('${agente.uuid}')">Excluir</button>
                        </div>
                    </div>
                </div>
            `;
            containerAgentes.innerHTML += cartaoAgente;
        });
    }

    // Exibir mapas
    function renderizarMapas() {
        containerMapas.innerHTML = '';
        dadosMapas.forEach(mapa => {
            const cartaoMapa = `
                <div class="col-md-4 mb-4">
                    <div class="card">
                        <img src="${mapa.splash || ''}" class="card-img-top" alt="${mapa.displayName}">
                        <div class="card-body">
                            <h5 class="card-title">${mapa.displayName}</h5>
                            <input type="text" placeholder="Novo Nome" class="form-control mb-2" id="novoNomeMapa-${mapa.uuid}">
                            <button class="btn btn-warning btn-sm" onclick="atualizarNomeMapa('${mapa.uuid}')">Atualizar Nome</button>
                            <button class="btn btn-danger btn-sm" onclick="excluirMapa('${mapa.uuid}')">Excluir</button>
                        </div>
                    </div>
                </div>
            `;
            containerMapas.innerHTML += cartaoMapa;
        });
    }

    // Filtrar dados
    function filtrarDados() {
        const busca = campoBusca.value.toLowerCase();
        const agentesFiltrados = dadosAgentes.filter(agente => agente.displayName.toLowerCase().includes(busca));
        const mapasFiltrados = dadosMapas.filter(mapa => mapa.displayName.toLowerCase().includes(busca));

        dadosAgentes = agentesFiltrados;
        dadosMapas = mapasFiltrados;

        renderizarAgentes();
        renderizarMapas();
    }

    // Atualizar nome do agente
    function atualizarNomeAgente(uuid) {
        const novoNome = document.getElementById(`novoNome-${uuid}`).value;
        if (novoNome) {
            const agente = dadosAgentes.find(a => a.uuid === uuid);
            agente.displayName = novoNome; // Atualiza localmente
            renderizarAgentes(); // Re-renderiza a lista
        }
    }

    // Excluir agente
    function excluirAgente(uuid) {
        dadosAgentes = dadosAgentes.filter(agente => agente.uuid !== uuid); // Remove localmente
        renderizarAgentes(); // Re-renderiza a lista
    }

    // Atualizar nome do mapa
    function atualizarNomeMapa(uuid) {
        const novoNome = document.getElementById(`novoNomeMapa-${uuid}`).value;
        if (novoNome) {
            const mapa = dadosMapas.find(m => m.uuid === uuid);
            mapa.displayName = novoNome; // Atualiza localmente
            renderizarMapas(); // Re-renderiza a lista
        }
    }

    // Excluir mapa
    function excluirMapa(uuid) {
        dadosMapas = dadosMapas.filter(mapa => mapa.uuid !== uuid); // Remove localmente
        renderizarMapas(); // Re-renderiza a lista
    }

    // Importar dados (inicia a carga de dados da API)
    botaoImportar.addEventListener('click', carregarDados);

    // Limpar dados
    botaoLimpar.addEventListener('click', () => {
        dadosAgentes = [];
        dadosMapas = [];
        renderizarAgentes();
        renderizarMapas();
    });

    // Buscar dados
    formularioBusca.addEventListener('submit', function (evento) {
        evento.preventDefault();
        filtrarDados();
    });

    // Inicializar com os dados
    carregarDados();
});
</script>

<script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.9.2/dist/umd/popper.min.js"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>
</body>
</html>
