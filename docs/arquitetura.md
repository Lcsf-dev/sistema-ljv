# Arquitetura

O Sistema LJV e uma aplicacao web serverless organizada em tres camadas principais: interface, API e banco de dados.

## Fluxo Geral

```text
Usuario no navegador
  -> Cloudflare Worker entrega HTML, CSS e JavaScript
  -> Frontend chama endpoints /api
  -> Worker valida sessao, permissoes e dados
  -> Worker consulta ou altera o Cloudflare D1
  -> Frontend atualiza a interface com a resposta
```

## Frontend

O frontend e escrito em TypeScript e compilado para JavaScript de browser. Ele controla login, navegacao entre telas, formularios, carrinho de venda, consultas, filtros, relatorios, backup pelo navegador e configuracoes visuais.

## Backend

O backend roda em Cloudflare Workers. Ele concentra as rotas HTTP, valida entradas, aplica regras de negocio, verifica permissoes e registra auditoria das acoes importantes.

## Banco de Dados

O banco utilizado e Cloudflare D1, baseado em SQLite. O schema e controlado por migrations, permitindo evoluir a estrutura com rastreabilidade.

Os valores monetarios sao armazenados internamente em centavos para evitar erro de ponto flutuante.

## Operacao

O projeto possui scripts para build, typecheck, migrations, backup, restore, sincronizacao, testes de API, smoke test e verificacao de seguranca.

