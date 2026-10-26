# Changelog

Todas as alterações relevantes deste projeto são documentadas neste arquivo.

## [Unreleased]

- Registre aqui as próximas alterações confirmadas.
- Atualize a versão e a data de lançamento quando uma nova versão for publicada.

## [1.9.0] - 2026-10-26

### Adicionado
- Adicionada verificação de segurança no fluxo de publicação para evitar o vazamento inadvertido de credenciais e tokens.
- Adicionada integração de hooks com `pre-commit` para validação local de arquivos sensíveis.
- Adicionado script automatizado (`minimist-updater`) para atualização segura da dependência `minimist` para a versão `1.2.8` com preservação de backups e execução via `--ignore-scripts`.

### Corrigido
- Corrigidas pequenas inconsistências no carregamento de configurações do workspace.

### Alterado
- Atualizadas as dependências do projeto para as versões mais recentes, incluindo auditoria de segurança via `npm audit`.

## [1.8.0]
