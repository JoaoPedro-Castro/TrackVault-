# AGENTS.md

## Contexto real deste repositório
- Projeto Node.js + Express + MySQL2 com front-end estático em `public/` e API em `src/`.
- A estrutura ativa hoje é:
  - `public/`: HTML/CSS/JS do cliente
  - `src/routes/`: rotas Express
  - `src/controllers/`: regras de requisição/resposta
  - `src/models/`: SQL e acesso ao banco via `src/database/config.js`
  - `src/database/script-tabelas.sql`: script SQL base (template Aquatech)

## Antes de alterar qualquer coisa
- **Verifique o estado real do código, não só o README**. Há inconsistências de documentação.
- Não inventar rotas, parâmetros, tabelas, colunas ou fluxos que não existam no código.
- Não apagar arquivos/dados sem autorização explícita.
- Para mudanças de banco, primeiro mapear impacto em `models/` e `controllers/`.

## Comandos e execução (importante)
- `package.json` define:
  - `npm start` → `node app.js`
  - `npm run dev` → `nodemon --exec node app.js`
- **Atualmente não existe `app.js` no repositório**. Antes de tentar subir servidor, localizar/alinhar o entrypoint com o time.
- Não há scripts de teste/lint/typecheck configurados no `package.json`.

## Banco e ambiente
- Variáveis de banco vêm de `.env` / `.env.dev` e são lidas por `src/database/config.js`.
- `AMBIENTE_PROCESSO` precisa ser `producao` ou `desenvolvimento`; fora disso, a conexão falha.
- Script SQL disponível em `src/database/script-tabelas.sql` usa schema/tabelas de template (`aquatech`, `empresa`, `aquario`, etc.). Validar antes de reutilizar no contexto TrackVault.

## Convenções para contribuições de agente
- Manter implementações simples e didáticas (público alvo: aprendizado inicial).
- Se precisar usar recurso não estudado pelo dono do projeto, explicar antes e pedir autorização.
- Evitar mudanças de arquitetura sem necessidade.
- Quando solicitado, entregar arquivo completo alterado para facilitar comparação/substituição.
