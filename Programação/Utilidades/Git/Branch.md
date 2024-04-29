# Branch
## Trabalhando com _Branches_
&nbsp; Em Git, um `branch` é uma versão nova/separada do repositório _main_, ele nos permite acompanhar alterações em partes específicas do código, sem afetar o repositório padrão.

#### Novo Git Branch
* `git branch`
&rdsh; Apresenta os _branchs_ existentes, marcando com `*` o branch em que o usuário se encontra no momento.

&nbsp;

* `git branch <branch_name>
&rdsh; Cria um novo _branch_ a partir do branch atual.

&nbsp;

* `git checkout <branch_name>`
&rdsh; Entra no _branch_ especificado. Ao fazermos novos _commits_, os mesmos serão inseridos na _branch_ em que estamos, portanto, caso não queiramos alterar a _main branch_, devemos verificar em qual nos encontramos antes de realizarmos um _commit_.

>[!NOTE] Saiba
> &nbsp; `git checkout` será substituido por `git switch` em breve.

&nbsp; Ao entrarmos realizarmos _commits_ em um _branch_, podemos notar que as alterações realizadas não se aplicarão à outras _branchs_, para tal, podemos usar `git checkout` para uma _branch_ diferente e verificar a mesma.

## Merging Branches
* `git merge <branch_name>`
&rdsh; Após fazer alterações em uma branch, caso queiramos passar essas alterações para a main ou para a branch pai, devemos realizar um merge, para tal é necessário que entremos na branch main/pai e usemos o comando `git merge`.

#### Conflitos em Merge
&nbsp; Quando possuimos algum conflito entre a main, e a branch que criamos (por exemplo, um commit que fizemos na main após termos criado a branch), o nosso merge poderá falhar. Para resolvermos este conflito devemos verificar nosso branch com `git status` e avaliar quais alterações deverão ou não ser feitas, e no final realizar um `git commit`, adicionando as alterações no repositório e _branch_