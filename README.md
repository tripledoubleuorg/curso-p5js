# P5.js
O p5.js é uma biblioteca JavaScript open-source para código criativo.
– [https://p5js.org/]

## Conteudos
- Do processing ao p5.js
– Editor do p5.js
- Funções Estruturais
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
O P5.js tem o seu próprio editor [editor.p5js.org] ou podemos fazer o download e montar localmente [p5js.org/download].

O P5.js funciona através de funções, que são conjuntos de instruções para que se execute uma tarefa. Uma função tem que ser definida e chamada e a sua estrutura é constituída por instruções e argumentos.

No site do P5.js podemos encontrar uma série de funções pré-definidas: [p5js.org/reference]

Entre elas temos duas funções estruturais:
- `setup()` → acontece apenas uma vez
- `draw()` → está sempre em loop de cima para baixo

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