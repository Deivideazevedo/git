<h1>
    <a href="https://www.dio.me/">
     <img align="center" width="40px" src="https://hermes.digitalinnovation.one/assets/diome/logo-minimized.png">
    </a>
    <span> Configuração do Git com Vscode</span>
</h1>

## Primeiros Passos

Para configurar o Git para abrir o VS Code para resolver conflitos de merge

1. Configurar VS Code como o editor padrão do Git:
    ```bash
    git config --global core.editor "code --wait"
    ```
1. Configurar VS Code como a ferramenta de merge do Git:
    ```bash
    git config --global merge.tool vscode
    ```
    ```bash
    git config --global mergetool.vscode.cmd "code --wait \$MERGED"
    ```
1. Configurar VS Code como a ferramenta de diff do Git:
    ```bash
    git config --global diff.tool vscode
    ```
    ```bash
    git config --global difftool.vscode.cmd "code --wait --diff \$LOCAL \$REMOTE"
    ```


        
        

#### Quando houver conflitos de merge, use:
```bash
git mergetool BRANCH -- caminho/do/arquivo(opcional)
```
#### Quando quiser ver as diferenças, use:
```bash
git difftool COMMIT1 COMMIT2 -- caminho/do/arquivo
```
    
    