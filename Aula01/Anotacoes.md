# Aula 01


## git init

É utilizado para inicializar um repositório Git em um diretório. Ele cria um novo repositório local, permitindo que você comece a versionar os arquivos desse projeto. Quando você executa esse comando, o Git cria um diretório oculto chamado .git, que contém todos os arquivos e metadados necessários para controlar as versões do projeto.

```` bash
git init
````
---
## git add

Pego um arquivo desconhecido, e digo para o git que eu conheço esse tal arquivo. Pois é responsável por adicionar alterações no seu projeto à "staging area" (área de preparação) antes de realizar um commit.

`````` bash
git add .
git add 'nomeDoArquivo'
``````

## git commit

É usado para salvar as alterações que foram adicionadas à staging area em um novo ponto de versão no histórico do repositório. Ao executar este comando, você registra permanentemente o estado atual do seu projeto, criando um snapshot que pode ser revisitado ou revertido no futuro.

---


`````` bash
git commit
``````

1.  O Vim abrirá. Pressione **i** para entrar no modo de inserção.

2.  Digite sua mensagem de commit.

3.  Pressione **Esc** para sair do modo de inserção.

4.  Digite **:wq** e pressione Enter para salvar e sair.

5.  Metódo ZALVA e ZAI:
shift + Z + Z (shit pois ira deixar Z maiusculo, pode usar capslock)

---
-   Faz um commit com um titulo, maneira rápida.

`````` bash
git commit -m "Titulo do commit"
``````

---
-   Faz um commit com um titulo, sua descrição, de maneira mas rápida.

`````` bash
git commit -M "Titulo do commit" -m "Descrição do commit"
``````

---
-   permite modificar o último commit, ajustando a mensagem ou incluindo arquivos esquecidos, sem criar um novo commit.

`````` bash
git commit --amend
``````


## git push
É utilizado para enviar as alterações confirmadas (commits) do seu repositório local para um repositório remoto, como o GitHub, GitLab ou Bitbucket.
`````` bash
git push
``````

---

## git log

Para exibir uma lista dos commits no repositório, incluindo informações como o hash do commit, autor, data e mensagem.
`````` bash
git log
``````
---

- Se você quer uma visualização mais compacta do histórico de commits, pode usar:
`````` bash
git log --oneline
``````
---

-Se você quiser ver o que foi modificado dentro dos arquivos em cada commit.
`````` bash
git log --stat
``````
---

# Aula 02


## git revert 

Esse comando é usado para desfazer mudanças de um commit específico criando um novo commit que anula as mudanças anteriores. Ao contrário de um reset, o histórico de commits permanece intacto.
`````` bash
git revert
``````