# Problemas aritméticos (JavaScript)

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
____

<h4> 2/5 - Coxinha de Bueno  </h4>

Este desafio diz que Mônica alcançou um novo recorde conseguindo comer 43 coxinhas em 10 min, enquanto seu antecessor conseguiu comer 38, no mesmo tempo.  O restaurante precisa de mais algumas informações.

**Desafio**:  Desenvolver um programa para calcular a quantidade média de coxinha que os participantes conseguiram comer. 

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

Mas o número total é flutuante, ou seja, não está associada a nenhum objeto. A função **parseFloat()** vai analisar um argumento string e retornar um número **ponto flutuante**. 

let total = parseFloat(H/P).toFixed(2);

Por fim, o código completo:
```
let line = gets().split(" ");
let H = parseInt(line[0])
let P = parseInt(line[1])
let total = parseFloat(H/P).toFixed(2);
console.log(total);
```
____

<h4> 3/5 - Cálculo de viagem  </h4>

Neste desafio, Rubens quer calcular e mostrar a quantidade de litros combustível gasto em uma viagem, sendo que seu carro faz 12km/L. 

**Desafio**: efetuar o cálculo, fornecer o tempo gasto em horas e a velocidade média em km/h. 

**Entrada**: Dois números inteiros: **t** (tempo gasto na viagem em horas) e **v** (velocidade média durante a msm em km/h).

**Saída** : Imprimir a quantidade de litros com três dígitos após o ponto decimal.



<u>Resolução</u>:

Como no desafio anterior (2/5), temos 2 variáveis (t e v) apresentadas em uma única linha (let line). Precisamos usar o método .split() para separar/dividir as strings e a função parseInt() para analisar a string e retornar um inteiro.

let line = gets().split(" ");
let t = parseInt(line[0]);
let v = parseInt(line[1]);

Para o cálculo da velocidade média (let media) precisamos da distância e do tempo da viagem (t), uma vez que, velocidade média= distância/tempo. Então: Distância = v * t.

let media = (v *t)/12

A saída pede o resultado com três casas decimais, então usamos .toFixed(3), onde 3 indica 3 casas decimais. 

let media = (v *t)/12.toFixed(3)

O resultado final é o console.log(media).

Por fim, o código completo:

```

let line = gets().split(" ");
let t = parseInt(line[0]);
let v = parseInt(line[1]);
let media = (t*v/12).toFixed(3);
console.log(media);

```

____

<h4> 4/5 - Imposto de renda  </h4>

Neste desafio, temos que ler um número com duas casas decimais (então devemos usar **.toFixed(2)**  no console.log) e calcular mostrando o valor que a pessoa deve pagar de imposto de renda, segundo a tabela:

