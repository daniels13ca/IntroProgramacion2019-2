# Ciclos

La utilización de ciclos (o bucles) permite crear de forma dinámica elementos de un sketch o controlar su comportamiento. La función `draw()` actua como un ciclo, ya que ejecuta constantemente todo el código que hay en ella de arriba a abajo.

Veamos un ejemplo:

*Nota: En este ejemplo se utilizarán tres nuevos elementos de P5:*

#### Función `map()`

Convierte un valor de un rango en su valor equivalente en otro rango:

`map(valor, inicio_rango_orginal, fin_rango_original, inicio_rango_nuevo, fin_rango_nuevo)`

#### Palabra reservada `let`

Se puede utilizar para indicar que se le está asignando un valor a una variable

`let rojo = 150`

#### Función `console.log()`

Sirve para imprimir en la consola información util para ver el estado de la ejecucución del sketch

`console.log(rojo);`

Ahora si al ejemplo:

```javascript
function setup() {
  createCanvas(400, 400);
}

function draw() {
	let rojo=map(mouseY,0,height,0,255);
	console.log(rojo);
  	background(rojo,0,0);
}
```

## Alcance de las variables

