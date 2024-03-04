# Versionamento de Código com Git e GitHub

## Introdução

O versionamento de código é uma prática fundamental para o desenvolvimento de software, permitindo o controle e a gestão eficiente das diferentes versões de um código-fonte ao longo do tempo. Os sistemas de controle de versão (VCS) desempenham um papel central nesse processo, registrando o histórico de alterações, facilitando o trabalho colaborativo e garantindo a integridade do código.

### O que é versionamento de código?

O versionamento de código, também conhecido como controle de versão, refere-se ao processo de rastreamento e gerenciamento das alterações feitas em um arquivo ou conjunto de arquivos ao longo do tempo. Isso inclui informações como quem fez uma alteração, quando ela foi feita e quais foram as modificações realizadas.

Existem dois tipos principais de sistemas de controle de versão:

- **Sistemas de Controle de Versão Centralizados (CVCS)**: Nesses sistemas, há um único servidor que contém todos os arquivos e é responsável pelo controle de versão. Exemplos incluem CVS e Subversion.

- **Sistemas de Controle de Versão Distribuídos (DVCS)**: Esses sistemas duplicam localmente o repositório completo, incluindo o histórico de versões, em cada máquina de desenvolvedor. Isso oferece mais flexibilidade e recursos para trabalhar offline. Exemplos incluem Git e Mercurial.

## Git e GitHub

### O que é o Git?

O Git é um sistema de controle de versão distribuído de código-fonte, amplamente utilizado na indústria de desenvolvimento de software. Ele é conhecido por sua eficiência, velocidade e suporte robusto a fluxos de trabalho complexos. O Git permite que os desenvolvedores gerenciem projetos através de ramificações e fusões, facilitando o desenvolvimento colaborativo e a manutenção do código.

### O que é o GitHub?

O GitHub é uma plataforma de hospedagem de código que utiliza o Git como sistema de controle de versão. Ele oferece uma variedade de recursos para armazenar, colaborar e gerenciar projetos de software. Com uma ampla comunidade de desenvolvedores, o GitHub facilita a colaboração e o compartilhamento de código entre equipes distribuídas globalmente.

## Instalação e Configuração do Git

### Instalando o Git

#### Windows

1. Acesse [o site oficial do Git para Windows](https://git-scm.com/download/win).
2. Faça o download do instalador e execute-o.
3. Aceite a licença e siga as instruções do instalador.
4. Certifique-se de selecionar as opções "Git Bash Here" e "Git GUI Here" durante a instalação.

#### Linux (Ubuntu)

1. Verifique a documentação oficial do Git para Linux [aqui](https://git-scm.com/download/linux).
2. Instale a última versão estável do Git usando os comandos apropriados para seu sistema.

#### macOS

1. Consulte a documentação oficial do Git para macOS [aqui](https://git-scm.com/download/mac).
2. Instale o Homebrew, se ainda não estiver instalado.
3. Use o Homebrew para instalar o Git.

### Configurando o Git

Execute os seguintes comandos no terminal para configurar o Git:

```bash
$ git config --global user.name "Seu Nome"
$ git config --global user.email seuemail@example.com
$ git config --global init.defaultBranch main
```

## Primeiros Passos com Git e GitHub

### Criando e Clonando Repositórios

Existem duas formas principais de obter um repositório Git na sua máquina:

1. Transformando um diretório local em um repositório Git.
2. Clonando um repositório Git existente.

#### Criando um Repositório Local

1. Acesse a pasta que deseja transformar em um repositório Git pelo terminal.
2. Inicialize um repositório Git no diretório escolhido:
   ```bash
   $ git init
   ```
3. Conecte o repositório local com o repositório remoto:
   ```bash
   $ git remote add origin https://github.com/username/nome-do-repositorio.git
   ```

### Trabalhando com Branches

As branches no Git são ramificações do seu projeto que permitem o desenvolvimento paralelo de novas funcionalidades ou experimentos sem afetar o código principal na branch principal, geralmente chamada de "main" ou "master".

## Comandos Úteis do Git

### Clonar repositório
```
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY
```

### Clonar repositório a partir de uma branch específica
```
git clone -branch new_feature <repositorio>
```

### Inicializando
```
git init
```

### Adicionar arquivo a ser commit
- Ao invés de escrever o nome do arquivo/pasta eu posso utilizar o . para adicionar todas modificações
```
git add <nome_da_pasta>
```

### Verificar se há itens a serem commitados
```
git status
```

### Fazer commit
```
git commit -m "Inserir o commit aqui"
```

### Alterar a branch de master para main
```
git branch -M main
```

### Enviando os commits para o github
```
git push -u origin main
```

### Atualiza o projeto para última atualização feita
```
git pull
```

### Copia as alterações no repositório local do git
```
git fetch
```

### Mostra as alterções entre uma fonte e outra
- Essas fontes de dados podem ser commits, ramificações, arquivos e outros.
```
git diff
```

### Para ver os commits já feitos e seus id's
```
git log --oneline
```

### Retorna os commits de forma mais detalhada
```
git reflog 
```

### Para voltar a uma antiga alteração
- Utilizando o . irá voltar toda a aplicação para aquela alteração
- Para voltar apenas um arquivo devo colocar o nome do arquivo
```
git restore source <IdDoCommit> .
```

### Olhar as informações do autor daquele commit
```
git log --author="user_name"
```

### Criando uma nova branch
- Enquanto não fizer algo com a nova branch criada ela não irá para o github
```
git checkout -b <nome da branch>
```

### Alternando entre branchs
```
git switch <nome da branch>
```

### Enviar mudanças de uma branch para o principal
- Após enviar para o principal é necessário fazer um push
- É preciso estar na branch que irá receber os novos dados
```
git merge <nome da branch>
```

### Arquiva as modificações
- list - lista itens arquivados
- pop - remove ou joga fora o stash mais recente
- apply - mantém o arquivo na lista
```
git stash list | pop | apply
```

### Como desfazer um commit
```
$ git reset --soft | --mixed | --hard
```

### Como alterar a mensagem do último commit
```
$ git commit --amend
```
Alterando a mensagem sem abrir o editor:  
```
$ git commit --amend –m"nova mensagem"
```