![img](https://resources.urionlinejudge.com.br/gallery/images/problems/UOJ_1051_pt.png)

Lembrando que: se o salario for de R$3002,00 a taxa fica só sobre R$1000,00, pois salários até R$2000,00 são isentos de imposto. Então, nesse exemplo temos 8% sobre R$1000,00 + 18% sobre R$2,0 = R$80,36.

**Entrada** : Um valor de ponto flutuante (parseFloat()) com duas casas decimais (to.Fixed(2)).

**Saída** : imprimir o texto "R$" seguindo de um espaço e do valor total devido de imposto de renda com duas casas decimais após o ponto. Se o valor de entrada for <= 2000, imprimir: "Isento".

<u>Resolução</u>:

Temos 2 variáveis (salario e imposto) apresentadas em uma única linha (let line). Precisamos usar o método **.split()** para separar/dividir as strings e a função **parseFloat()** para analisar a string e retornar um ponto flutuante, mas só no caso do salário.

let line = gets().split(" ");
let salario = parseFloat(line[0]);
let imposto;

A variável imposto de renda varia de acordo com a variação do salário, então precisamos usar as condicionais **if** e **else**. Dessa forma, a condicional if verifica se a afirmação, dentro do bloco, é  verdadeira, se for falsa, verifica as afirmações dentro do else. 

A primeira condicional é em relação a isenção de imposto:

if (salario <= 2000,00) {

imposto = 0,00;

}

if (imposto == 0,00) {

console.log("Isento");

}

Se o valor for menor ou igual a 2000,00, irá ser impresso "Isento".

A segunda condicional é para salários entre 2000 e 3000,00. Como o imposto só é válido acima de 2000, precisamos subtrair o salário do valor de 2000 e multiplicar pelo valor do imposto, no caso, 0,08 (equivalente a 8%).

else if (salario <= 3000.00) {
   imposto = (salario - 2000.00) * 0.08;

A terceira condicional é para salários entre 3000 e 4500. Neste caso, de 3000, somente 1000 será cobrado imposto referente a 8%. Entre 3000 e 4500 será cobrado 18%, então, do valor do salário será subtraído 3000, pois este corresponde aos 8% que será somado posteriormente. Assim temos,  

else if (salario <= 4500.00) {
   imposto = (salario - 3000.00) * 0.18 + 1000.00 * 0.08;



A quarta e última condicional é para salário acima de 4500. Do mesmo modo que a terceira condicional, de até 3000, somente 1000 será aplicado imposto de 8%, até 4500, somente 1500 será aplicado do imposto de 18% e acima de 4500, imposto de 28%. Assim temos, 

else {
   imposto = (salario - 4500.00) * 0.28 + 1500.00 * 0.18 + 1000.00 * 0.08;

A saída esperada é um texto em R$ com duas casas decimais (.toFixed(2)) e caso o valor seja menor ou igual a 2000, a mensagem "Isento" deve ser impressa. Então:

if (imposto == 0.0) {
    console.log("Isento");
}
else {
    console.log("R$ ", imposto .toFixed(2));
}

O código final ficará:

```

let line = gets().split(' ');
let salario = parseFloat(line[0]);
let imposto;
if (salario <= 2000.00) {
   imposto = 0.00;

} else if (salario <= 3000.00) {
   imposto = (salario - 2000.00) * 0.08;

} else if (salario <= 4500.00) {
   imposto = (salario - 3000.00) * 0.18 + 1000.00 * 0.08;

} else {
   imposto = (salario - 4500.00) * 0.28 + 1500.00 * 0.18 + 1000.00 * 0.08;

}
if (imposto == 0.0) {
    console.log("Isento");
}
else {
    console.log("R$ ", imposto .toFixed(2));
}

```

____

<h4> 5/5 - Teorema da divisão  </h4>

Este desafio pede para desenvolver um programa para calcular o quociente e o resto  da divisão de dois números inteiros. Sendo que **a** (inteiro) divisão por **b** (não-nulo) são os números inteiros **q** e **r**, tais que:

0 ≤ **r** < |**b**|

Se r < 0: **r = r -** |**b**|

**a** = **b** × **q** + **r**

**q = ( a - r ) / b**

**Entrada**: Dois números inteiros **a** e **b** em linha (-1.000 ≤ **a**, **b** < 1.000).  

**Saída** : imprimir o quociente **q** seguido pelo resto **r** da divisão de a por b. 

<u>Resolução</u>:

Temos 4 variáveis e uma entrada (as explicações estão nos desafios anteriores):

let line = gets().split(" ");
let a = parseInt(line[0]);
let b = parseInt(line[1]);
let q;
let r;

O desafio pede para imprimir o resto. Para isso temos operadores específicos. A atribuição para uma divisão é **x /= y** , enquanto a atribuição de resto é **x %= y**. Então:

r = a%b;

E o quociente é 

q = ( a - r ) / b;

Mas aqui temos as condicionais para o caso de r ser <0: 

if (r<0) {

​	r = - r - Math.abs(b);
​	r = Math.abs(r);

}

**Math.abs()** nos retorna um valor absoluto de um número "x". 

A saída pede o quociente seguido pelo resto, as " " indicam um espaço entre eles. 

console.log(q + " " + r);

Por fim, o código completo:

```
let line = gets().split(" ");
let a = parseInt(line[0]);
let b = parseInt(line[1]);
let q;
let r;
r = a%b;
if (r<0){
  r = - r - Math.abs(b);
  r = Math.abs(r);
}
q = (a-r)/b;
console.log(q + " " + r);
```




