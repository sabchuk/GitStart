# **Obtendo um Repositório Git**

Você pode obter um projeto Git utilizando duas formas principais. 1. Você pode pegar um diretório local que atualmente não está sob controle de versão e transformá-lo em um repositório Git, ou 2. Você pode fazer um clone de um repositório Git existente em outro lugar.


# **Inicializado um repositório em um diretório existente**

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

# **Verificar o status de seus arquivos**

O comando **_git status_** te permite verificar o status de todos os arquivos do seu diretório. Esse comando te permite verificar o estado de cada arquivo.

Vamos voltar para a pasta e o arquivo _index.html_. Dentro da pasta criada, execute o comando:

```
git status
```

![Git status](./imagens/gitstatus.png)

Você pode ver que o seu novo arquivo _index.html_ é um arquivo não rastreado, porque está abaixo do subtítulo “Untracked files” na saída do seu status. "Não rastreado" basicamente significa que o Git vê um arquivo que você não tinha no snapshot (commit) anterior. Isso significa que em caso de realizar um procedimento para enviar o arquivo para um repositório remoto este arquivo irá ficar de fora.




