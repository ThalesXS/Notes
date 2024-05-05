# Métodos

Continuar anotando de [w3schools](https://www.w3schools.com/python/python_ref_string.asp)

* Capitalize : [[#Capitalize|capitalize()]]
* Casefold : [[#Casefold|casefold()]]
* Center : [[#Center|center()]]
* Count : [[#Count|count()]]
* Encode : [[#Enconde|enconde()]]
* Ends With :  [[#Ends With|endswith()]]
* Expand Tabs : [[]]
* Find : [[]]
* Format : [[]]
* Format Map : [[]]
* Index : [[]]
* Is Alpha-numeric : [[]]
* Is Aphabet : [[]]
* Is ASCII : [[]]
* Is Decimal : [[]]
* Is Digit : [[]]
* Is Identifier : [[]]
* Is Lower : [[]]
* Is Numeric : [[]]
* Is Printable : [[]]
* Is Space : [[]]
* Is Title : [[]]
* Is Upper : [[]]
* Join : [[]]
* Left Justify : [[]]
* Lower : [[#Lower|lower()]]
* Left Strip : [[]]
* Make Translation : [[]]
* Partition : [[]]
* Replace : [[#Replace|replace()]]
* Reverse Find : [[]]
* Reverse Index : [[]]
* Right Justify : [[]]
* Reverse Partition : [[]]
* Reverse Split : [[]]
* Right Strip : [[]]
* Split : [[#Split|split()]]
* Split Lines : [[]]
* Starts With : [[]]
* Strip : [[#Strip|strip()]]
* Swap Case : [[]]
* Title : [[]]
* Translate : [[]]
* Upper : [[#Upper|upper()]]
* Z Fill : [[]]
## Capitalize
```python
string.capitalize()
```
&rdsh; Este método não recebe parâmetros.

&nbsp; O método `capitalize()` retorna a string com o primeiro caractér maiúsculo e o restante minúsculo.
```python
txt = "hello, and welcome to my world."  
  
x = txt.capitalize()  
  
print(x) # Will print "Hello, and welcome to my world."
```
## Casefold
```python
string.casefold()
```
&rdsh; Este método não recebe parâmetros.

&nbsp; O método `casefold()` retorna a string com todos os caractéres minúsculos.

```python
txt = "Hello, and Welcome to my World."  
  
x = txt.casefold()  
  
print(x) # Will print "hello, and welcome to my world."
```
## Center

```python
string.center(lenght, character)
```
&rdsh; **lenght** - O comprimento mínimo da string. (Mandatório)
&rdsh; **character** - O caracter que será usado para preencher, caso não haja valor será usado `' '` (space). (Opcional)

&nbsp; O método `center()` retorna a string com pelo menos `lenght` caractéres, com a string que invocou o método no centro.
```python
txt = "hello"  
  
x = txt.center(15)  
  
print(x) # Will print "     hello     "
```
## Count
```python
string.count(value, start, end)
```
&rdsh; **value** : A string com o valor a ser procurado. (Mandatório)
&rdsh; **start** :  Um inteiro indicando a posição inicial (Opcional)
&rdsh; **end** :  Um inteiro indicando a posição final (Opcional)

&nbsp; O método `count()` retorna o número de vezes que um valor específico aparece na string.
```python
txt = "I love apples, apples are my favorite fruit"  
  
x = txt.count("apple", 10, 24)  
  
print(x) # Will print 1
```
## Encode
## Ends With
## Expand Tabs
## Find
## Format
## Format Map
## Index
## Is Alpha-Numeric
## Is Alphabet
## Is ASCII
## Is Decimal
## Is Digit
## Is Identifier
## Is Lower
## Is Numeric
## Is Printable
## Is Space
## Is Title
## Is Upper
## Join
## Left Justify
## Lower
```python
string.lower()
```
&rdsh; Este método não recebe parâmetros.

&nbsp; O método `lower()` retorna a string com todos os caractéres minúsculos.

```python
txt = "Hello, and WELCOME."  
  
x = txt.lower()  
  
print(x) # Will print "hello, and welcome."
```
## Left Strip
## Make Translation
## Partition
## Replace
```python
string.replace(oldvalue, newvalue, count)
```
&rdsh; **oldvalue** : A string a ser substituída. (Mandatório)
&rdsh; **newvalue** :   A string que irá substituir. (Mandatório)
&rdsh; **count** :  Um número específico de vezes que deverá substituir. (Opcional)

&nbsp; O método `count()` retorna o número de vezes que um valor específico aparece na string.
```python
txt = "I love apples, apples are my favorite fruit"  
  
x = txt.replace("apples", "bananas")  
  
print(x) # Will print "I love bananas, bananas are my favorite fruit"  
```
## Reverse Find
## Reverse Index
## Right Justify
## Reverse Partition?
## Reverse Split?
## Right Strip
## Split
```python
string.split(separator, maxsplit)
```
&rdsh; **separator** - A string que deverá ser usada para definir o que será separado. Usa `' '` caso nada seja definido. (Opcional)
&rdsh; **maxsplit** - Especifica um quantas vezes poderá ser feito o split. (Opcional)

&nbsp; O método `split()` retorna uma lista com pedaços da string dividida.

```python
txt = "hello, my name is Peter, I am 26 years old"  
  
x = txt.split(", ")  
  
print(x) # Will print a list ['hello', 'my name is Peter', 'I am 26 years old']
```

```python
txt = "apple#banana#cherry#orange"  
  
# setting the maxsplit parameter to 1, will return a list with 2 elements!  
x = txt.split("#", 1)  
  
print(x) # Will print a list ['apple', 'banana#cherry#orange']
```
## Split Lines
## Starts With
## Strip
```python
string.strip(characters)
```
&rdsh; **characters** - Um conjunto de caracteres a ser removido das pontas. (Opcional)

&nbsp; O método `strip()` retorna a string com os caracteres indicados removidos das pontas, caso não seja usado argumentos, removerá _whitespaces_.

```python
txt = "   Hello, and Welcome.   "  
  
x = txt.strip()  
  
print(x) # Will print "Hello, and Welcome."
```
## Swap Case
## Title
## Translate
## Upper
```python
string.upper()
```
&rdsh; Este método não recebe parâmetros.

&nbsp; O método `upper()` retorna a string com todos os caractéres maiúsculos.

```python
txt = "Hello, and Welcome."  
  
x = txt.upper()  
  
print(x) # Will Print "HELLO, AND WELCOME."
```
## Z Fill