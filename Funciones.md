# Funciones

## Descripción

Una función, subrutina o subprograma es un subalgoritmo que forma parte del algoritmo principal, el cual permite resolver una tarea específica y que puede ser invocada (utilizada) tantas veces como se requiera sin necesidad de volver a escribir todo el código.

![Funciones](https://raw.githubusercontent.com/daniels13ca/Intro_Programacion/master/images/Funciones.png)

Ya hemos usado algunas

`dist()`: Retorna la distancia entre dos puntos

Otras funciones que ya se encuentran implementadas por defecto son:

```javascript
setup()

draw()

createCanvas()

mousePressed()

line()
```


## Estructura

Los elemementos que componen una función son:

* Palabra reservada `function`
* Nombre de la función
* Parámetros de entrada
* Instrucciones a ejecutar
* Valor retornado **(opcional)**

```javascript
function suma(a, b){
    return a+b; 
} 
```

**Ejemplo 1:**

```javascript
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
  forma(mouseX, mouseY);
}

function forma(a, b){
  circle(a, b, 60);
  rect(a - 80, b - 30, 60, 60);
  rect(a + 20, b - 30, 60, 60);
}
```

![Ejemplo 1](https://raw.githubusercontent.com/daniels13ca/Intro_Programacion/master/images/Funciones1.png)

**Ejemplo 2:**

```javascript

function draw() {
  drawTarget(width * 0.25, height * 0.4, 200, 4);
  drawTarget(width * 0.5, height * 0.5, 300, 10);
  drawTarget(width * 0.75, height * 0.3, 120, 6);
}

function drawTarget(xloc, yloc, size, num) {
  const grayvalues = 255 / num;
  const steps = size / num;
  for (let i = 0; i < num; i++) {
    fill(i * grayvalues);
    ellipse(xloc, yloc, size - i * steps, size - i * steps);
  }
}

```

![Ejemplo 2](https://raw.githubusercontent.com/daniels13ca/Intro_Programacion/master/images/Funciones2.PNG)

## Recursión 

Es una función que se llama a si misma modificando el valor de un paramétro y teniendo un criterio de parada, es decir deja de invocarse cuando se cumple una condición.

### Ejemplo factorial

El factorial de un número es multiplicar dicho número por todos sus anteriores hasta llegar a 1. Se representa con una exclamación (!). 

**Por ejemplo:** 5! = 5x4x3x2x1 = 120

*Nota*: 0! = 1

```javascript

function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
  
  let f = factorial(5);
  textSize(32);
  text(f, 150, 150);
}

function factorial(n){
  if(n == 0){
    return 1;
  } else {
    return n * factorial(n-1);
  }    
} 

```

### Ejemplo Fibonacci

En matemáticas, la sucesión o serie de Fibonacci es la siguiente sucesión infinita de números naturales:

**0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55...**

La sucesión comienza con los números 0 y 1, y a partir de estos, «cada término es la suma de los dos anteriores», es la relación de recurrencia que la define.

A los elementos de esta sucesión se les llama números de Fibonacci. Esta sucesión fue descrita en Europa por Leonardo de Pisa, matemático italiano del siglo XIII también conocido como Fibonacci. Tiene numerosas aplicaciones en ciencias de la computación, matemática y teoría de juegos. También aparece en configuraciones biológicas, como por ejemplo en las ramas de los árboles, en la disposición de las hojas en el tallo, en las flores de alcachofas y girasoles, en las inflorescencias del brécol romanesco, en la configuración de las piñas de las coníferas, en la reproducción de los conejos y en cómo el ADN codifica el crecimiento de formas orgánicas complejas. De igual manera, se encuentra en la estructura espiral del caparazón de algunos moluscos, como el nautilus.

```javascript

function setup() { 
  createCanvas(400, 400);
} 

function draw() { 
  background(220);

  for (var i = 0;  i <= 10; i++) {
    var s = "fib(" + i + ") = " + fib(i);
    text(s, 100, 50 + i * 20);
  }
}

function fib(n) {
  if (n <= 0) {
    return 0;
  } else if (n == 1) {
    return 1;
  } else {
    return fib(n - 1) + fib (n - 2);
  }
}

```

### Tarea:

Crear un sketch estilo fractal

```javascript

function setup() {
  createCanvas(400, 400);
  background(0);
}

function draw() {

  drawCircle(width / 2, height / 2, 200);
  noLoop();
}

function drawCircle(x, y, r) {
  
  stroke(255);
  noFill();
  ellipse(x, y, r, r);
  if (r > 2) {
    drawCircle(x + r / 2, y, r / 2);
    drawCircle(x - r / 2, y, r / 2);
  }
}

```
![Fractal](https://raw.githubusercontent.com/daniels13ca/Intro_Programacion/master/images/Fractal.PNG)

