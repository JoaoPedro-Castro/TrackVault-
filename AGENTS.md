# AGENTS.md

## Visão geral
Descreva brevemente o projeto: qual é o objetivo da aplicação, qual problema ela resolve e, se necessário, quem são os principais usuários.


O TrackVault é uma aplicação web voltada à descoberta, organização e prospecção de músicas eletrônicas.
O objetivo do projeto é permitir que usuários se cadastrem, façam login e encontrem e adicionem tracks de diferentes vertentes da música eletrônica, como Tech House, Techno, Melodic Techno e Progressive House.
A aplicação terá um catálogo de tracks com informações como nome da música, produtor, vertente e link para ouvir a produção em uma plataforma externa. Podendo 
prospectar e trazer mais players para as produções.
O projeto também contará com um banco de dados SQL para armazenar e organizar as informações necessárias para o funcionamento da aplicação.
Os principais usuários serão pessoas interessadas em descobrir novas produções musicais e administradores responsáveis pelo gerenciamento do catálogo.


## Tecnologias
Liste as principais tecnologias, frameworks, bibliotecas e serviços utilizados no projeto.


As tecnologias previstas para o projeto são:
HTML: estrutura das páginas.
CSS: aparência, cores, organização dos elementos e responsividade.
JavaScript: interatividade das páginas e comunicação com a API.
MySQL: armazenamento e organização dos dados.
MySQL Workbench: ferramenta utilizada para criar e administrar o banco de dados.
API fornecida pela faculdade: será utilizada para implementar as funcionalidades que já estiverem disponíveis, como cadastro, login e controle de permissões.
Antes de alterar a API, analisar o código existente e identificar como ela funciona.


## Comandos
Informe os comandos necessários para trabalhar com o projeto.


Utilizar somente comandos estudados até agora 
 
 SQL - MySql
Para consultas e modelagem de banco de dados, utilizar somente esses conceitos 
Banco de dados e tabelas: CREATE DATABASE, USE, DROP, DATABASE,  CREATE TABLE, ALTER TABLE, DROP TABLE, 
tipos de dados: INT, CHAR, VARCHAR, DATE, DATETIME , TINYINT
Restrições e relacionamentos: PRIMARY KEY, FOREIGN KEY, AUTO_INCREMENT, UNIQUE, NOT NULL, DEFAULT, CHECK
Manipulação de dados : INSERT INTO, VALUES, UPDATE, DELETE
Consultas: SELECT, FROM, LIKE, *, WHERE, DESC 
Relacionamento entre as tabelas: JOIN, INNER JOIN, LEFT JOIN , RIGHT JOIN, chaves primarias (PK), chaves estrangeiras (FK)
Funcções : NOW(), COUNT(); 

Restrições SQL : Não utilizar TRIGGER, STORED PROCEDURE, VIEW ou subconsultas complexas sem autorização
Não criar tabelas ou colunas desnecessárias.
Analisar a API antes de definir ou modificar a estrutura do banco de dados.
Antes de executar DROP TABLE ou DROP DATABASE, explicar o que será excluído e solicitar autorização.
Não utilizar comandos SQL que não estejam listados sem explicar sua finalidade e solicitar autorização.

HTML 
Elementos: html, head, body, title, h1, h2, p, div, label, input, button e link.
Atributos: id, class, for, onclick, type, value, href, rel, name e placeholder.
ão utilizar elementos ou atributos fora dessa lista sem explicar a necessidade e solicitar autorização

JAVASCRIPT 
utilizar somente esses seguintes comandos ja estudados
Variáveis: let.
Valores de campos: .value.
Conversão numérica: Number().
Eventos e exibição: onclick, alert() e innerHTML.
Condições: if, else e else if.
Operadores: >, <, >=, <=, ==, ===, !=, !==, &&, || e %.
Repetição: while e incremento de variáveis, como i++
Vetores: criação e utilização de arrays
Métodos de texto: .length, .includes(), .startsWith(), .endsWith(), .toLowerCase(), .toUpperCase() e .replaceAll().

Restrições HTML -
 Não utilizar o laço for, pois ainda não foi estudado
 Não utilizar document.getElementById() 
 Não introduzir const, funções de seta (=>), fetch(), async/await, Promises, addEventListener() ou querySelector() sem explicar a necessidade e solicitar autorização.
 Caso a integração com a API exija algum recurso não listado, explicar como funciona e por que é necessário antes de utilizá-lo.


CSS 
Utilizar CSS para estilizar as páginas, organizar os elementos e adaptar a interface a diferentes tamanhos de tela.
Manter o código simples e organizado 
Explicar propriedades ou recursos avançados antes de introduzi-los, quando necessário.

