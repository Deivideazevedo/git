<h1>
    <a href="https://www.dio.me/">
     <img align="center" width="40px" src="https://hermes.digitalinnovation.one/assets/diome/logo-minimized.png">
    </a>
    <span> Versionamento de Código com Git e Vscode</span>
</h1>

## Primeiros Passos

Para criação e configuração da chave ssh da maquina e github

1. #### Verificar Chaves SSH Existentes:
    ```bash
    ls -al ~/.ssh
    ```
1. #### Criar uma Nova Chave SSH:
    ```bash
    ssh-keygen -t ed25519 -C "your_email@example.com"
    ```
    #### ou se nao for compativel, use:
    ```bash
    ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
    ```
    por fim coloque uma senha para o ssh apos inserir o email
    <br><br>

1. #### Pegando a chave SSH publica:
    ```bash
    cat ~/.ssh/id_ed25519.pub
    ```
    #### ou
    ```bash
    cat ~/.ssh/id_rsa.pub
    ```
    #### ou para copiar logo
    ```bash
    cat ~/.ssh/id_ed25519.pub | clip
    ```
  

1. #### Configurar VS Code como a ferramenta de diff do Git:
    ```bash
    git config --global diff.tool vscode
    ```
    ```bash
    git config --global difftool.vscode.cmd "code --wait --diff \$LOCAL \$REMOTE"
    ```
1. **Adicionar a Chave SSH ao ssh-agent** para nao colocar a senha toda vez sempre que reiniciar o pc
    #### Inicie o ssh-agent em segundo plano:
    ```bash
    eval "$(ssh-agent -s)"
    ```
    #### Adicione sua chave SSH ao ssh-agent:
    ```bash
    ssh-add ~/.ssh/id_ed25519
    ```
    #### Se criou uma chave RSA, use:
    ```bash
    ssh-add ~/.ssh/id_rsa
    ```       
    <br>
## Configurando key no github
1. Vá para Configurações de SSH e GPG keys na sua conta do GitHub.
2. Clique em "New SSH key" (Nova chave SSH), dê um título à chave e cole a chave SSH na caixa "Key".
3. Clique em "Add SSH key" (Adicionar chave SSH).
        

#### Testar a Conexão SSH:
```bash
ssh -T git@github.com
```
### Configurar o Git para Usar a Chave SSH
```bash
git clone git@github.com:username/repository.git
```




    
    