# 💡 Memoteca

Um espaço digital para você organizar trechos de músicas, citações de livros, frases icônicas e aquelas ideias brilhantes que surgem do nada e que você não quer perder.

## 🚀 O Projeto

Este é um projeto **CRUD** (Create, Read, Update, Delete) completo, que permite ao usuário gerenciar uma lista de pensamentos de forma dinâmica. O sistema consome uma API simulada para garantir a persistência dos dados.

### Principais Funcionalidades:

* **Visualização:** Mural interativo com todos os pensamentos cadastrados.
* **Criação:** Formulário intuitivo para adicionar novas frases e autores.
* **Edição:** Altere o conteúdo ou a autoria de pensamentos já existentes.
* **Exclusão:** Remova pensamentos que não fazem mais sentido para você.
* **Feedback Visual:** Estado vazio (empty state) quando não há pensamentos no mural.

---

## 🛠️ Tecnologias Utilizadas

O projeto foi construído utilizando as seguintes tecnologias:

* **HTML5 & CSS3:** Estrutura e estilização com variáveis CSS e fontes personalizadas (*Poppins* e *Roboto Mono*).
* **JavaScript (ES6+):** Lógica de programação, manipulação de DOM e módulos.
* **Axios:** Cliente HTTP para comunicação com a API.
* **JSON Server:** Ferramenta para criar uma API REST fake completa para o backend.

---

## 📂 Estrutura de Pastas

```text
├── assets/             # Imagens e ícones
├── css/
│   └── styles.css      # Estilização global e componentes
├── js/
│   ├── api.js          # Configuração e chamadas ao Axios
│   ├── ui.js           # Manipulação da interface (DOM)
│   └── main.js         # Orquestrador principal da aplicação
├── db.json             # Banco de dados da aplicação (JSON)
├── index.html          # Página principal
└── package.json        # Dependências e scripts do backend

```

---

## 🔧 Como Executar o Projeto

### 1. Pré-requisitos

Você precisará ter o [Node.js](https://nodejs.org/) instalado em sua máquina.

### 2. Instalação do Backend

Navegue até a pasta onde está o arquivo `package.json` e instale o `json-server`:

```bash
npm install json-server

```

### 3. Iniciando a API

Para rodar o servidor mock e permitir que o frontend salve as informações, execute:

```bash
npm start

```

> **Nota:** O servidor rodará por padrão na porta `3000`. Certifique-se de que a `URL_BASE` no arquivo `api.js` está apontando para `http://localhost:3000`.

### 4. Executando o Frontend

Basta abrir o arquivo `index.html` no seu navegador de preferência ou utilizar a extensão *Live Server* do VS Code.

---

## 📝 Endpoints da API

A aplicação utiliza os seguintes caminhos baseados no `json-server`:

| Método | Endpoint | Descrição |
| --- | --- | --- |
| **GET** | `/pensamentos` | Retorna todos os pensamentos. |
| **POST** | `/pensamentos` | Cria um novo pensamento. |
| **PUT** | `/pensamentos/:id` | Atualiza um pensamento existente. |
| **DELETE** | `/pensamentos/:id` | Remove um pensamento do banco. |
