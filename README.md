# Gantt Chart

Este projeto é uma aplicação web que utiliza o **Syncfusion Gantt Chart** para exibir um gráfico de Gantt interativo. A aplicação é composta por um **back-end** feito em **Python (Flask)** e um **front-end** em **HTML, CSS e JavaScript**.

### Visão Geral

- O **back-end** é uma API RESTful construída com **Flask** que fornece os dados do gráfico de Gantt em formato JSON.
- O **front-end** utiliza o **Syncfusion Gantt Chart** para exibir os dados recebidos da API e renderizar o gráfico interativo.

---

## Estrutura do Projeto

```
/meu_projeto_gantt
│
├── /backend               # Back-end com Flask
│   ├── /app               # Lógica do Flask
│   ├── requirements.txt   # Dependências do Python
│   ├── run.py             # Inicia o servidor Flask
│   ├── config.py          # Configurações do Flask
│
├── /frontend              # Front-end com Syncfusion Gantt Chart
│   ├── /public            # Arquivos estáticos (HTML, CSS)
│   ├── /src               # Código JavaScript
│   ├── index.html         # HTML principal
│   └── index.js           # JavaScript principal para consumir a API
│
├── /docs                  # Documentação do projeto
│   └── setup.md           # Como configurar o ambiente
│
└── README.md              # Documentação principal do projeto
```

---

## Pré-requisitos

Antes de começar, certifique-se de que você tem os seguintes programas instalados:

- **Python 3.x** ou superior
- **Node.js** e **npm** (para o front-end)

---

## Como Configurar o Projeto

### 1. **Configuração do Back-end (Python/Flask)**

#### Passo 1: Instalar dependências

1. Navegue até a pasta `backend`:

```bash
cd backend
```

2. Crie e ative um ambiente virtual (opcional, mas recomendado):

```bash
# Cria um ambiente virtual
python -m venv venv

# Ativa o ambiente virtual
# No Windows
venv\Scripts\activate
# No Mac/Linux
source venv/bin/activate
```

3. Instale as dependências do projeto:

```bash
pip install -r requirements.txt
```

#### Passo 2: Executar o servidor Flask

1. Com o ambiente virtual ativado, inicie o servidor Flask:

```bash
python run.py
```

2. O back-end estará rodando em `http://localhost:5000`.

### 2. **Configuração do Front-end (JavaScript/Syncfusion)**

#### Passo 1: Instalar dependências do front-end

1. Navegue até a pasta `frontend`:

```bash
cd frontend
```

2. Instale as dependências do front-end:

```bash
npm install
```

#### Passo 2: Executar o Front-end

1. Abra o arquivo `index.html` no seu navegador. Você também pode usar uma ferramenta como o **Live Server** no VSCode para servir o arquivo.

2. O front-end fará uma requisição `fetch` para a API Flask e exibirá o gráfico de Gantt.

---

## Como Funciona

1. O **back-end** fornece os dados em JSON através da rota `/api/gantt-data`.
2. O **front-end** (JavaScript) faz uma requisição `fetch()` para essa rota e recebe os dados.
3. Os dados são passados para o **Syncfusion Gantt Chart**, que renderiza o gráfico interativo no navegador.

---

## Funcionalidades

- **Exibição de Gráfico de Gantt**: O Syncfusion Gantt Chart exibe tarefas com datas de início e término, além de progressos.
- **Integração com API**: O front-end consome dados de uma API RESTful construída em Flask.
- **Configuração Simples**: O back-end e o front-end podem ser configurados e executados de forma independente.

---

## Tecnologias Utilizadas

- **Back-end**: Python, Flask
- **Front-end**: HTML, CSS, JavaScript, Syncfusion Gantt Chart
- **Banco de Dados** (opcional): Nenhum banco de dados foi configurado nesta versão, mas você pode integrar facilmente com um banco de dados no back-end.

---

## Como Contribuir

1. Faça um fork deste repositório.
2. Crie uma nova branch (`git checkout -b minha-nova-funcionalidade`).
3. Faça as alterações desejadas e envie um commit (`git commit -am 'Adicionando nova funcionalidade'`).
4. Envie para a branch principal (`git push origin minha-nova-funcionalidade`).
5. Abra um Pull Request.

---

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).
