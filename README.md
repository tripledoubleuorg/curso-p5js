# P5.js
O p5.js é uma biblioteca JavaScript open-source para código criativo.
– [https://p5js.org/]

## Conteudos
- [Do processing ao p5.js](do-processing-ao-p5.js)
- [Ambiente do p5.js](ambiente-do-p5-js)
- [Formas](forma)
- [Cores](cores)
- [Texto](texto)
- [Variáves](variaveis)
- [Operadores](operadores)
- [Condicionais](condicionais)
- [Loops](loops)
- [Funções](funcoes)
- [Classes e Objectos](classes-e-objectos)
- [Imagens](imagens)


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
- colorMode()
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
}

function draw() {
  background(255,255, 0);
  for(var i = 0; i <= width; i+=50){
    ellipse(i, height/2, 25, 25);
  }
}
````

````Javascript
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(255,255, 0);
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
}

function draw() {
  background(255,255, 0);
  noStroke();
  for (var x = 0; x <= mouseX; x += 50) {
    for (var y = 0; y <= mouseY; y += 50) {
      fill(random(255), random(255), random(255));
      ellipse(x, y, 25, 25);
    }
  }
}
````

## Funções
As funções funcionam como acções no Javascript. Elas permitem executar determinado código e podem ter argumentos e retornar determidado valor. As funções são declaradas pelo termo function e têm de ser chamadas ou executadas.

````Javascript
function nomeFuncao(props){
    // corpo da funcao
}

nomeFuncao(); // chamar funcao
````
````Javascript
let canvas, r, g, b;

function setup() {
  canvas = createCanvas(400, 400);
  canvas.mouseClicked(randomColor);
  r = 0;
  g = 0;
  b = 0;
}

function draw() {

background(r,g,b);
}

function randomColor() {
  r = random(0, 255);
  g = random(0, 255);
  b = random(0, 255);
}
````

## Classes e objectos
As classes em p5.js são módulos de código reutilizáveis que encapsulam informação e funcionalidades.
Os objectos são contruídos a partir das classes e podem ser adicionados ou removidos enquanto o programa está a correr.

````Javascript
let circulo;
let circulo1;
function setup() {
  createCanvas(400, 400);
  circulo = new Circulo(200, 200, 20);
  circulo1 = new Circulo(100, 300, 50);
}

function draw() {
  background(220);
  circulo.mostrar();
  circulo.mover();
  circulo1.mostrar();
  circulo1.mover();
}

class Circulo{
  constructor(x, y, r){
    this.x = x;
    this.y = y;
    this.r = r;
  }
  
  mostrar(){
    ellipse(this.x, this.y, this.r);
  }
  
  mover(){
    this.x = this.x + random(-2, 2);
    this.y = this.y + random(-2, 2);
  }
}
````

### Array de objectos
````Javascript
let circulos = [];
function setup() {
  createCanvas(400, 400);
  for (var i = 0; i < 5; i++){
    circulos[i] = new Circulo(random(0, height), random(0, height), random(20, 40));
  }
  print(circulos.length)
}

function draw() {
  background(220);
  for (var i = 0; i < circulos.length; i++){
     circulos[i].mostrar();
     circulos[i].mover();
  }
}

class Circulo{
  constructor(x, y, r){
    this.x = x;
    this.y = y;
    this.r = r;
  }
  
  mostrar(){
    ellipse(this.x, this.y, this.r);
  }
  
  mover(){
    this.x = this.x + random(-2, 2);
    this.y = this.y + random(-2, 2);
  }
}
````
### Objectos interactivos
````Javascript
let circulos = [];
let circulo
function setup() {
  createCanvas(400, 400);
  print(circulos.length)
}

function mousePressed(){
  circulo = new Circulo(mouseX, mouseY, random(20, 40));
  circulos.push( circulo);
}


function draw() {
  background(220);
  for (var i = 0; i < circulos.length; i++){
     circulos[i].mostrar();
     circulos[i].mover();
  }
}

class Circulo{
  constructor(x, y, r){
    this.x = x;
    this.y = y;
    this.r = r;
  }
  
