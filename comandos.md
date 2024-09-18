<h1>
    <a href="https://www.dio.me/">
     <img align="center" width="40px" src="https://hermes.digitalinnovation.one/assets/diome/logo-minimized.png">
    </a>
    <span> Versionamento de Código com Git e GitHub</span>
</h1>

## Primeiros Passos com Git e GitHub

### Criando e Clonando Repositórios
Existem duas formas de obter um repositório Git na sua máquina:
1. Transformando um diretório local que não está sob controle de versão, num repositório Git;
2. Clonando um repositório Git existente.

#### Criando um Repositório Local
Acesse a pasta que deseja transformar em um repositório Git  pelo terminal ou clique no atalho em “Git Bash Here”:

1. Inicialize um repositório Git no diretório escolhido:
    ```bash
    git init
    ```
    #### Removendo repositorio git da pasta:
    ```bash
    rm -rf .git
    ```
2. Configurando usuario e email em um repositorio:
    #### Localmente
    ```bash
    git config user.name "Seu Nome"
    ```
    ```bash
     git config user.email "seu.email@example.com"
    ```
    #### Globalmente
    ```bash
    git config user.name "Seu Nome"
    ```
    ```bash
    git config user.email "seu.email@example.com"
    ```

3. #### Conecte o repositório local com o repositório remoto:
    ```bash
    $ git remote add origin https://github.com/username/nome-do-repositorio.git
    ```
    #### Execute e na próxima basta: git push para trazer do remoto
    ```bash
    git push -u origin main
    ```
    ou
4. #### Clone repositório remoto:
    Clonar todo repositorio
    ```bash
    git clone <URL> Novo-nome(Opcional) 
    ```
    apenas uma branch
    ```bash
    git clone URL --branch Nome-da-branch --single-branch
    ```
    
    

### Comandos Básicos

1. #### Verifição de status
    ```bash
    git status
    ```

1. #### Adicionando ao rastramento:
    #### Arquivo especifico
    ```bash
    git add <file.extesion>
    ```
    #### Todos arquivos da pasta
    ```bash
    git add .
    ```

1. #### Commitando arquivos rastreados
    ```bash
    git commit -m "Sua mensagem" 
    ```
    ##### Ou
    ```bash
    git commit 
    ```

1. #### Alterando a mensagem sem abrir o editor:  
    ```bash
    git commit --amend –m"nova mensagem"
    ```
1. #### Remove todos os arquivos nao comitados
    
    ```bash
    git reset <commit\branch>(opcional) --hard (opcional)
    ```
1. #### Arquivar modificações
    ```bash
    git stash
    ```

    1. Aplica as mudanças do stash e remove o stash da lista:
        ```bash
        git stash pop
    2. Aplica as mudanças do stash mas mantém o stash na lista:
        ```bash
        git stash apply
        ```
### Comando Avançados
    
1. #### Enviando commits para o repositório remoto (configure primeiro)
        
    ```bash
    git push
    ```
    
2. #### Trazendo commits do repositorio remota (configure primeiro)
    ```bash
    git pull
    ```

3. #### Visualizar commits
    ```bash
    git log
    ```
    #### ou
    ```bash
    git log --oneline
    ```

4. #### Mudar para branch\commit
    ```bash
    git checkout <commit\branch>
    ```
    
5. #### Baixar alterações sem modificar a branch local
    ```bash
    git fetch origin main <remoto>
    ```

6. #### verificar diferença
    ```bash
    git diff main origin/main
    ```

### BRANCH's

1. #### Criação de branch
        git branch nome-da-nova-branch
    
1. #### Renomear branch
        git branch -m nome-branch

1. #### Criar branch e acessa ao mesmo tempo:
        git checkout -b nome-da-nova-branch

1. #### Remover branch 
    1. #### Remover branch mesclada
        ```bash
        git branch -d nome-da-branch
        ```
    1. #### Remover branch independente de estar mesclada
        ```bash
        git branch -D nome-da-branch
        ```

1. #### Ver todas as branchs remotas
    ```bash        
    git branch -r
    ```

1. #### Fazer uma nova branch local com base na remota
    ```bash        
    git checkout -b branch-local origin/branch-remota
    ```

1. #### Fazer push de uma nova branch:
    ```bash        
    git push origin nome-da-branch-local
    ```

1. #### Remover branch do remoto
        git push origin --delete nome-da-branch
        

### Gitignore
Com o .gitignore é possivel colocar dentro dele arquivos para nao serem rastreados pelo git. Apos criar o .gitignore, caso o arquivo posto la esteja comitado, após executar, realize um commit:
```bash        
git rm --cached caminho/do/.gitignore
```

### EXTRA:
site para criação e visualização de markdown: https://readme.so/pt/editor

<div align="center">Créditos a <a href="https://github.com/elidianaandrade">Eli</a>.</div>