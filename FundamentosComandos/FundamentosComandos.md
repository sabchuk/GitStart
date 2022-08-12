# **Obtendo um Repositório Git**

Você pode obter um projeto Git utilizando duas formas principais. 1. Você pode pegar um diretório local que atualmente não está sob controle de versão e transformá-lo em um repositório Git, ou 2. Você pode fazer um clone de um repositório Git existente em outro lugar.


# **Inicializado um repositório em um diretório existente -  Git init**

Vamos criar uma pasta e depois iniciar o repositório git.

Criar um diretório:

```
mkdir site
```

Inicializar o git neste diretório:

```
git init
```

Após a inicialização do git nesta pasta repare que será criado um arquivo _.git_. Esse arquivo contem todos os arquivos necessários de seu repositório, um esqueleto.

```
ls -la 
```

![Git init](./imagens/gitinit.png)


Dentro desta pasta vamos criar um arquivo chamado _index.html_:

```
touch index.html
```

Neste tópico você consegiu perceber o uso do comando **_git init_**.

# **Verificar o status de seus arquivos - Git status**

O comando **_git status_** te permite verificar o status de todos os arquivos do seu diretório. Esse comando te permite verificar o estado de cada arquivo.

Vamos voltar para a pasta e o arquivo _index.html_. Dentro da pasta criada, execute o comando:

```
git status
```

![Git status](./imagens/gitstatus.png)

Você pode ver que o seu novo arquivo _index.html_ é um arquivo não rastreado, porque está abaixo do subtítulo “Untracked files” na saída do seu status. "Não rastreado" basicamente significa que o Git vê um arquivo que você não tinha no snapshot (commit) anterior. Isso significa que em caso de realizar um procedimento para enviar o arquivo para um repositório remoto este arquivo irá ficar de fora.


# **Git add**

Para começar a rastrear um novo arquivo, você deve usar o comando git add. Para começar a rastrear o arquivo README, você deve executar o seguinte:

```
git add index.html
```

Agora execute o comando _git status_ para verificar o estado atual do arquivo.

![Git add](./imagens/gitadd.png)

Veja que seu arquivo esta sendo rastreado e preparado (staged) para o commit.

Vamos adicionar nesta pasta mais um arquivo chamado _contact.index_.

Apos a criação do arquivo execute o comando _git status_ e veja como ficará:

![Git add files](./imagens/gitddfiles.png)

O arquivo contact.md aparece sob a seção “Changes not staged for commit” — que indica que um arquivo rastreado foi modificado no diretório de trabalho mas ainda não foi mandado para o stage (preparado).

Assim como foi feito para adicionar o arquivo anteriormente, execute o comando _git add_ para adicionar o arquivo contact.index no rastreamento.

Supondo que você precisou modificar algum destes arquivos, vamos ver como ficaria o estado do arquivo.

Para este cenário vamos inserir alguma coisa dentro do arquivo _index.html_.

![Git add files](./imagens/gitchangefile.png)

Repare que o estado do arquivo modificado esta justamente como "modified" e ainda esta com o estado de preparado para "committed".

Acontece que o Git põe um arquivo no stage exatamente como ele está no momento em que você executa o comando git add. Se você executar git commit agora, a versão do index.html que vai para o repositório é aquela de quando você executou git add, não a versão que está no seu diretório de trabalho. Se você modificar um arquivo depois de executar git add, você tem que executar git add de novo para por sua versão mais recente no stage.

Vamos adicionar essa alteração executando o comando _git add index.html_. Desta forma a sua modificação esta rastreada.


# **Git diff**

Com o comando _git diff_ você tem a possibilidade de comparar a diferença de um arquivo que você já adicionou para o commit e do estado de uma outra modificação. Para melhor compreender vamos montar o nosso cenário.

Altere o conteúdo do arquivo _contact.index_ insira qualquer texto dentro dele e depois execute o comando:

```
git diff
```
![Git diff](./imagens/gitdiff.png)

Esse comando compara o que está no seu diretório de trabalho com o que está no stage. O resultado permite que você saiba quais alterações você fez que ainda não foram mandadas para o stage.
Repare que no final dele você tem a informação do que esta sendo, no caso, adicionado.

Uma outra solução que pode te auxiliar na jornada de comparação do arquivo como estava e como ficou após a sua modificação é o comando:

```
git difftool
```
![Git difftool](./imagens/gitifftool.png)

# **Realizando o commit das modificações - Git commit**

