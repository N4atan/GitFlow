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

---

## git commit

É usado para salvar as alterações que foram adicionadas à staging area em um novo ponto de versão no histórico do repositório. Ao executar este comando, você registra permanentemente o estado atual do seu projeto, criando um snapshot que pode ser revisitado ou revertido no futuro.




`````` bash
git commit
``````

>1.  O Vim abrirá. Pressione **i** para entrar no modo de inserção.

>2.  Digite sua mensagem de commit.

>3.  Pressione **Esc** para sair do modo de inserção.

>4.  Digite **:wq** e pressione Enter para salvar e sair.

>5.  Metódo ZALVA e ZAI:
shift + Z + Z (shit pois ira deixar Z maiusculo, pode usar capslock)

`````` bash
# Faz um commit com um titulo, maneira rápida:
git commit -m "Titulo do commit"


#Faz um commit com um titulo, sua descrição, de maneira mas rápida.
git commit -M "Titulo do commit" -m "Descrição do commit"
``````


-   Permite modificar o último commit, ajustando a mensagem ou incluindo arquivos esquecidos, sem criar um novo commit.

`````` bash
git commit --amend
``````


## git push
É utilizado para enviar as alterações confirmadas (commits) do seu repositório local para um repositório remoto, como o GitHub, GitLab ou Bitbucket.
`````` bash
git push
git push -f #Irá forcar o push
``````

---

## git log

Para exibir uma lista dos commits no repositório, incluindo informações como o hash do commit, autor, data e mensagem.
`````` bash
git log

git log --oneline   #Se você quer uma visualização mais compacta do histórico de commits.

git log --stat  #-Se você quiser ver o que foi modificado dentro dos arquivos em cada commit.
``````
---

# Aula 02


## git revert 

Esse comando é usado para desfazer mudanças de um commit específico criando um novo commit que anula as mudanças anteriores. Ao contrário de um reset, o histórico de commits permanece intacto.
`````` bash
git revert
``````  

## git restore 
É usado para desfazer alterações em arquivos no diretório de trabalho (working directory), revertendo-os para o estado em que estavam no último commit. Isso remove quaisquer mudanças não salvas ou não adicionadas ao staging, mas não afeta a área de staging.
`````` bash
git restore
`````` 

- É usado para remover arquivos da área de staging (index) sem excluir ou modificar os arquivos no diretório de trabalho. Ele basicamente desfaz o comando `git add`, movendo as mudanças de volta para a área de trabalho, mas sem perder o conteúdo alterado.
`````` bash
git restore --staged
`````` 

## git tag
No Git, uma `tag` é uma referência fixa a um ponto específico na história do repositório, geralmente usada para marcar versões ou lançamentos de um projeto. As tags são úteis para identificar versões importantes de um software, como v1.0, v2.0, etc., permitindo que você retorne facilmente a esses pontos no futuro.

- **Tag leve:** É simplesmente um ponteiro para um commit específico e não contém informações adicionais.
`````` bash
git tag "tagname"
`````` 

- **Tag anotada:** É uma tag que é armazenada como um objeto completo no repositório Git, contendo informações como o autor, data e uma mensagem de tag, semelhante a um commit.
`````` bash
git tag "tagname" -m "descrição"
`````` 
- **Possibilidades:**
`````` bash
# Ver tags:
git tag 
git tag -l "1.*"    #Irá buscar todas que começam com 1.


# Push de tags:
git push --tags     #Subira todas as tags


# Deletar tag:
git tag -d "tagname"               # Remove a tag localmente
git push --delete origin v1.0  # Remove a tag do repositório remoto


# Em um `commit` especifico:
git tag -a tag-name commit-id -m "Mensagem da tag"
``````