# Desafios Comentados

<h3> Problemas aritméticos </h3>

<h6>
    <ul>
    1/5 - Soma Simples<br>
    2/5 - Coxinha de Bueno <br>
    3/5 - Cálculo de viagem <br>
    4/5 - Imposto de Renda <br>
    5/5 - Teorema da Divisão <br>
    </ul>
</h6>


<h4> 1/5 - Soma Simples  </h4>

Este desafio pede para que dois números inteiros sejam lidos como as variáveis <b>A</b> e <b>B</b>. A partir disso, a soma entre essas variáveis deve ser lida e uma nova variável criada: <b>SOMA</b>. 

<b>Entrada</b>: 2 valores inteiros

<b>Saída</b>: <b>SOMA</b> (com letras maiúsculas, um espaço em branco antes e depois do símbolo de igualdade, seguido pelo valor correspondente à soma A e B.)

<u>Resolução:</u> 

O desafio pede 2 variáveis A e B. Então:

var A =

var B = 

Como é feito em JS, a entrada deve ter <b>gets</b> e a saída, <b>console.log</b>. 

var A = gets();
var B = gets();

console.log();

No entanto, precisamos analisar uma <b>String</b> e retornar um número inteiro na base especificada. Para isso, usamos a função <b>parseInt</b>(), do seguinte modo: parseInt(string, base);

var A = parseInt(gets());
var B = parseInt(gets());

Agora temos as variáveis A e B e precisamos criar a variável soma para somar essas variáveis.

let soma = (A + B);

Como resposta, SOMA com um espaço em branco e o valor da soma: 

console.log("SOMA = " + soma);    

Por fim, o código completo:
```
var A = parseInt(gets());
var B = parseInt(gets());
let soma = (A + B);
console.log("SOMA = " + soma);    

```

Nota: 

1. Se usar somente gets():

- **Dado de entrada:** 30 10
- **Saída esperada:** SOMA = 40
- **Sua Saída:** SOMA = 3010

2. Usando parseInt(gets()):

- **Dado de entrada:** 30 10
- **Saída esperada: **SOMA = 40
- **Sua Saída: **SOMA = 40



<h4> 2/5 - Coxinha de Bueno  </h4>

Este desafio diz que Mônica alcançou um novo record conseguindo comer 43 coxinhas em 10 min, enquanto seu antecessor conseguiu comer 38, no mesmo tempo.  O restaurante precisa de mais algumas informações.

**Desafio**:  Desenvolver um programa para calcular a quantidade média de coxinha que os participanetes conseguiram comer. 

**Entrada**: Linha única contendo dois inteiros **H** (número total de coxinhas consumidas) e **P** (número total de participantes na competição), sendo (1<= H, P <= 1000).



**Saída**: Linha única com um número racional representando o número médio de coxinhas consumidas. Resultado em número racional com 2 dígitos após o ponto decimal.

<u>Resolução</u>:

Neste caso temos 2 variáveis e um total: 

let H = número total de coxinhas 

let P = número total de participantes

let total = número médio de coxinhas = (H/P)

A entrada é uma linha única com 2 números. Se colocar somente gets(), os números vão ficar juntos. O método **split()**, que permite dividir/separar strings. 

let x = gets().split(" ");

No  valor das variáveis H e P usa-se a função **parseInt()** (explicação no desafio 1/5) e dentro dos () é indicada a entrada com o valor a ser analisado (x) e uma base. No caso, não estamos usando uma base, pois queremos somente uma string, então usa-se para H, x[0] e para P, x[1], ou seja, 2 números em linha. 

let H = parseInt(x[0])
let P = parseInt(x[1])

A saída pede uma linha única com número médio, então, números com casas decimais. Para tal, precisamos usar **.toFixed()** e indicar o número de casas decimais, no caso (2). 

let total = (H/P).toFixed(2); 

Mas o número total é flutuante, ou seja, não está associada a nenhum objeto. A função parseFloat() vai analisar um argumento string e retornar um número de ponto flutuante. 

let total = parseFloat(H/P).toFixed(2);

Por fim, o código completo:
```
let x = gets().split(" ");
let H = parseInt(x[0])
let P = parseInt(x[1])
let total = parseFloat(H/P).toFixed(2);
console.log(total);
```
Nota: 

1. Se usar somente gets():

- **Dado de entrada:** 10 90
- **Saída esperada:** 0.11
- **Sua Saída:** Infinity

2. Usando gets().split(" "):

- **Dado de entrada:** 10 90
- **Saída esperada: **0.11
- **Sua Saída: **0.11


Se não usar parseFloat, não passa em alguns desafios fechados.
