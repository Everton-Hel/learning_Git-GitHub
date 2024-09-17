# Manual de Git + GitHub (Pratico e Rápido)


## 0 Ações rápidas
    git init
    git add README.md | git add .
    git commit -a -m "first commit"
    git branch -M main
    git remote add origin https://github.com/usuario/repo.git
    git push -u origin main | git push
    git pull

## 1. O que é Git e GitHub?
    Git: Um sistema de controle de versão distribuído que permite rastrear mudanças no código-fonte e colaborar com outras pessoas.
    GitHub: Uma plataforma baseada na web que hospeda repositórios Git, facilitando a colaboração e o compartilhamento de código.
    
    Links diversos
    Comandos: https://comandosgit.github.io/
    Manual original: https://git-scm.com/docs/user-manual.html
    Manual git em português produzido coletivamente: https://git-na-pratica.gitbooks.io/git-na-pratica/content/
    Formatação padrão Markdown (http://daringfireball.net/projects/markdown/syntax);

## 2. Instalação do Git
    Windows: Baixe o Git em git-scm.com e siga as instruções de instalação.
    Iniciar o Git Bash na pasta do projeto ou entrar na pasta via comando CMD do prompt ou no VS

## 3. Configuração Inicial do Git
    Após a instalação, configure seu nome e e-mail (obrigatórios para commit):
        git config --global user.name "Seu Nome"
        git config --global user.email "seuemail@exemplo.com"

    Para verificar se a configuração foi bem-sucedida:
        Git git config --list 

    Conectando ao Repo do GitHub
        git remote add origin https://github.com/usuario/repo.git
    verifica o link existente
        git remote -v
    remove o link
        git remote rm origin
        
## 4. Comandos Básicos do Git
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
|-----------------------------------|---------------------------------------------------------------------|

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
|------------------------------------------------------------|-------------------------------------------------------------------|


## 5. Dicas úteis
    Crie um arquivo .gitignore para excluir arquivos ou pastas que você não quer versionar
        /node_modules
        *.log

    existem três maneiras de obter a ajuda para qualquer um dos comandos Git
    git help {comando}
    git {comando} --help
    man git- {comando}

