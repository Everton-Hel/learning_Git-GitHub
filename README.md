# Manual de Git + GitHub

## 1. O que é Git e GitHub?
    Git: Um sistema de controle de versão distribuído que permite rastrear mudanças no código-fonte e colaborar com outras pessoas.
    GitHub: Uma plataforma baseada na web que hospeda repositórios Git, facilitando a colaboração e o compartilhamento de código.

## 2. Instalação do Git
    Windows: Baixe o Git em git-scm.com e siga as instruções de instalação.

## 3. Configuração Inicial do Git
    Após a instalação, configure seu nome e e-mail (obrigatórios para commit):
        git config --global user.name "Seu Nome"
        git config --global user.email "seuemail@exemplo.com"

    Para verificar se a configuração foi bem-sucedida:
        Git git config --list 

## 4. Comandos Básicos do Git
    Aqui estão os principais comandos para iniciar no Git:
    init:   Para iniciar um novo repositório Git em um diretório
    clone:  Para clonar um repositório existente (por exemplo, de um projeto do GitHub)
    status: Para ver as mudanças feitas nos arquivos
    add   : Para adicionar todos os arquivos modificados
    commit: Salva as mudanças locais no repositório
    
        git init
        git clone https://github.com/usuario/repo.git
        git status
        git add .
        git commit -m "Mensagem explicando a mudança"



