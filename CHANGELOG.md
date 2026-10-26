# Changelog

Todas as alterações relevantes deste projeto são documentadas neste arquivo.

## [Unreleased]

- Registre aqui as próximas alterações confirmadas.
- Atualize a versão e a data de lançamento quando uma nova versão for publicada.

## [1.8.0]

- Corrigido erro que poderia ocorrer quando não existia um remote `origin` (#63).
- Adicionado suporte à publicação no Open VSX (#115).
- Atualizadas as dependências.

## [1.7.1]

- Adicionada solução alternativa para o problema #88, relacionado a erros ao carregar projetos do diretório pessoal no Ubuntu.
- Otimizado o método `getProjectPath` (PR #87, por [@KyrychukD](https://github.com/KyrychukD)).

## [1.7.0]

- Corrigido o problema #78, em que a extensão apontava para o diretório de configuração incorreto no VS Code OSS (PR #79, por [@alyyasser](https://github.com/alyyasser)).
- Alterado o atalho `gitProjectManager.openRecents`, que entrava em conflito com o atalho de logout no macOS (PR #82, por [@timlogemann](https://github.com/timlogemann)).
- Corrigido um erro que impedia o carregamento da extensão em alguns casos (PR #83, por [@Tedyst](https://github.com/Tedyst)).
- Adicionada a opção `displayProjectPath`, que permite exibir os caminhos dos projetos independentemente do valor de `checkRemoteOrigin` (issue #80, PR #84, por [@KyrychukD](https://github.com/KyrychukD)).

## [1.6.0]

- Corrigida a abertura de projetos em uma nova janela: quando não há uma pasta no workspace atual, o projeto é aberto na janela atual (#71).
- Documentado o valor padrão de profundidade máxima da recursão no README (PR #74, por @andys8).
- Melhorada a apresentação das capturas de tela (PR #70, por @Tyriar).
- Corrigido um erro de digitação no README (PR #69, por @a-sync).

## [1.5.1]

- Corrigida a duplicação de projetos encontrados em diferentes diretórios-base (issue #68, por @Tyriar).

## [1.5.0]

- Adicionado suporte a projetos Mercurial e SVN (issue #62).

## [1.4.0]

- Adicionada compatibilidade com o caminho do diretório pessoal do Windows (PR #54, por [@DamonOehlman](https://github.com/DamonOehlman)).
- Corrigida mensagem relacionada à issue #56 (por [@DavidDeSloovere](https://github.com/DavidDeSloovere)).

## [1.3.2]

- Corrigido erro de digitação em uma mensagem (PR #51, por [@aaron7](https://github.com/aaron7)).
- Corrigido o problema #50: utilização do diretório de configuração do VS Code Insiders (reportado por @Tyriar).

## [1.3.1]

- Corrigido o problema #50, em que `MaxDepthRecursion` não funcionava (reportado por @Tyriar).
- Corrigido o problema #49, em que as informações do repositório não eram exibidas (reportado por @Tyriar).

## [1.3.0]

- Adicionada configuração para interromper a busca em níveis mais profundos após encontrar um projeto, ignorando `MaxDepthRecursion` (#47).
- Refatoradas as classes `GitProjectLocator` e `GitProjectManager` para receberem configurações por injeção de dependência, facilitando os testes.

## [1.2.1]

- Corrigidas informações sobre os atalhos de teclado no macOS (PR #45, por @kaiwood).
- Corrigido o problema #44, relacionado ao funcionamento de `storeRepositoriesBetweenSessions` ao carregar dados do cache.

## [1.2.0]

- Adicionado suporte a subpastas (#34).
- Realizadas diversas refatorações para melhorar a estabilidade e o desempenho.

## [1.1.0]

- Adicionado comando para abrir um projeto em uma nova janela (#39).
- Corrigido um problema em que as informações de atualização na barra de status não eram removidas (PR #38, por @zackschuster).

## [1.0.1]

- Corrigido o problema #36, removendo o callback de promessa da execução do comando (por [@Tyriar](https://github.com/Tyriar)).

## [1.0.0]

- Adicionado o comando `GPM - Open Recent Git Project`, permitindo abrir projetos Git recentes com mais rapidez.

## [0.1.18]

- Corrigido o problema [#32](https://github.com/felipecaputo/git-project-manager/issues/32), relacionado ao tratamento de links simbólicos.

### [0.1.17]

- Correção emergencial para o erro de publicação introduzido na versão 0.1.16.

### [0.1.16]

- Corrigido o problema [#31](https://github.com/felipecaputo/git-project-manager/issues/31): o alias `~` do Linux não era considerado uma variável de ambiente.

### [0.1.15]

- Reconhecidas as contribuições de @Tyriar para a resolução de problemas:
  - [#24](https://github.com/felipecaputo/git-project-manager/issues/24): restaurado o `QuickPick` baseado em promessas, removido na versão 0.1.14.
  - [#21](https://github.com/felipecaputo/git-project-manager/issues/21): ordenada a lista de projetos.
  - [#16](https://github.com/felipecaputo/git-project-manager/issues/16): corrigido o comportamento que mantinha repositórios removidos da configuração na lista de projetos.
  - [#13](https://github.com/felipecaputo/git-project-manager/issues/13): adicionada a análise de variáveis de ambiente na configuração das pastas de projetos.
  - [#11](https://github.com/felipecaputo/git-project-manager/issues/11): atualização automática da lista de projetos após alterações na configuração.
- Registrada também a atualização automática da lista de projetos relacionada à [issue #10](https://github.com/felipecaputo/git-project-manager/issues/10).
- Realizadas melhorias de experiência do usuário relacionadas às issues [#12](https://github.com/felipecaputo/git-project-manager/issues/12) e [#14](https://github.com/felipecaputo/git-project-manager/issues/14).

### [0.1.14]

- Adicionada correção temporária para as issues #8 e #9: o `ShowQuickPick` não funcionava corretamente ao receber promessas. Como efeito colateral, a lista de seleção só era exibida após a conclusão da busca em todas as pastas.

### [0.1.13]

- Correção emergencial para o problema da versão 0.1.12, que não respeitava a configuração `gitProjectManager.openInNewWindow`.

### [0.1.12]

- Atualizada a API do VS Code utilizada para abrir pastas, evitando problemas com caminhos e configurações.
- Adicionada configuração para escolher entre abrir o projeto na janela atual ou em uma nova janela.

### [0.1.11]

- Alterada a exibição para mostrar somente o nome da pasta em vez do caminho completo.
- Quando `checkRemoteOrigin` é `false`, o caminho passa a ser exibido como descrição na lista de seleção, em vez da origem remota.
- Alterada a forma de configurar `codePath`.

### [0.1.10]

- Adicionada a configuração `gitProjectManager.checkRemoteOrigin`, que permite desativar a verificação da origem remota para melhorar o desempenho.

### [0.1.9]

- Corrigido um erro no gerenciamento de dependências no VS Code.

### [0.1.8]

- Melhoradas as mensagens de erro.

### [0.1.7]

- Corrigido um problema com a configuração do VS Code que alterava o valor padrão de uma configuração do tipo array.

### [0.1.6]

- Corrigido o problema #2, que continuava sem funcionar na versão 0.1.5.

### [0.1.5]

- Adicionadas duas configurações para resolver o problema #2 e melhorar o desempenho:
  - `maxDepthRecursion`
  - `ignoredFolders`

### [0.1.4]

- Corrigido parcialmente o problema #1, com agradecimento a @martinpengellyphillips pela contribuição no PR #3, que permitiu configurar o caminho da aplicação de código.