REGRA DE COMANDOS NOVOS 
A lista acima representa os comandos e recursos autorizados neste momento. Se alguma funcionalidade do TrackVault exigir algo que não esteja listado, explicar o que é, para que serve e por que é necessário, apresentando a alternativa mais simples possível antes de solicitar minha autorização.


## Arquitetura
Explique como o projeto está organizado e como uma funcionalidade deve ser implementada.

Antes de implementar qualquer funcionalidade, analisar a estrutura existente do projeto e a API fornecida.
Estrutura e responsabilidade dos arquivos:
public: arquivos do front-end, como HTML, CSS, JavaScript e outros recursos utilizados pelas páginas.
routes: define as rotas disponibilizadas pela API e direciona as requisições para os controllers
controllers: recebe as requisições, organiza o processamento e retorna as respostas ao cliente.
models: contém as operações relacionadas aos dados e às consultas ao banco de dados.
database: contém os arquivos relacionados à conexão com o banco de dados, conforme a estrutura existente.
app.js: arquivo responsável pela configuração do servidor, pelo registro das rotas e pela disponibilização dos arquivos públicos, conforme a implementação da API.
Script SQL: arquivo utilizado para criar e configurar o banco de dados.
Essa organização serve como referência para analisar a API. Antes de criar, mover ou modificar arquivos, verificar quais pastas e arquivos realmente existem.

Fluxo de uma requisição: 
1.O usuário interage com uma página HTML.
2.O JavaScript identifica a ação realizada.
3.O JavaScript envia os dados para a rota correspondente da API.
4.A rota direciona a requisição para o controller responsável.
5.O controller processa a solicitação e utiliza o model quando precisa acessar ou modificar dados.
6.O model executa as operações necessárias no MySQL por meio da conexão configurada.
7.A resposta retorna pela API e o JavaScript utiliza os dados para atualizar a página.

Implementação de novas funcionalidades:
Verificar primeiro se a funcionalidade já existe na API.
Para alterações no front-end, trabalhar nos arquivos HTML, CSS e JavaScript correspondentes.
Para novas operações da API, seguir a organização existente de rotas, controllers e models.
Para alterações no banco, verificar os scripts SQL, as tabelas existentes e a forma como a API utiliza os dados.
Manter a comunicação entre o front-end, a API e o banco de dados compatível com a implementação existente.
Não criar arquivos ou pastas desnecessários nem modificar a arquitetura sem justificativa.


## Padrões de desenvolvimento
- Utilizar somente as tecnologias definidas neste documento e respeitar as restrições da seção Comandos
- Manter o código simples, organizado e compreensível para um aluno do primeiro semestre de ADS
- Seguir os padrões de nomenclatura e organização já utilizados nos arquivos existentes.
- Utilizar nomes de variáveis, funções, arquivos e tabelas que indiquem claramente sua finalidade.
- Manter HTML, CSS e JavaScript organizados conforme a estrutura atual do projeto
- Evitar duplicação de código e funcionalidades desnecessárias.
- Reaproveitar as funcionalidades da API que já estejam implementadas e funcionando
- Não alterar partes funcionais sem necessidade.
- Explicar as alterações realizadas e a finalidade dos principais trechos de código.
- Quando solicitado, fornecer o código completo do arquivo alterado para facilitar a comparação e a substituição.
- Não adicionar funcionalidades que não foram solicitadas.
- 


## Cuidados e restrições

Analisar o código existente antes de implementar qualquer alteração.
Não inventar rotas, parâmetros, métodos, tabelas, campos ou funcionalidades da API.
Não apagar arquivos, tabelas ou dados sem minha autorização.
Antes de executar DROP TABLE ou DROP DATABASE, explicar o que será excluído e solicitar autorização.
Não utilizar comandos, métodos ou recursos de programação que não estejam autorizados na seção Comandos sem antes explicar sua finalidade e solicitar autorização.
Não utilizar o laço for, pois ainda não estudei esse comando.
Não introduzir frameworks, bibliotecas ou tecnologias adicionais sem autorização.
Não modificar a estrutura do banco de dados sem verificar o impacto na API.
Não adicionar upload de arquivos de áudio, comentários, curtidas ou outras funcionalidades extras sem autorização.
Se uma funcionalidade exigir um comando ou recurso ainda não estudado, explicar o motivo e apresentar a alternativa mais simples antes de implementá-la.
Priorizar as funcionalidades essenciais para concluir o projeto dentro do prazo disponível.

## Regra geral: 
Antes de implementar uma alteração, siga as tecnologias, arquitetura, convenções e restrições descritas neste documento. Caso alguma informação esteja ausente, analise o código existente e siga os padrões já adotados no projeto.
O objetivo é desenvolver o TrackVault de forma funcional, organizada e compatível com o conteúdo que já aprendi na SPTech, garantindo que eu consiga compreender as alterações realizadas.