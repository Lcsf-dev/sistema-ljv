# Estrutura do Projeto

Abaixo esta uma visao organizada da estrutura do Sistema LJV original. Arquivos sensiveis, dados locais, backups e dependencias instaladas nao fazem parte deste repositorio publico.

```text
.
|-- src/
|   |-- frontend/
|   |   |-- app.ts
|   |   |-- dom.ts
|   |   `-- schemas.ts
|   `-- worker/
|       |-- index.ts
|       |-- security.ts
|       |-- permissions.ts
|       |-- audit.ts
|       |-- http-security.ts
|       `-- login-rate-limit.ts
|-- public/
|   |-- index.html
|   |-- styles.css
|   |-- app.js
|   `-- favicon.ico
|-- migrations/
|   |-- 0001_schema.sql
|   |-- 0002_seed_config.sql
|   |-- 0003_auditoria.sql
|   |-- 0004_codigo_itens.sql
|   |-- 0005_usuarios.sql
|   |-- 0006_permissoes_auditoria.sql
|   |-- 0007_login_tentativas.sql
|   |-- 0008_tipo_diverso.sql
|   |-- 0009_cor_destaque.sql
|   `-- 0010_cor_painel.sql
|-- scripts/
|   |-- abrir-sistema-ljv-cloudflare.ps1
|   |-- build-frontend.mjs
|   |-- backup-d1.mjs
|   |-- restore-d1.mjs
|   |-- sync-remote-to-local.mjs
|   |-- verify-db.mjs
|   |-- verify-security.mjs
|   |-- smoke-api.mjs
|   |-- test-api.mjs
|   `-- deploy-check.mjs
|-- docs/
|   |-- documentacao-tecnica-sistema-ljv.md
|   `-- documentacao-tecnica-sistema-ljv.pdf
|-- package.json
|-- package-lock.json
|-- tsconfig.json
|-- tsconfig.frontend.json
|-- tsconfig.worker.json
|-- worker-configuration.d.ts
|-- wrangler.toml
`-- README.md
```

## Pastas Mantidas Fora do Repositorio Publico

```text
.dev.vars     Variaveis e senha local
.wrangler/    Estado local do Wrangler e banco local
Backup/       Backups SQL
logs/         Logs de execucao
node_modules/ Dependencias instaladas
```

