# Versionamento de Código com Git e GitHub

# O que é versionamento de código

- VCS = Version Controll System
- Software de controle de versão
- Resgistra histórico de versão de um arquivo
- Gerencia quais alterações, a data, autor e etc…

## Tipos de sistemas de controles de versão

| Sistema | Descrição | Exemplo |
| ------- | ----------| ------- |
| Centralizado (CVCS) | Um único servidor onde vai conter todos os arquivos responsável pelo controler de versão. | CVS, Subversion |
| Distribuído (DVCS) | Duplica localmente o repositório completo, incluindo o histórico de versões. | Git, Mercurial |

# O que é o Git
O Git é um sistema de controle de versão distribuído de código-fonte, conhecido por sua natureza Open Source. Ele permite o gerenciamento eficiente de projetos através de ramificações (branching) e fusões (merging), facilitando o trabalho colaborativo de equipes de desenvolvimento. Além disso, o Git é reconhecido por sua leveza e rapidez, tornando-o uma escolha popular para o desenvolvimento de software.

# O que é GitHub

O GitHub é uma plataforma de hospedagem de código amplamente utilizada, oferecendo serviços para armazenar, colaborar e gerenciar projetos de software. Com uma comunidade ativa de desenvolvedores, o GitHub facilita a colaboração e o compartilhamento de código entre programadores de todo o mundo. Além disso, é famoso por seu mascote "Octocat", que se tornou um símbolo reconhecível da plataforma.

# Como instalar e configurar o Git

### Instalando o Git no Windows
- Acesse < https://git-scm.com/download/win >;
- Faça o download do instalador e execute;
- Aceite a licença e clique em “Next”, e siga configurando como desejar e clicando em “Next”;
- Finalize clicando em “Install”, e “Finish”.

Em "Select Components“, deixe as opções “Git Bash Here” e “Git GUI Here” marcadas.

##

### Instalando o Git no Linux (Ubuntu)
- Confira a doc.: < https://git-scm.com/download/linux >;
- Instale a última versão estável do Git:
    ```bash
    # add-apt-repository ppa:git-core/ppa
    ```
    ```bash
    # apt update
    ```
    ```bash
    # apt install git
    ```
##

### Instalando o Git no macOS
- Confira a doc.: < https://git-scm.com/download/mac>;
- Instale o Homebrew: < https://brew.sh/ >;
- Instale o Git:
    ```
    $ brew install git
    ```
##

### Configurando o Git
```bash
$ git config --list
```

#### Configurando seu nome de usuário e e-mail (globalmente):
```bash
$ git config --global user.name "Nome Sobrenome"
$ git config --global user.email seuemail@email.com
```
#### Configurando o nome da Branch Padrão:
```bash
$ git config --global init.defaultBranch main
```

# Primeiros Passos com Git e GitHub

## Criando e Clonando Repositórios
Existem duas formas de obter um repositório Git na sua máquina:
1. Transformando um diretório local que não está sob controle de versão, num repositório Git;
2. Clonando um repositório Git existente.

## Criando um Repositório Local
Acesse a pasta que deseja transformar em um repositório Git  pelo terminal ou clique no atalho em “Git Bash Here”:
1. Inicialize um repositório Git no diretório escolhido:
    ```bash
    $ git init
    ```
2. Conecte o repositório local com o repositório remoto:
    ```bash
    $ git remote add origin https://github.com/username/nome-do-repositorio.git
    ```

# Trabalhando com branches

- Branch (em tradução “ramo”), é uma ramificação do seu projeto
- Funciona como um universo paralelo para que possa ser feito testes ou desenvolver novas funções no código sem que afete o código principal na branch main/master

# Comandos

## Clonar repositório
```
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY
```

## Clonar repositório a partir de uma branch específica
```
git clone -branch new_feature <repositorio>
```

## Inicializando
```
git init
```

## Adicionar arquivo a ser commit
- Ao invés de escrever o nome do arquivo/pasta eu posso utilizar o . para adicionar todas modificações
```
git add <nome_da_pasta>
```

## Verificar se há itens a serem commitados
```
git status
```

## Fazer commit
```
git commit -m "Inserir o commit aqui"
```

## Alterar a branch de master para main
```
git branch -M main
```
## Enviando os commits para o github
```
git push -u origin main
```

## Atualiza o projeto para última atualização feita
```
git pull
```

## Copia as alterações no repositório local do git
```
git fetch
```

## Mostra as alterções entre uma fonte e outra
- Essas fontes de dados podem ser commits, ramificações, arquivos e outros.
```
git diff
```

## Para ver os commits já feitos e seus id's
```
git log --oneline
```

## Retorna os commits de forma mais detalhada
```
git reflog 
```

## Para voltar a uma antiga alteração
- Utilizando o . irá voltar toda a aplicação para aquela alteração
- Para voltar apenas um arquivo devo colocar o nome do arquivo
```
git restore source <IdDoCommit> .
```

## Olhar as informações do autor daquele commit

```
git log --author="user_name"
```

## Criando uma nova branch
- Enquanto não fizer algo com a nova branch criada ela não irá para o github
```
git checkout -b <nome da branch>
```

## Alternando entre branchs
```
git switch <nome da branch>
```

## Enviar mudanças de uma branch para o principal
- Após enviar para o principal é necessário fazer um push
- É preciso estar na branch que irá receber os novos dados
```
git merge <nome da branch>
```

## Arquiva as modificações
- list - lista itens arquivados
- pop - remove ou joga fora o stash mais recente
- apply - mantém o arquivo na lista
```
git stash list | pop | apply
```

## Como desfazer um commit
```
$ git reset --soft | --mixed | --hard
```

## Como alterar a mensagem do último commit
```
$ git commit --amend
```
Alterando a mensagem sem abrir o editor:  
```
$ git commit --amend –m"nova mensagem"
```
