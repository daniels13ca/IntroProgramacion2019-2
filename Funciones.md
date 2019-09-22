# Funciones

## Descripción

Una función, subrutina o subprograma es un subalgoritmo que forma parte del algoritmo principal, el cual permite resolver una tarea específica y que puede ser invocada (utilizada) tantas veces como se requiera sin necesidad de volver a escribir todo el código.

![Funciones](https://raw.githubusercontent.com/daniels13ca/Intro_Programacion/master/images/Funciones.png)

Ya hemos usado algunas

`dist()`: Retorna la distancia entre dos puntos

Otras funciones que ya se encuentran implementadas por defecto son:

`setup()
draw()
createCanvas()
mousePressed()
line()`


## Estructura

Los elemementos que componen una función son:

* Palabra reservada `function`
* Nombre de la función
* Parámetros de entrada
* Instrucciones a ejecutar
* Valor retornado **(opcional)**

`
function suma(a, b){
  return a+b; 
} 
`

**Ejemplo:**

`
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
`


Más avanzado:

https://p5js.org/examples/structure-functions.html

## Recursión 
Ejemplo fibonacci

Más avanzado: 

https://p5js.org/examples/structure-recursion.html

Tarea:

Crear un sketch estilo fractal

https://editor.p5js.org/projects/Sk4bc9cp
