# Primeros Sktech en P5

## Estructura básica

Un sketch tiene dos partes básicas:

```javascript
//El setup() que se ejecuta al ejecutar el programa
function setup(){
    //Paso 1a
    //Paso 1b
    //Paso 1c
}
```
```javascript
//El draw() que se ejecuta cíclicamente
function setup(){
    //Paso 2a
    //Paso 2b
    //Paso 2c
}
```
## Dibujando una línea
Por ejemplo para dibujar una línea:
```javascript
function setup(){
    createCanvas(480, 120);
}

function draw(){
    background(204);
    
    line(20, 50, 420, 110);
}
```
![Línea](https://github.com/daniels13ca/Intro_Programacion/blob/master/images/L%C3%ADnea.JPG "Línea recta")

## Coordenadas
![Sistema de coordenadas](https://github.com/daniels13ca/Intro_Programacion/blob/master/images/Coordenadas.JPG "Sistema de coordenadas")

[Ejemplo Sistema de coordenadas](https://www.openprocessing.org/sketch/743823)

## Primitivas 2D
![Primitivas 1](https://github.com/daniels13ca/Intro_Programacion/blob/master/images/primitivas1.JPG "Primitivas 1")
![Primitivas 2](https://github.com/daniels13ca/Intro_Programacion/blob/master/images/primitivas2.JPG "Primitivas 2")

## Radianes
![Radianes](https://github.com/daniels13ca/Intro_Programacion/blob/master/images/radianes.JPG "Radianes")

Algunos ejemplos de `arch()`:

```javascript
function setup(){
    createCanvas(480, 120);
}

function draw(){
    background(204);
    
    arc(90, 60, 80, 80, 0, HALF_PI);
	arc(190, 60, 80, 80, 0, PI+HALF_PI);
	arc(290, 60, 80, 80, PI, TWO_PI+HALF_PI);
	arc(390, 60, 80, 80, QUARTER_PI, PI+QUARTER_PI);
}
```

Si se prefiere trabajar con grados se pueden usar dos estrategias:

* Función `radians()`:
```javascript
arc(90, 60, 80, 80, 0, radians(90);
```

* Establecer el `angleMode()`:
```javascript
function setup(){
    createCanvas(480, 120);
    angleMode(DEGRESS);
}
```

## Colores




