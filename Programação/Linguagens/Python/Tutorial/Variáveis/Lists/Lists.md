# Lists

* [[Programação/Linguagens/Python/Tutorial/Variáveis/Lists/Métodos|Métodos]]
&nbsp; Em Python, `list` é um dos 4 tipos de dados usados para armazenar coleções de dados, As outras 3 são [[Tuples|tuples]], [[Sets|sets]] e [[Dicts (dictionary)|dicts]], cada um com suas próprias vantagens e desvantagens.
```python
x = ["apple", "banana", "cherry"]
print(x)
```
&rdsh; Listas são criadas com cochetes `[]`.
## Itens da Lista
&nbsp; Os itens da lista são alteráveis, permitem valores duplicados, e são ordenados através do index, da mesma maneira que um vetor/array.

* #### Ordenado
&nbsp; Ao dizermos que as listas em Python são ordenadas, queremos dizer que os itens possuem uma ordem definida, à qual não poderemos alterar. Caso adicionemos novos itens à lista, ele será inserido no final da mesma.

* #### Alterável
&nbsp; Em Python, dizemos que a lista é alterável por podermos alterar, adicionar e remover itens da lista, mesmo após ela ter sido criada.

* #### Permite Valores Duplicados
&nbsp; Uma vez que listas são apenas indexes, elas podem possuir itens com o mesmo valor.

> [!NOTE] Anote
> &nbsp; Existem [[métodos para listas]] que são capazes alterar a sua ordem, mas em geral, a ordem dos itens não mudará.

## Comprimento da Lista
&nbsp; Para medirmos o comprimento de uma lista, podemos usar a função `len()`.

```python
x = ["apple", "banana", "cherry"]
print(len(x))
```
&nbsp; Note também que a função `len()` é a mesma usada para verificar o comprimento de uma string. Isso se dá pelo fato de que em Python as strings são apenas listas com bytes definidos como caractéres.

## Itens de uma Lista
&nbsp; Uma das grandes vantagens das listas em Python é o fato de podermos atribuir qualquer _data type_ à seus indexes.
```python
list = ["abc", 34, True, 40, "male"]
print(list)
```

## `list()` Constructor
&nbsp; Por se tratar de uma linguagem orientada à objetos, todas as _data types_ são feitas por objetos, portanto, todas elas possuem um constructor.

&nbsp; Para criarmos uma lista através de seu constructor, devemos seguir o seguinte formato.
```python
thislist = list(("apple", "banana", "cherry")) # note the double round-brackets
print(thislist)
```

## Acessando Itens
&nbsp; Para podermos acessar itens em Python devemos indicar o index onde o item se encontra.

```python
thislist = list(("apple", "banana", "cherry"))
print(thislist[0])   # Will print only "apple"
```

#### Index Negativo
&nbsp; Quando usamos indexes negativos, estamos a indicar o valor a partir do final, `-1` por exemplo indica o último index de todos.
```python
thislist = list(("apple", "banana", "cherry"))
print(thislist[-1])   # Will print only "cherry"
```

#### Faixa de Indexes
&nbsp; É possível indicarmos apenas uma faixa de itens que queremos pegar de uma lista, para tal, usamos o operador `:`, com o valor do começo à esquerda, e o valor final à direita.

&nbsp; Caso um dos dois valores não seja atribuído, python irá devidamente considerar o início e o final como `0` e `n` respectivamente. (onde n é o final da lista).
```python
thislist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
print(thislist[2:5])
```
&rdsh; No caso acima irá ser printado apenas os valores do index `2` ao index `4`. Sim, quando indicamos o final, ele não é incluído na faixa, caso no exemplo acima quisessemos também o index `5`, teríamos que escrever `thislist[2:6]`.

