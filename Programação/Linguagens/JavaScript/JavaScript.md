# JavaScript


## Por quê Aprender JavaScript?
&nbsp; JavaScript é uma das 3 linguagens principais que desenvolvedores web precisam aprender.

* #### JavaScript Pode Alterar o Conteúdo de Ficheiros HTML
&nbsp; Um dos muitos métodos HTML em JS é o `getElementByID()`.

O exemplo abaixo "encontra" um elemento HTML (com id="demo"), e altera o conteúdo (innerHTML) para "Hello JavaScript".
```js
document.getElementById("demo").innerHTML = "Hello JavaScript";
//                                                 ||
document.getElementById("demo").innerHTML = 'Hello JavaScript';
```

> [!NOTE] Atenção
> &nbsp; JavaScript aceita tanto aspas simples quanto duplas para strings.

* #### JavaScript Pode Alterar o Valor de Atributos HTML
```js
document.getElementById('myImage').src='pic_bulbon.gif'
//                                           &&
document.getElementById('myImage').src='pic_bulboff.gif'
```
* #### JavaScript Pode Alterar o Estilo HTML (CSS)
```js
document.getElementById("demo").style.fontSize = "35px";
```
* #### JavaScript Pode Esconder Elementos HTML
```js
document.getElementById("demo").style.display = "none";
```
* #### JavaScript Pode Mostrar Elementos HTML
```js
document.getElementById("demo").style.display = "block";
```