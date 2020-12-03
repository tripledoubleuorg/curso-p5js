# P5.js
O p5.js é uma biblioteca JavaScript open-source para código criativo.
– [https://p5js.org/]

## Conteudos
- [Do processing ao p5.js](do-processing-ao-p5.js)
- [Ambiente do p5.js](ambiente-do-p5-js)
- Principais funções do p5.js
- Operadores
- Funções
- Condicionais
- Loops
- Sensores

##  Do processing ao P5.js

### Processing
> “O Processing é um software flexível para desenhar e uma linguagem para aprender a código no contexto das artes visuais.” — [processing.org](https://processing.org/)

O Processing é um projecto iniciado em 2001 por [Casey Reas](http://reas.com/) e [Ben Fry](https://benfry.com/), com o objectivo de ser uma ferramenta para não programadores iniciarem na programação, uma vez que tem um resultado visual rápido e fácil.

A sua sintaxe é baseda em JAVA e tem o seu próprio IDE – Integrated Development Environment ([processing.org/download](https://processing.org/download/)).

O Processing é uma das linguagens mais utilizada para a Programação Criativa e Arte Generativa.

### P5.js
O P5.js, criado por [Lauren McCarthy](https://lauren-mccarthy.com/) e desenvolvido por uma comunidade de colaboradores, consiste numa interpretação do Processing para a web. Ou seja, é uma tradução do Processing para Javascript de modo que o seu código possa ser lido pelos browsers.

Javascript é uma das principais linguagem de programação web, que permite manipular comportamentos e também tornar as páginas interactivas.
[Curso Javascript](https://github.com/tripledoubleuorg/curso-javascript)

A documentação do P5.js pode ser encontrada no site [p5js.org](https://p5js.org/).

Tanto o Processing como o P5.js são gratuitos e open-source.


## Ambiente do p5.js
O P5.js tem o seu próprio editor [editor.p5js.org](https://editor.p5js.org/) ou podemos fazer o download e montar localmente [p5js.org/download](https://p5js.org/download/).

O P5.js funciona através de funções, que são conjuntos de instruções para que se execute uma tarefa. Uma função tem que ser definida e chamada e a sua estrutura é constituída por instruções e argumentos.

No site do P5.js podemos encontrar uma série de funções pré-definidas: [p5js.org/reference](https://p5js.org/reference/)

Entre elas temos duas funções estruturais:
- [setup()](https://p5js.org/reference/#/p5/setup) → acontece apenas uma vez
- [draw()](https://p5js.org/reference/#/p5/draw) → está sempre em loop de cima para baixo

### Exercício
````Javascript
  function setup() {
    createCanvas(400, 400);
  }
  
  function draw() {
    background(220);
  }
````
````Javascript
function setup() {
  createCanvas(400, 400);
  ellipse(mouseX, mouseY, 25, 25);
}

function draw() {
  background(220);
}
````
````Javascript
function setup() {
  createCanvas(400, 400);
  background(220);
  ellipse(mouseX, mouseY, 25, 25);
}

function draw() {

} 
````
````Javascript
function setup() {
  createCanvas(400, 400);
  background(220);
}

function draw() {
  ellipse(mouseX, mouseY, 25, 25);
}
````
````Javascript
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
  ellipse(mouseX, mouseY, 25, 25);
}
````

## Formas
Dentro das funções encontramos também formas primitivas como:
- arc()
- ellipse()
- circle()
- line()
- point()
- quad()
- rect()
- square()
- triangle()

## Cores
Por defeito o P5.js utiliza o sistema de cor RGB e também tem funções pré-definidas:
- olorMode()
- fill()
- noFill()
- stroke()
- noStroke()

## Texto
Para escrever texto utiliza-se a função `text()`

````Javascript
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
  text('hello world', 10, 30);
}
````

````Javascript
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
  fill('red');
  text('Lorem ipsum dolor sit amet, consectetur adipiscing elit,', 10, 10, 70, 80); //faz uma caixa para o texto
}
````

### Atributos:

- textAlign()
- textLeading()
- textSize()
- textStyle()
- textWidth()
- textAscent()
- textDescent()

## Variáveis
"Variável" é um recurso em programação para armazenar um valor na memória do computador durante a execução de um algoritmo.

No P5.js uma variável para ser utilizada tem de ser declarada e atribuido um valor inicial.

````Javascript
var largura; //declarar
function setup(){
  createCanvas(400,400);
  largura = 100; //atribuir valor inicial
}

function draw(){
  background(220);
  rect(largura, 200, 25, 25); //utilizar
}

````
Enquanto biblioteca, o P5.js tem algumas variáveis pré-definidas (built-in) como `mouseX`, `mouseY`, `width` ou `height`

````Javascript
function setup(){
  createCanvas(400,400);
}

function draw(){
  background(220);
  rectMode(CENTER);
  rect(mouseX, mouseY, 25, 25);
}
````

## Operadores
- adição +
- subtração -
- multiplicação *
- divisão /
- exponencial **
- incrementação ++
- decrementação --

````Javascript
var posicaoX = 0;

function setup(){
  createCanvas(400,400);
}

function draw(){
  background(255, 255, 0);
  ellipse(posicaoX, height/2, 30, 30);
  posicaoX = posicaoX + 1;
}
````

````Javascript
var posicaoX = 0;

function setup(){
  createCanvas(400,400);
}

function draw(){
  background(255, 255, 0);
  ellipse(posicaoX, height/2, 30, 30);
  posicaoX ++;
}
````

## Condicionais
As estruturas condicionais em programação servem para verficar se uma condição é verdadeira ou falsa (expressão boleana).

### Exemplo
- 10 < 5 → falso
- 20 > 1 → verdadeiro

## Operadores relacionais
- maior >
- menor <
- maior ou igual >=
- menor ou igual <=
- igual ==
- não igual !=

````
if(expressão booleana for verdadeira) {
	Alguma coisa acontece.
}
````

````Javascript
var posicaoX = 0;
var velocidade = 1;

function setup(){
  createCanvas(400,400);
}

function draw(){
  background(255, 255, 0);
  ellipse(posicaoX, width/2, 30, 30);
  if(posicaoX > width) {
    velocidade = -1;
  } else if(posicaoX < 0) {
    velocidade = 1;
  }
  posicaoX = posicaoX + velocidade;
}
````

## Loop
Um loop ou repetidor é uma estrutura controlada para correr código repetidamente, com valores diferentes a cada vez.

````Javascript
function setup() {
  createCanvas(400, 400);
  background(220);
}

function draw() {
  for(var i = 0; i <= width; i+=50){
    ellipse(i, height/2, 25, 25);
  }
}
````

````Javascript
function setup() {
  createCanvas(400, 400);
  background(220);
}

function draw() {
  noStroke();
  for (var x = 0; x <= width; x += 50) {
    for (var y = 0; y <= height; y += 50) {
      fill(random(255), random(255), random(255));
      ellipse(x, y, 25, 25);
    }
  }
}
````

````Javascript
function setup() {
  createCanvas(400, 400);
  background(220);
}

function draw() {
  noStroke();
  background(255,255, 0);
  for (var x = 0; x <= mouseX; x += 50) {
    for (var y = 0; y <= mouseY; y += 50) {
      fill(random(255), random(255), random(255));
      ellipse(x, y, 25, 25);
    }
  }
}
````

