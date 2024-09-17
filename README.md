# Manual de Git + GitHub (Pratico e Rápido)

### Menu Rápido
[Topo](#manual-de-git--github-pratico-e-rápido) | [0. Ações rápidas](#0-ações-rápidas) | [1. O que é Git e GitHub](#1-o-que-é-git-e-github) | [2. Instalação do Git](#2-instalação-do-git) | [3. Configuração Inicial do Git](#3-configuração-inicial-do-git) | [4. Comandos do Git](#4-comandos-do-git) | [5. Comandos do Markdown](#5-comandos-do-markdown) | [6. Dicas úteis](#6-dicas-úteis)

## 0 Ações rápidas
    git config --global user.name "Seu Nome"
    git config --global user.email "seuemail@exemplo.com"
    git remote add origin https://github.com/usuario/repo.git

    git init
    git add README.md | git add .
    git commit -a -m "first commit"
    git branch -M main
    git remote add origin https://github.com/usuario/repo.git
    git push -u origin main | git push
    git pull

| **Comando Git**                  | **Funcionalidade**                                                  |
|-----------------------------------|---------------------------------------------------------------------|
| `git init`                        | Inicializa um novo repositório Git                                  |
| `git clone [url]`                 | Clona um repositório remoto                                         |
| `git status`                      | Verifica o estado dos arquivos no repositório                       |
| `git add [arquivo]`               | Adiciona um arquivo ao estágio                                      |
| `git commit -m "[mensagem]"`      | Cria um commit com as mudanças do estágio                           |
| `git pull`                        | Baixa e mescla mudanças do repositório remoto                       |
| `git push`                        | Envia mudanças para o repositório remoto                            |
| `git checkout [branch]`           | Troca para uma branch específica                                    |
| `git branch`                      | Lista as branches locais                                            |
| `git merge [branch]`              | Mescla as mudanças de uma branch na branch atual                    |


## 1. O que é Git e GitHub?
    Git: Um sistema de controle de versão distribuído que permite rastrear mudanças no código-fonte e colaborar com outras pessoas.
    GitHub: Uma plataforma baseada na web que hospeda repositórios Git, facilitando a colaboração e o compartilhamento de código.
    
    Links diversos
    [Comandos: https://comandosgit.github.io/] (https://comandosgit.github.io/)
    [Manual original: (https://git-scm.com/docs/user-manual.html)](https://git-scm.com/docs/user-manual.html)
    [Manual git em português produzido coletivamente: (https://git-na-pratica.gitbooks.io/git-na-pratica/content/)](https://git-na-pratica.gitbooks.io/git-na-pratica/content/)
    [Formatação padrão Markdown (http://daringfireball.net/projects/markdown/syntax)](http://daringfireball.net/projects/markdown/syntax)

## 2. Instalação do Git
    Windows: Baixe o Git em git-scm.com e siga as instruções de instalação.
    Iniciar o Git Bash na pasta do projeto ou entrar na pasta via comando CMD do prompt ou no VS

## 3. Configuração Inicial do Git

| **Comando Git**                                  | **Funcionalidade**                                        |
|--------------------------------------------------|-----------------------------------------------------------|
| `git config --global --list`                     | Mostra todas as configurações globais do Git              |
| `git config --global alias.[atalho] [comando]`   | Cria um atalho (alias) para um comando Git                |
| `git config --global user.name "Seu-Nome-Aqui`   |configure seu nome (obrigatórios para commit)              |
| `git config --global user.email "SeuEmailAqui`   |configure seu e-mail (obrigatórios para commit)            |
|--------------------------------------------------|-----------------------------------------------------------|
| `git remote add origin https://github.com/usuario/repo.git` | Conecta o repositório local a um repositório remoto no GitHub       |
| `git remote -v`                                  | verifica o link existente                                 |
| `git remote rm origin`                           | remove o link                                             |

        
## 4. Comandos do Git
### Essa tabela organiza os principais comandos do Git e suas funcionalidades para referência rápida!

| **Comando Git**                  | **Funcionalidade**                                                  |
|-----------------------------------|---------------------------------------------------------------------|
| `git init`                        | Inicializa um novo repositório Git                                  |
| `git clone [url]`                 | Clona um repositório remoto para o seu ambiente local               |
| `git status`                      | Mostra o estado dos arquivos no repositório (modificados, staged)   |
| `git add [arquivo]`               | Adiciona um arquivo ao staging (preparando para commit)             |
| `git add .`                       | Adiciona todos os arquivos modificados ao staging                   |
| `git commit -a -m "[mensagem]"`   | Cria um commit com as mudanças do staging                           |
| `git log`                         | Exibe o histórico de commits                                        |
| `git diff`                        | Mostra as diferenças entre arquivos não commitados                  |
| `git branch`                      | Lista todas as branches do repositório                              |
| `git branch [nome-da-branch]`     | Cria uma nova branch                                                |
| `git checkout [nome-da-branch]`   | Troca para uma branch específica                                    |
| `git checkout -b [nome-da-branch]`| Cria e troca para uma nova branch                                   |
| `git merge [nome-da-branch]`      | Mescla as mudanças de uma branch para a branch atual                |
| `git pull [origin] [branch]`      | Atualiza o repositório local com as mudanças do repositório remoto  |
| `git push [origin] [branch]`      | Envia (faz push) das mudanças para o repositório remoto             |
| `git remote add origin [url]`     | Conecta o repositório local a um repositório remoto no GitHub       |
| `git reset [arquivo]`             | Remove o arquivo do estágio (desfaz `git add`)                      |
| `git checkout -- [arquivo]`       | Desfaz mudanças em um arquivo não commitado                         |
| `git rebase [branch]`             | Reorganiza commits ao aplicar rebase da branch                      |
| `git tag -a [v1.0] -m "[msg]"`    | Cria uma tag anotada para marcar uma versão                         |
| `git push origin --tags`          | Envia tags criadas para o repositório remoto                        |
| `git rebase -i HEAD~[n]`          | Squash: combina vários commits em um só                             |


### Essa tabela complementa a anterior com comandos mais avançados e específicos, ampliando a funcionalidade para diferentes cenários no Git.

| **Comando Git**                                            | **Funcionalidade**                                                |
|--------------------------------------                      |-------------------------------------------------------------------|
| `git fetch [remote]`                                       | Baixa dados do repositório remoto, mas sem mesclar com a branch atual |
| `git merge --abort`                                        | Cancela um merge em andamento, voltando ao estado anterior        |
| `git stash`                                                | Armazena temporariamente as mudanças locais (sem fazer commit)    |
| `git stash apply`                                          | Aplica as mudanças guardadas com o `git stash`                    |
| `git stash pop`                                            | Aplica e remove as mudanças do stash                              |
| `git stash list`                                           | Lista as mudanças guardadas no stash                              |
| `git rm [arquivo]`                                         | Remove um arquivo do repositório e do sistema de arquivos         |
| `git mv [arquivo_antigo] [arquivo_novo]`                   | Renomeia ou move um arquivo                                       |
| `git show [commit]`                                        | Mostra os detalhes de um commit específico                        |
| `git blame [arquivo]`                                      | Mostra quem alterou cada linha de um arquivo                      |
| `git reflog`                                               | Exibe o histórico de referências, inclusive ações de checkout e reset |
| `git reset --hard [commit]`                                | Reseta o repositório para um commit específico, descartando mudanças |
| `git reset --soft [commit]`                                | Reseta para um commit específico, mantendo as mudanças no staging |
| `git bisect start`                                         | Inicia uma busca binária para encontrar um commit com bug         |
| `git bisect good [commit]`                                 | Marca um commit como "bom" no processo de bisect                  |
| `git bisect bad [commit]`                                  | Marca um commit como "ruim" no processo de bisect                 |
| `git cherry-pick [commit]`                                 | Aplica um commit específico em outra branch                       |
| `git remote -v`                                            | Exibe as URLs associadas aos repositórios remotos                 |
| `git branch -d [nome-da-branch]`                           | Deleta uma branch local                                           |
| `git push origin --delete [branch]`                        | Deleta uma branch no repositório remoto                           |
| `git tag -d [nome-da-tag]`                                 | Deleta uma tag local                                              |
| `git push origin :refs/tags/[nome-da-tag]`                 | Deleta uma tag no repositório remoto                           |
| `git config --global --list`                               | Mostra todas as configurações globais do Git                      |
| `git config --global alias.[atalho] [comando]`             | Cria um atalho (alias) para um comando Git                   |
| `git archive --format=zip --output=[arquivo.zip] [branch]` | Exporta o conteúdo de uma branch para um arquivo ZIP |
| `git rev-parse [HEAD]`                                     | Exibe o hash completo do commit atual                             |
| `git shortlog -s -n`                                       | Mostra o número de commits por autor                              |
| `git diff [branch1] [branch2]`                             | Compara diferenças entre duas branches                            |

## 5. Comandos do Markdown
### Essa tabela fornece os comandos mais comuns para formatação e estruturação de conteúdo em Markdown.
Markdown é uma linguagem de marcação simples que facilita a formatação de texto. Usada em documentos e plataformas como GitHub, ela permite criar títulos, listas, links e formatações básicas com uma sintaxe fácil de ler e escrever.

| **Comando Markdown**              | **Funcionalidade**                                             |
|-----------------------------------|----------------------------------------------------------------|
| `# Título`                        | Cria um título de nível 1 (equivalente a `<h1>`)               |
| `## Subtítulo`                    | Cria um título de nível 2 (equivalente a `<h2>`)               |
| `### Subsubtítulo`                | Cria um título de nível 3 (equivalente a `<h3>`)               |
| `**texto em negrito**`            | Deixa o texto em **negrito**                                   |
| `*texto em itálico*`              | Deixa o texto em *itálico*                                     |
| `> citação`                       | Cria um bloco de citação                                       |
| `- Item de lista`                 | Cria uma lista não ordenada (bullet points)                    |
| `1. Item numerado`                | Cria uma lista ordenada                                        |
| `[link](https://exemplo.com)`      | Cria um [link](https://exemplo.com)                            |
| `![alt texto](imagem.png)`         | Insere uma imagem                                              |
| `` `código` ``                    | Insere código inline                                           |
| \`\`\`                            | Marca o início de um bloco de código                           |
| \`\`\`                            | Marca o fim de um bloco de código                              |
| `---`                             | Cria uma linha horizontal (divisória)                          |
| `| Coluna 1 | Coluna 2 |`         | Cria uma tabela                                                |
| `![Descrição](caminho/imagem.jpg)` | Insere uma imagem com descrição alternativa                    |
| `- [ ] Tarefa`                    | Cria uma lista de tarefas                                      |
| `- [x] Tarefa concluída`          | Marca uma tarefa como concluída                                |

### Esses comandos complementam os anteriores e cobrem funcionalidades avançadas de Markdown, incluindo notas de rodapé, alinhamento em tabelas, e formatações especiais.

| **Comando Markdown**                    | **Funcionalidade**                                                    |
|-----------------------------------------|-----------------------------------------------------------------------|
| `~~texto~~`                             | Aplica **tachado** no texto                                           |
| `![alt text](url "Título da imagem")`   | Insere uma imagem com título ao passar o mouse sobre ela              |
| `[texto do link][id]`                   | Cria um link de referência (usando identificadores no final do texto) |
| `[id]: https://exemplo.com`             | Define a URL de referência para o link                                |
| `\*caracter especial\*`                 | Escapa caracteres especiais (não interpreta como Markdown)            |
| `| :--- | ---: | :---: |`              | Alinha o conteúdo da tabela: esquerda, direita, ou centralizado       |
| `- [ ] Item de tarefa`                  | Cria uma lista de tarefas não marcadas                                |
| `- [x] Item de tarefa concluída`        | Marca um item de tarefa como concluído                                |
| `---`                                   | Cria uma linha horizontal (divisória)                                 |
| `<br>`                                  | Quebra de linha manual                                               |
| `[^1]`                                  | Cria uma nota de rodapé no texto                                      |
| `[^1]: Texto da nota de rodapé`         | Define o conteúdo da nota de rodapé                                   |
| `::emoji::`                             | Insere emojis (suporte depende da plataforma)                         |
| `![Exemplo GIF](url.gif)`               | Insere um GIF animado                                                 |
| `[![Texto Alt](imagem.png)](url)`       | Insere uma imagem que funciona como link                              |
| `<mark>texto</mark>`                    | Marca o texto com cor de destaque (suporte depende da plataforma)     |
| `<sub>texto</sub>`                      | Formata texto como subscrito                                          |
| `<sup>texto</sup>`                      | Formata texto como sobrescrito                                        |

### Comandos adicionais (variantes ou extensões do Markdown):
| **Comando Markdown**                 | **Funcionalidade**                                                              |
|--------------------------------------|---------------------------------------------------------------------------------|
| `<u>texto</u>`                       | Sublinha o texto (suporte depende da plataforma)                                |
| `<kbd>Ctrl+C</kbd>`                  | Exibe um texto formatado como tecla (útil para atalhos de teclado)              |
| `<details><summary>Texto</summary>Conteúdo</details>` | Cria uma seção que pode ser expandida ourecolhida              |
| `==texto==`                          | Realça texto com uma cor de destaque (varia por plataforma)                     |
| `:emoji:`                            | Insere emojis por atalho de texto (suporte depende da plataforma)               |
| `<abbr title="exemplo">txt</abbr>`   | Cria uma abreviação com uma dica ao passar o mouse sobre o texto                |
| `<!–– comentário ––>`                | Insere um comentário invisível no Markdown                                      |
| `\LaTeX{fórmula}`                    | Insere fórmulas matemáticas usando sintaxe LaTeX (suporte em algumas plataformas)|
| `<iframe src="url"></iframe>`        | Insere um iframe para incorporar conteúdo de outros sites (suporte limitado)    |
| `<audio controls><source src="audio.mp3"></audio>` | Insere um player de áudio (suporte limitado)                      |
| `<video controls><source src="video.mp4"></video>` | Insere um player de vídeo (suporte limitado)                      |
| `<blockquote>`                       | Adiciona citações com formatação HTML                                           |
| `<table><tr><th>Header</th></tr></table>` | Cria tabelas mais personalizadas usando HTML                               |
| `[toc]`                              | Gera automaticamente um sumário com base nos títulos do documento (varia por plataforma) |
| `{#id}`                              | Adiciona um id a um título ou elemento para referência direta (Markdown estendido) |
| `@usuário`                           | Menciona um usuário (suporte comum em plataformas como GitHub)                  |
| `<script>` ou `<style>`              | Adiciona scripts ou estilos CSS (geralmente não permitido por razões de segurança) |


## 6. Dicas úteis
   - Crie um arquivo .gitignore para excluir arquivos ou pastas que você não quer versionar
        /node_modules
        *.log

    - existem três maneiras de obter a ajuda para qualquer um dos comandos Git
    git help {comando}
    git {comando} --help
    man git- {comando}
    - Markdown : (Menu de links internos) para pegar o link, selecione no Readme.md o texto e no browse copia o # atÃ© o final
     ``` [Bem vindo](#Bem-vind0....) ```


[Topo](#manual-de-git--github-pratico-e-rápido) 