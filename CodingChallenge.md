#Coding Challenge

## Reglas

1. Etapa 1: Presentación de un ejemplo que sirve como base para el desarrollo del reto
2. Etapa 2: Desarrollo del reto de forma individual
3. Solo se aceptarán lo resultados subidos en OpenProcessing antes de las 11:00 a.m. (Se recomienda subier lo que tengan en ese momento así no este terminado)

## Etapa 1

![Reto 1](https://raw.githubusercontent.com/daniels13ca/Intro_Programacion/master/images/Reto1.JPG)

```javascript
function setup() {
	createCanvas(windowHeight, windowHeight);
}

function draw() {
	background('#507DBC');
	for (let i = 0; i < height; i = i + 20) {
		line(i, 0, 0, height - i);
	}
}
```

## Etapa 2

A partir del sketch de la Etapa 1, crear un propuesta creativa que lo modifique aumentando su complejidad, por ejemplo:

![Reto 2](https://raw.githubusercontent.com/daniels13ca/Intro_Programacion/master/images/Reto2.JPG) 