## Verificar se o Item Existe na Lista
&nbsp; Para podermos verificar se um certo item existe dentro de uma lista, podemos usar o operador [[04. Operadores#Operadores de Participação|in]].

```python
thislist = ["apple", "banana", "cherry"]

if "apple" in thislist:
  print("Yes, \"apple\" is in the fruits list")
```

## Alterar o Valor de um Item
&nbsp; podemos alterar o valor de um item através da atribuição de um novo valor. Para tal, primeiro acessamos o item através de seu index, e então, atribuímos o valor desejado.

```python
thislist = ["apple", "banana", "cherry"]
thislist[1] = "blackcurrant"

print(thislist)
```
&rdsh; No exemplo acima, o item de index 1 `"banana"` será substituído por `"blackcurrant"`

* #### Alterando uma Faixa de Itens
&nbsp; Podemos também alterar uma faixa inteira da lista em python, seja por 1 ou itens
```python
thislist = ["apple", "banana", "cherry", "orange", "kiwi", "mango"]
thislist[1:3] = ["blackcurrant", "watermelon"]

print(thislist)
```
&rdsh; Neste exemplo, `"banana"` e `"cherry"` serão substituídos por `"blackcurrant"` e `"watermelon"`.

* #### Alterando um Item por um Conjunto
```python
thislist = ["apple", "banana", "cherry"]
thislist[1:2] = ["blackcurrant", "watermelon"]

print(thislist)
```
&rdsh; Neste exemplo, `"banana"` será substituídos por `"blackcurrant"` e `"watermelon"`.

* #### Alterando um Conjunto por Apenas um Item

```python
thislist = ["apple", "banana", "cherry"]
thislist[1:3] = ["watermelon"]

print(thislist)
```
&rdsh; Neste exemplo, `"banana"` e `"cherry"` serão substituídos por `"watermelon"`.

## Inserindo Itens
&nbsp; Para inserir um novo item na lista sem ter que substituír um valor existente, podemos usar o método `insert()`, ele irá inserir o item no index que for especificado.
```python
thislist = ["apple", "banana", "cherry"]

thislist.insert(2, "watermelon")
print(thislist)
```

## Append Itens
&nbsp; Para adicionarmos itens ao final da lista, podemos usar o método `append()`.
```python
thislist = ["apple", "banana", "cherry"]

thislist.append("orange")
print(thislist)
```

## Extendendo a Lista
&nbsp; Para realizer _append_ de uma lista em outra, devemos usar o método `extend()`.
```python
thislist = ["apple", "banana", "cherry"]
tropical = ["mango", "pineapple", "papaya"]

thislist.extend(tropical)  
print(thislist)
```
&nbsp; O método `extend()` também é capaz de adicionar qualquer tipo de _collection_ (tuples, sets, dictionaries, etc.).
```python
thislist = ["apple", "banana", "cherry"]
thistuple = ("kiwi", "orange")

thislist.extend(thistuple)
print(thislist)
```
## Removendo Itens Específicos da Lista
&nbsp; Podemos remover itens específicos da lista através do método `remove()`.
```python
thislist = ["apple", "banana", "cherry"]

thislist.remove("banana")
print(thislist)
```
&nbsp; Caso a lista possua mais de um item com o valor específicado, `remove()` irá retirar apenas a primeira ocorrência.

## Removendo Itens Através do Index
&nbsp; O método `pop()` é o responsável por remover um index específico da lista.
```python
thislist = ["apple", "banana", "cherry"]

thislist.pop(1)
print(thislist)
```
&rdsh; Caso não seja específicado um index, `pop()` irá retirar o último item da lista.

&nbsp; Podemos também retirar um item da lista através _keyword_ `del`.
```python
thislist = ["apple", "banana", "cherry"]

del thislist[0]
print(thislist)
```

## Limpar a Lista
&nbsp; Caso queiramos retirar todos os itens da lista, mas ainda manter ela, podemos usar o método `clear()`.
```python
thislist = ["apple", "banana", "cherry"]

thislist.clear()
print(thislist)
```

## Loop em uma Lista
&nbsp; Em Python é possível realizar loops em listas com o uso da _keyword_ `for`
```python
thislist = ["apple", "banana", "cherry"]

for x in thislist:
  print(x)
```
&rdsh; No exemplo dado acima, irémos correr cada item da lista e imprimir seus valores no terminal.

&nbsp; Podemos também realizar um loop em uma lista através da seguinte sintaxe.
```python
thislist = ["apple", "banana", "cherry"]
[print(x) for x in thislist]
```
&rdsh; À essa técnica damos o nome de _"[[#List Comprehension|List Comprehension]]"_
* #### Loop Através do Index da Lista
&nbsp; Para fazermos loops através do index de uma lista, precisamos trabalhar com a função `len()` e o objeto `range`.
```python
thislist = ["apple", "banana", "cherry"]

for i in range(len(thislist)):
  print(thislist[i])
```
&rdsh; Para que o loop funcione no exemplo acima, precisamos definir um diferente array para realizar o loop, neste caso, criamos um `range` do tamanho da lista, note que o objeto `range` não possui valor, apenas index. Usamos então o iterador `i` para realizar o loop, fazendo com que `i` passe a ser um número, diferente do [[#Loop em uma Lista|caso acima]] em que tínhamos `x` como um item da lista.

* #### Usando o Loop While em uma Lista
&nbsp; Podemos também realizar loops em uma lista com a _keyword_ `while`.

&nbsp; Para tal, usamos a função `len()` para definir o tamanho da lista, e iniciamos com o iterador a 0.

```python
thislist = ["apple", "banana", "cherry"]
i = 0
while i < len(thislist):
  print(thislist[i])
  i = i + 1
```

## List Comprehension
&nbsp; _List Comprehension_ é uma técnica usada para criar uma nova lista baseada em outra existente.

&nbsp; Observo o primeiro caso (criação de uma lista de forma comum).
```python
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist = []

for x in fruits:
  if "a" in x:
    newlist.append(x)
print(newlist) 
```
&rdsh; No exemplo acima, todas as frutas que possuem a letra `a` irão ser adicionada à nova lista.

&nbsp; Agora observe o segundo caso (criação de uma lista com list comprehension)
```python
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
  
newlist = [x for x in fruits if "a" in x]
print(newlist)
```
&rdsh; Essa técnica é um dos exemplos do que pode ser implementado em Python através de sua sintaxe.

&nbsp; Ambos exemplos realizam a mesma tarefa, porém, a sintaxe do segundo caso é menor.

#### Syntax
```python
newlist = [_expression_ for _item_ in _iterable_ if _condition_ == True]
```

&rdsh; `iterable` : Pode ser qualquer objeto iterável. (lists, tuples, sets, range, etc.)
&rdsh; `expression` :  É o item atual na iteração.

## Ordenando Listas
&nbsp; Em Python podemos usar o método `sort()` para ordenar listas de forma alpanumérica, ascendente.
```python
thislist = ["orange", "mango", "kiwi", "pineapple", "banana"]

thislist.sort()
print(thislist)
```

#### Ordenando de Forma Decrescente
Podemos definir a lista de forma contrária à anterior, apenas adicionando o argumento `rever = True`.
```python
thislist = ["orange", "mango", "kiwi", "pineapple", "banana"]

thislist.sort(reverse = True)
print(thislist)
```

#### Customizando Funções de Ordenação
&nbsp; Podemos também criar nosso próprio método de ordenação, para enviarmos o mesmo para nossa `sort()` devemos usar um argumento no formato `key = myFunction`.
```python
def myfunc(n):
  return abs(n - 50) 
  
thislist = [100, 50, 65, 82, 23]
thislist.sort(key = myfunc)
print(thislist)
```
&rdsh; No caso acima, nossa função irá fazer com que os itens fiquem ordenados de acordo com a proximidade ao número 50.