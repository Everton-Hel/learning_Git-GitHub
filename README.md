# Manual de Git + GitHub (Pratico e Rápido)

## 1. O que é Git e GitHub?
    Git: Um sistema de controle de versão distribuído que permite rastrear mudanças no código-fonte e colaborar com outras pessoas.
    GitHub: Uma plataforma baseada na web que hospeda repositórios Git, facilitando a colaboração e o compartilhamento de código.
    
    Links diversos
    Manual original: https://git-scm.com/docs/user-manual.html
    Manual git em português produzido coletivamente: https://git-na-pratica.gitbooks.io/git-na-pratica/content/
    Formatação padrão Markdown (http://daringfireball.net/projects/markdown/syntax);

## 2. Instalação do Git
    Windows: Baixe o Git em git-scm.com e siga as instruções de instalação.

## 3. Configuração Inicial do Git
    Após a instalação, configure seu nome e e-mail (obrigatórios para commit):
        git config --global user.name "Seu Nome"
        git config --global user.email "seuemail@exemplo.com"

    Para verificar se a configuração foi bem-sucedida:
        Git git config --list 

    Conectando ao Repo do GitHub
        git remote add origin https://github.com/usuario/repo.git
        

## 4. Comandos Básicos do Git
### Aqui estão os principais comandos para iniciar no Git:
#### INIT - CLONE - STATUS - ADD - COMMIT
    Para iniciar um novo repositório Git em um diretório
         git init 
    Para clonar um repositório existente (por exemplo, de um projeto do GitHub
        git clone https://github.com/usuario/repo.git
    Para ver as mudanças feitas nos arquivos
        git status
    Para adicionar todos os arquivos modificados
        git add .
    Salva as mudanças locais no repositório
        git commit -a -m "Mensagem explicando a mudança"

### BRANCHES - CHECKOUT - MERGE - RESET - LOG - PUSH - PULL:
    Para criar uma nova branch
        git branch nome-da-branch
    Para mudar de branch
        git checkout nome-da-branch
    Para criar e trocar de branch ao mesmo tempo
        git checkout -b nome-da-branch
    Para mesclar as mudanças de outra branch para a branch atual
        git merge nome-da-branch
    Para remover um arquivo da área de stage
        git reset arquivo.txt
    Para ver a lista de commits feitos no repositório
        git log        
    Para enviar suas mudanças locais (main) para o repositório no GitHub (main)
        git push
        git push -u origin nome-da-branch
    Para baixar as mudanças do repositório remoto
        git pull
        git pull origin nome-da-branch

## 5. Dicas úteis
    Crie um arquivo .gitignore para excluir arquivos que você não quer versionar
        /node_modules
        *.log