  mostrar(){
    ellipse(this.x, this.y, this.r);
  }
  
  mover(){
    this.x = this.x + random(-2, 2);
    this.y = this.y + random(-2, 2);
  }
}
````
````Javascript
let circulos = [];
let circulo;
let mic;
let mapVol;
let vol;

function setup() {
  createCanvas(400, 400);
    // iniciar microfone
  mic = new p5.AudioIn();
  mic.start();
}

function volCirculo() {
  circulo = new Circulo(random(0, width), random(0, height), random(20, 40));
  circulos.push(circulo); 
}


function draw() {
  background(220);
  
  vol = mic.getLevel();
  mapVol = map(vol, 0, 1, 0, 5000);
  print(mapVol )
  

  if(  mapVol > 500){
    volCirculo()
  } 
  
  
  for (var i = 0; i < circulos.length; i++) {
    circulos[i].mostrar();
    circulos[i].mover();
  }
}

class Circulo {
  constructor(x, y, r) {
    this.x = x;
    this.y = y;
    this.r = r;
  }

  mostrar() {
    ellipse(this.x, this.y, this.r);
  }

  mover() {
    this.x = this.x + random(-2, 2);
    this.y = this.y + random(-2, 2);
  }
}
````
## Imagens

````Javascript
let img;
function preload() {
  img = loadImage('img/imagem.jpg');
}

function setup() {
  createCanvas(400, 400);
    background(220);
}

function draw() {
  image(img, 0, 0, width, img.height*width/img.width)
  
  var scale = .6;
  image(img, 0, 0, scale * width, scale * img.height*width/img.width)
}
````

## Sensores

### Microfone
````Javascript
let mic; 
let mapVol;

function setup() {
  // tela
  createCanvas(400, 400); 
  
   // iniciar microfone
    mic = new p5.AudioIn();
    mic.start();

}

function draw() {
  var vol = mic.getLevel();
  mapVol = map(vol, 0, 1, 0, 255*10);
  // fundo
  background(mapVol, 0, 255);
}
````

### Câmera

#### Mostrar como imagem
````Javascript
let video;

function setup() { 
  createCanvas(320, 240);
  video = createCapture(VIDEO);
  video.size(width, height);
  video.hide();
}

function draw() {
  background(0)
  image(video, 0, 0, width, height)
}
````

#### Manipulação de Pixels
````Javascript
var video;

function setup() { 
  createCanvas(320, 240);
  pixelDensity(1);
  video = createCapture(VIDEO);
  video.size(width, height);
}

function draw() {
  loadPixels();
  video.loadPixels();
  for (var y = 0; y <= height; y++) {
    for (var x = 0; x <= width; x++) {
      var index = (x + y * video.width) * 4;
      var r = video.pixels[index];
      var g = video.pixels[index + 1];
      var b = video.pixels[index + 2];
      
      pixels[index] = r;
      pixels[index + 1] = g;
      pixels[index + 2] = b;
      pixels[index + 3] = 255;
    }
  }
  updatePixels();
}
````

Exemplo adaptado de [The Coding Train](https://www.youtube.com/watch?v=rNqaw8LT2ZU&list=PLRqwX-V7Uu6aKKsDHZdDvN6oCJ2hRY_Ig&index=4)
````Javascript
var video;
var videoScale = 10;

function setup() { 
  createCanvas(320, 240);
  pixelDensity(1);
  video = createCapture(VIDEO);
  video.size(width / videoScale, height / videoScale);
}

function draw() {
  background(0);
  video.loadPixels();
  for (var y = 0; y <= video.height; y++) {
    for (var x = 0; x <= video.width; x++) {
      var index = (x + y * video.width) * 4;
      var r = video.pixels[index];
      var g = video.pixels[index + 1];
      var b = video.pixels[index + 2];
      var bright = (r+g+b) / 3;
      var rectSize = map(bright, 0, 255, 0, videoScale);
      fill(255);
      rectMode(CENTER);
      rect(x * videoScale, y * videoScale, rectSize);
    }
  }
}
````
