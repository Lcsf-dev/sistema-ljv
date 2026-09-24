# 🧱 Arquitetura

O Sistema LJV é uma aplicação web serverless organizada em três responsabilidades principais: interface, serviços de aplicação e persistência de dados.

```text
Pessoa usuária
  → Interface web
  → Serviços serverless
  → Banco de dados
```

## Interface

A interface foi desenvolvida em TypeScript e reúne as áreas de vendas, estoque, financeiro, relatórios e administração. Ela oferece formulários, filtros, indicadores e tabelas voltados à operação diária.

## Serviços de aplicação

Os serviços serverless processam autenticação, validação de dados, regras de negócio, permissões e auditoria. Essa separação mantém as regras sensíveis fora do navegador.

## Dados

Os dados operacionais são persistidos em banco SQLite serverless. A evolução da estrutura é controlada por versionamento, o que favorece rastreabilidade e manutenção.

## Princípios adotados

- Segurança aplicada nas regras de negócio.
- Validação de dados entre interface e serviços.
- Separação entre apresentação, regras e dados.
- Rastreabilidade de ações relevantes.
- Evolução controlada da estrutura de dados.
