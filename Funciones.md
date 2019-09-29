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

![Ejemplo 2](https://raw.githubusercontent.com/daniels13ca/Intro_Programacion/master/images/Funciones2.png)

## Recursión 


Ejemplo fibonacci

Más avanzado: 

https://p5js.org/examples/structure-recursion.html

### Tarea:

Crear un sketch estilo fractal

https://editor.p5js.org/projects/Sk4bc9cp
