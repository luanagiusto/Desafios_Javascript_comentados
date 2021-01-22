<h1>Solução de Problemas Essenciais (JavaScript) </h1>

<h5>
<ul>
    1/5 - Quadrado e ao cubo <br>
    2/5 - A corrida de Tartarugas <br>
    3/5 - Ultrapassando V <br>
    4/5 - Validação de Nota <br>
    5/5 - Pedro Bento e o Mundo de OZ
</ul></h5>


____

<h3> 1/5 - Quadrado e ao cubo </h3>

Este desafio pede para escrever um programa que leia um valor inteiro **N** (1<N<1000). Sendo que N é a quantidade de linhas de saída.

**Entrada**: Número inteiro positivo **N**.

**Saída**: Conforme o exemplo: 

1 1 1
2 4 8
3 9 27
4 16 64
5 25 125

<u>Resolução:</u>

Temos uma entrada de um número N indicando o número de linhas. Cada linha tem 3 números. O primeiro é o valor de N, seguido pelo N² e depois N³. 

Na entrada temos: 

let input = parseInt(gets());

pois queremos analisar uma string e retornar um número inteiro. 

Como o N indica o número de linhas, precisamos de um loop até a quantidade de linhas indicada. A instrução **for** cria esse loop da seguinte forma: 

```
for ([inicialização]; [condição]; [expressão final])
   declaração
```

Neste caso, na inicialização declaramos a variável: var i=1, 1 indicando o início. A condição é uma expressão que vai ser avaliada antes da iteração do loop, se for true, ela continua. Assim, o valor i deve ser menor ou igual a valor de entrada (se 5, o valor de i vai ser menor ou igual a 5, mas começando em 1). A expressão final será validada para atualizar ou incrementar a variável do contador: i++. Então temos um for: 

for(var i = 1; i <= input; i++)

A saída é uma variável, então é preciso declará-la, mas de forma vazia, pois a expressão será colocada no console.log.

 let output = " ";

O desafio pede o quadrado de i e o cubo de i, para isso, informamos no console.log as multiplicações, de forma:

console.log(i , i  * i, i * i * i);

Por fim, o código completo:

```

```

let input = parseInt(gets());
for(var i = 1; i <= input; i++)
{
let output = " ";
console.log(i , i  * i, i * i * i);
}

```

```

____

<h3> 2/5 - A corrida das Tartarugas </h3>