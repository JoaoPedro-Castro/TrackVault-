<div align="center">
 
<img src="./public/assets/imagens/capaReadme.jpg" alt="Banner do Projeto" width="100%"/>
  <h1>🎧 TrackVault </h1>

  <p>
    <strong>Um sistema completo para catalogar, gerenciar e pesquisar faixas de música eletrônica.</strong><br>
    <em>Organize BPM, vertentes, gêneros e artistas em uma única plataforma.</em>
  </p>

  
  <img src="https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript" />
  <img src="https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL" />
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5" />
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3" />

  <br><br>
</div>

---

## 📌 Índice Interativo

- [Sobre o Projeto](#-sobre-o-projeto)
- [Funcionalidades](#-principais-funcionalidades)
- [Estrutura de Arquivos](#-estrutura-e-responsabilidade-dos-arquivos)
- [Fluxo de Requisição](#-fluxo-de-uma-requisição)
- [Diretrizes de Implementação](#-diretrizes-para-novas-funcionalidades)
- [Como Executar](#-como-executar-o-projeto)
- [Diagramas](#-diagramas-do-projeto)

---

## 📖 Sobre o Projeto
Desenvolvimento de um website que nasceu a partir de uma paixão, voltado para prospecção de produções musicais voltadas para diferentes vertentes de musica.3
eletrônica, destinado a auxiliar DJs, produtores e entusiastas a organizarem suas bibliotecas musicais. A aplicação conta com uma API robusta no back-end que se comunica de forma eficiente com um banco de dados relacional e fornece todas as informações para uma interface interativa no front-end.

---

## ⚡ Principais Funcionalidades

- **🎹 Cadastro de Tracks:** Inserção de novas faixas no banco de dados com seus respectivos metadados (BPM, Key, etc).
- **🔍 Consulta Avançada:** Busca de músicas específicas por gênero, artista ou faixa de tempo.
- **🛠️ Gerenciamento:** Atualização de dados de faixas existentes e remoção de registros.

---

## 📁 Estrutura e Responsabilidade dos Arquivos

A arquitetura do projeto foi desenhada utilizando o conceito de separação de responsabilidades. **Antes de implementar qualquer funcionalidade, verifique esta estrutura:**

| Diretório/Arquivo | Responsabilidade Principal |
| :--- | :--- |
| 🌐 **`public/`** | Arquivos estáticos do front-end (`.html`, `.css`, `.js` do cliente). |
| 🛣️ **`routes/`** | Define as rotas (endpoints) da API e direciona as requisições. |
| 🧠 **`controllers/`** | Recebe as requisições das rotas, processa a lógica de negócio e retorna as respostas. |
| 📦 **`models/`** | Operações diretas com os dados e consultas ao banco (Query SQL). |
| 🔌 **`database/`** | Arquivos de conexão com o banco de dados MySQL. |
| ⚙️ **`app.js`** | Configuração do servidor Node.js, middlewares e registro global de rotas. |
| 💾 **`Script SQL`** | Script base para criar e popular o banco de dados. |

---

## 🔄 Fluxo de uma Requisição

<details>
<summary><b>Clique aqui para visualizar o ciclo de vida completo de uma requisição 🚀</b></summary>

<br>

1. **🧑‍💻 Usuário:** Interage com uma página HTML (ex: pesquisa um gênero).
2. **👀 Front-end (JS):** O JavaScript intercepta a ação (evento de clique/teclado).
3. **📨 Envio (Fetch):** O JS envia os dados para a rota correspondente da API.
4. **🛣️ Rotas (`routes`):** Direciona a requisição para o controller responsável.
5. **⚙️ Processamento (`controllers`):** Valida a solicitação e utiliza o model, se necessário.
6. **🗄️ Persistência (`models`):** O model executa operações no MySQL via `database`.
7. **🔄 Resposta:** Os dados retornam pela API (JSON) e o JS atualiza o HTML dinamicamente.

</details>

---

## 🛠️ Diretrizes para Novas Funcionalidades

Se você for contribuir ou expandir este código, siga este checklist:

- [ ] **1. Verificação:** Verifique se a funcionalidade já existe na API.
- [ ] **2. Front-end:** Altere apenas os arquivos dentro da pasta `public/` para mudanças visuais.
- [ ] **3. Back-end:** Siga rigorosamente a ordem lógica de `Rota ➔ Controller ➔ Model`.
- [ ] **4. Banco de Dados:** Mantenha os Scripts SQL atualizados e respeite os relacionamentos existentes.
- [ ] **5. Padronização:** Mantenha a comunicação JSON e o mesmo padrão de variáveis e estilos.

---

## 🚀 Como Executar o Projeto

<details>
<summary><b>Mostrar instruções passo a passo de instalação 💻</b></summary>

<br>

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/seu-usuario/seu-repositorio.git
   ```

2. **Configure o Banco de Dados:**
   - Execute o arquivo `Script SQL` no seu MySQL.
   - Configure suas credenciais de acesso na pasta `database/`.

3. **Instale as dependências:**
   ```bash
   npm install
   ```

4. **Inicie o servidor:**
   ```bash
   node app.js
   ```

5. **Acesse a aplicação:**
   Abra o seu navegador em `http://localhost:3000` (ou na porta configurada).

</details>

---

