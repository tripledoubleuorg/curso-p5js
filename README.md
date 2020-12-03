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

## Video

### Iniciar
Para dar início a uma captura é necessário na função de `setup()` utilizar a função `createCapture(VIDEO)`. Esta função vai ligar a webcam do computador e criar um elemento na DOM separado da `canvas`.

````Javascript
function setup() {
  createCanvas(320, 240);
  background(50);
  createCapture(VIDEO);
}

function draw() {
  
}
````

### Video dentro da Canvas
````Javascript
var video;
function setup() {
  createCanvas(320, 240);
  video = createCapture(VIDEO);
  video.size(320, 240);
}

function draw() {
  image(video, 0, 0, width, height);
}
````



### Manipular video
````Javascript
var video;
function setup() {
  createCanvas(320, 240);
  video = createCapture(VIDEO);
  video.size(320, 240);
}

function draw() {
  tint(mouseY, 0, 0);
  image(video, 0, 0, mouseX, height);
}
````


### Pixel Arrays
````Javascript
function setup() {
  createCanvas(400, 400);
  pixelDensity(1);
}

function draw() {
  background(0);
  loadPixels();
  
  for(var y = 0; y < height; y++){
    for(var x = 0; x < width; x++){
      var index = (x + y * width) * 4;
        pixels[index] = random(0,255);
        pixels[index+1] = random(0,255);
        pixels[index+2] = random(0,255);
        pixels[index+3] = random(0,255);
    }
  }
 
  updatePixels();
}
````

### Vidoe Pixel Arrays
````Javascript
let video;
function setup() {
  createCanvas(400, 400);
  pixelDensity(1);
  video = createCapture(VIDEO);
  video.size(400, 400)
}

function draw() {
  background(0);
  
  video.loadPixels()
  loadPixels();
  
  for(var y = 0; y < height; y++){
    for(var x = 0; x < width; x++){
      var index = (x + y * width) * 4;
        pixels[index] = video.pixels[index];
        pixels[index+1] = video.pixels[index+1];
        pixels[index+2] = video.pixels[index+2];
        pixels[index+3] = video.pixels[index+3];
    }
  }
 
  updatePixels();
}
````

````Javascript
let video;
function setup() {
  createCanvas(400, 400);
  pixelDensity(1);
  video = createCapture(VIDEO);
  video.size(400, 400)
}

function draw() {
  background(0);
  
  video.loadPixels()
  loadPixels();
  
  for(var y = 0; y < height; y++){
    for(var x = 0; x < width; x++){
      var index = (x + y * width) * 4;
      
      var r = video.pixels[index];
      var g = video.pixels[index+1];
      var b = video.pixels[index+2];
      
      
      
        pixels[index] = r;
        pixels[index+1] = g;
        pixels[index+2] = b;
        pixels[index+3] = 255;
    }
  }
 
  updatePixels();
}
````
````Javascript
let video;
let vScale = 20;
function setup() {
  createCanvas(800, 600);
  pixelDensity(1);
  video = createCapture(VIDEO);
  video.size(width/vScale, height/vScale)
}

function draw() {
  background(0, 0, 255);
  
  video.loadPixels()
  loadPixels();
  
  for(var y = 0; y <= video.height; y++){
    for(var x = 0; x <= video.width; x++){
      var index = (video.width - x + 1 + (y * video.width)) * 4;
      var r = video.pixels[index];
      var g = video.pixels[index+1];
      var b = video.pixels[index+2];
      
        var bright = (r+g+b)/3; 
        var mapBright = map(bright, 0, 255, 0, vScale);
        noStroke();
        fill(255, 255, 0);
        rectMode(CENTER)
        rect(x*vScale, y*vScale, mapBright, mapBright)
    }
  }

}
````