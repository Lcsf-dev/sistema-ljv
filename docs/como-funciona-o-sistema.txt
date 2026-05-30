Como o Sistema Funciona
=======================

1. O usuario acessa o sistema pelo navegador.
2. O Cloudflare Worker entrega os arquivos estaticos da interface.
3. O frontend em TypeScript faz chamadas para endpoints /api.
4. O Worker valida autenticacao, permissao e dados recebidos.
5. As operacoes sao executadas no Cloudflare D1.
6. Acoes importantes sao registradas em auditoria.
7. A interface atualiza as telas de vendas, estoque, financeiro, relatorios e configuracoes.

O sistema foi pensado para ser simples de operar e facil de publicar. O mesmo projeto contem frontend, backend, migrations, scripts de verificacao, backup e deploy.

Areas principais:

- Vendas: PDV, carrinho, consulta e edicao.
- Estoque: produtos e movimentacoes.
- Financeiro: gastos, faturamento e resumo mensal.
- Relatorios: indicadores por periodo.
- Usuarios: controle de acesso por permissoes.
- Auditoria: rastreabilidade das acoes sensiveis.
- Backup: exportacao e restauracao em SQL.

