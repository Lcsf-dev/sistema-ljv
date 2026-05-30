# Seguranca e Operacao

## Seguranca Aplicada

- Senhas armazenadas com hash PBKDF2.
- Comparacao de senha em tempo constante.
- Tokens de sessao aleatorios.
- Apenas hash do token salvo no banco.
- Expiracao e renovacao de sessao.
- Limpeza de sessoes expiradas.
- Bloqueio temporario apos muitas falhas de login.
- Rate limit por usuario e IP.
- Permissoes por area do sistema.
- Auditoria de eventos sensiveis.
- Headers HTTP de seguranca.
- Senha inicial fora da configuracao publica.

## Auditoria

O sistema registra acoes importantes para rastreabilidade:

- Login e logout.
- Alteracao de configuracoes.
- Cadastro e edicao de usuarios.
- Vendas.
- Gastos.
- Movimentacoes de estoque.
- Backup.
- Reset do sistema.

## Automacao

O projeto possui scripts para:

- Build do frontend.
- Typecheck.
- Migrations locais e remotas.
- Verificacao do banco.
- Verificacao de seguranca.
- Smoke test.
- Testes de API.
- Backup e restore.
- Deploy.

## Estrategia de Publicacao

O codigo-fonte principal permanece privado. Este repositorio publico apresenta o projeto como case study tecnico, com imagens, arquitetura, estrutura e textos tecnicos suficientes para avaliacao sem expor uma copia operacional do sistema.

