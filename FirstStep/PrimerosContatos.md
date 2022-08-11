# **Passos inicias**

Com o git instalado, vamos realizar algumas configurações iniciais no ambiente Git. Essas alterações so tem a necessidade de serem feitas apenas uma vez e elas podem mudá-las a qualquer momento.

Vamos configurar a sua identida. Essa configuração permite indicar nome e email onde ela irá informar a sua identidade nos commits (vamos falar a respeito futuramente).

No seu terminal, execute:

```
git config --global user.name "Fulano de Tal"
```

```
git config --global user.email fulanodetal@exemplo.br
```

Apos esse procedimento execute o comando abaixo para visualizar as informaçoes configuradas.

```
git config --list
```

Output
```
user.name=Ricardo Capeli
user.email=ricardo.capeli@pteor.com
```

Existem outros parâmetro que podem ser adicionados e configurados no git config. Caso queira saber mais basta executar:

```
git help config
```

Ou para pesquisar alguma coisa mais geral:

```
git help
```






