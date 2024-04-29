# Git
&nbsp; O Git é um sistema de controle de versão, através dele podemos verificar as alterações realizadas no código.

## Comandos
* `git `
## Configurando o Git.

* `git config --global user.name <"name_here">`

&nbsp;

* `git config --global user.email <"email_here">`

## Trabalhando com Git
* `git init`
&rdsh; Para transformarmos um diretório em um repositótio git é necessário entrarmos no mesmo e executar o comando `git init`.

&nbsp;

* `git status`
&rdsh; Podemos verificar se estamos em um repositório git, e o estado do mesmo em qualquer momento, sendo necessário apenas realizar o comando `git status`.

&nbsp;

* `git add <files>`
&rdsh; Na primeira vez que criamos um repositório e adicionamos ficheiros ao mesmo, e a cada alteração feita nos mesmos, é necessário realizarmos o comando `git add` para adicionar as alterações feitas ao "_stage_".

&nbsp;

* `git commit`
&rdsh Após adicionarmos alterações ao "_stage_", para transmitir tais alterações ao repositório, é necessário fazer um _"commit"_, desta forma, teremos um um "_save point_" das alterações em nosso projeto. Sempre que fazemos um _commit_, devemos incluir uma mensagem, para tal, usamos a flag `-m` seguida de uma mensagem entre aspas duplas.

&nbsp;

* `git log`
&rdsh; Caso queiramos verificar o histórico de _commits_ feitos, podemos usar o comando `git log`, será então apresentado todos os _commits_ realizados.

&nbsp;

* `git help --all`
&rdsh; Caso tenha alguma dúvida sobre algum comando, `git help --all` apresenta todos os comandos com breves explicações, para mais detalhes, use `git <command> -help`.

