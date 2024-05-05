# Strings

* [[Programação/Linguagens/Python/Tutorial/Variáveis/Strings/Métodos|Métodos]]

## String de Linhas Múltiplas
&nbsp; Em Python, é possível atribuir uma string de múltiplas linhas à uma variável, para tal, usa se três aspas duplas ou três aspas simples.
```python
text = """Hello World!
Today is a beautiful day."""

text2 = '''Hello World!
Today is a beautiful day.'''
```
## Strings São Arrays
&nbsp; Assim como em outras linguágens de programação, strings em pythons são arrays de bytes representando caracteres unicode.

&nbsp; Porém, Python não possui um tipo `char`, um caractér único é simplesmente uma string de tamanho 1.

&nbsp; Para acessar um elemento de uma string, usa-se o cochete.
```python
a = "Hello World!"

print(a[1])
```

## Loop em um String
&nbsp; Uma vez que strings são apenas arrays, é possível fazer um loop através dos caractéres em uma string com o loop `for`.
```python
for x in "banana":
	print(x)
```
## String Length
&nbsp; Para adquirirmos o tamanho de uma string, usamos a função `len()`
```python
a = "Hello!"

print(len(a))
```

## Check String
&nbsp; Para verificar que uma certa string está presente em uma outra string, podemos usar a _keyword_ `in`.
```python
txt = "The best things in life are free!"

print("free" in txt)
```
&nbsp; Uma vez que a _keyword_ `in` retorna um boolean, podemos usar ela em conjunto de um `if` para definir uma ação.
```python
txt = "The best things in life are free!"

if "free" in txt:
	print("Yes, \"free\" is present.")
```

## Check if NOT
&nbsp; Para verificar que uma certa string NÃO está presente em outra, podemos usar a keyword `not in`.
```python
txt = "The best things in life are free!"

if "expensive" not in txt:
	print("No, \"expensive\" is NOT present.")
```

## Slicing
&nbsp; Em Python, é possível retornar apenas uma faixa de caractéres através da sintaxe do _slicing_.

&nbsp; Para tal, basta especificar o index incial e o final, separado por um `:`. 

**ATENÇÃO**, o index final não será incluido.
```python
b = "Hello, World!"

print(b[2:5]) # Will print 'llo'
```

&nbsp; Para imprimir a partir do início, ou garantir que vá até o final, basta omitir o valor do index na devida posição.

```python
b = "Hello, World!"

print(b[:5]) # Will print 'Hello'
print(b[2:]) # Will print 'llo, World!'
```

## Concatenação de Strings
&nbsp; Em Python, é possível concatenar 2 ou mais strings através do operador `+`.

```python
a = "Hello"
b = "World"
c = a + b

print(c) # Will print "HelloWorld"
```

## F-Strings (String Format)
&nbsp; Como apresentado anteriormente, não é possível concatenar strings com núḿeros em python normalmente, porém, é possível fazer isto através do método `format()` ou _f-strings_.

&nbsp; A F-String foi introduzida em Python 3.6, e desde então tem sido a melhor forma de se formatar uma string.

&nbsp; Para específicar uma string como _f-string_ basta adicionar um `f` antes da string literal, e adicionar chaves (`{}`) como espaço reservado para variáveis ou outras operações.

```python
age = 36
txt = f"My name is John, I am {age}"

print(txt) # Will print "My name is John, I am 36"
```
&nbsp; Além disso, espaços reservados podem incluir _modificadores_ para formatar o valor.

&nbsp; Um modificador é incluído com a adição de `:` seguido de um tipo permitido de formatados, como `.2f` que define o limite de casas decimais a ser impresso por um número.

```python
price = 59  
txt = f"The price is {price:.2f} dollars"  
print(txt) # Will print "The price is 59.00 dollars"  
```

&nbsp; E para finalizar, é possível realizar operações matemáticas dentro de um espaço reservado em Python.

```python
txt = f"The price is {20 * 59} dollars"  
print(txt) # Will print "The price is 1180 dollars"
```