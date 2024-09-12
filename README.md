# Manual de Git + GitHub (Pratico e Rápido)

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
### Aqui estão os principais comandos para iniciar no Git:
#### INIT - CLONE - STATUS - DIFF - ADD - COMMIT
    Para iniciar um novo repositório Git em um diretório
         git init 
    Para clonar um repositório existente (baixa o REPO do GitHub para sua máquina)
        git clone https://github.com/usuario/repo.git
    Para ver as mudanças feitas nos arquivos
        git status
    Informa as linhas exatas que foram alteradas
        git diff
        git diff --cached
    Para adicionar o monitoramento de todos os arquivos modificados
        git add .
    Salva as mudanças locais no repositório
        git commit -a -m "Mensagem explicando a mudança"

### BRANCHES - CHECKOUT - MERGE - RESET - REFLOG - LOG - PUSH - FETCH - PULL:
    verifica as branch existentes
        git branch
    Para criar uma nova branch
        git branch nome-da-branch
    Para mudar de branch
        git checkout nome-da-branch
    Serve para deletar a brench
        git branch -d <NomeDaBrench>
        git branch --delete <NomeDaBrench>
    Aqui vc irá navegar entre as branchs
        git checkout <NomeDaBranch>
    Para criar e trocar de branch ao mesmo tempo
        git checkout -b nome-da-branch
    Para mesclar as mudanças de outra branch para a branch atual
        git merge nome-da-branch
    Para visualizar os hashs - Recuperando commit apagado pelo git reset        
        git reflog
    Para Desfazer as ações, retornando para o original da main
        git reset --hard origin/main
    Para voltar ao último commit e mantém os últimos arquivos no Stage:
        git reset --soft HEAD~1
    Volta para o commit com a hash XXXXXXXXXXX:
        git reset --hard XXXXXXXXXXX
    Para ver a lista com histórico de commits existente
        git log
    Para enviar suas mudanças locais (main/BRANCH) para o repositório no GitHub (main)
        git push
        git push -u origin nome-da-branch
    Verificar na repo github se existe alguma branch nova
        git fetch -a
    Para baixar as mudanças do repositório remoto
        git pull
        git pull origin nome-da-branch
#### RM - MV - 
    Para remover um arquivo do Git e removê-lo dos arquivos que estão sendo monitorados 0 '-f' força a ação
        git rm -f nome-do-arquivo
    Para mover um arquivo especifico
        git mv "arquivo.css NovaPasta/arquivo.css"
    Se você quiser renomear um arquivo no Git
        git mv arquivo_origem arquivo_destino

## 5. Dicas úteis
    Crie um arquivo .gitignore para excluir arquivos ou pastas que você não quer versionar
        /node_modules
        *.log

    existem três maneiras de obter a ajuda para qualquer um dos comandos Git
    git help {comando}
    git {comando} --help
    man git- {comando}

