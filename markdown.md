<!-- <h1>
    <a href="https://www.dio.me/">
     <img align="center" width="40px" src="https://hermes.digitalinnovation.one/assets/diome/logo-minimized.png"></a>
    <span> Versionamento de Código com Git e GitHub</span>
</h1> -->

## Primeiros Passos com Git e GitHub

### Criando e Clonando Repositórios
Existem duas formas de obter um repositório Git na sua máquina:
1. Transformando um diretório local que não está sob controle de versão, num repositório Git;
2. Clonando um repositório Git existente.

#### Criando um Repositório Local
Acesse a pasta que deseja transformar em um repositório Git  pelo terminal ou clique no atalho em “Git Bash Here”:
1. Inicialize um repositório Git no diretório escolhido:
    ```bash
    $ git init
    ```
2. Conecte o repositório local com o repositório remoto:
    ```bash
    $ git remote add origin https://github.com/username/nome-do-repositorio.git
    ```
##

### Desfazendo Alterações no Repositório Local

#### Como alterar a mensagem do último commit
```bash
$ git commit --amend
```
Alterando a mensagem sem abrir o editor:  
```bash
$ git commit --amend –m"nova mensagem"
```

#### Como desfazer um commit
```bash
$ git reset
```
```bash
$ git reset --soft
```
```bash
$ git reset --mixed
```
```bash
$ git reset --hard
```

##
<div align="center">Créditos à <a href="https://github.com/elidianaandrade">Eli</a>.</div>
