# Ciclos

La utilización de ciclos (o bucles) permite crear de forma dinámica elementos de un sketch o controlar su comportamiento. La función `draw()` actua como un ciclo, ya que ejecuta constantemente todo el código que hay en ella de arriba a abajo.

**Veamos un ejemplo:**

*Nota: En este ejemplo se utilizarán tres nuevos elementos de P5:*

* **Función `map()`**

	Convierte un valor de un rango en su valor equivalente en otro rango:

	`map(valor, inicio_rango_orginal, fin_rango_original, inicio_rango_nuevo, fin_rango_nuevo)`

* **Palabra reservada `let`**

	Se puede utilizar para indicar que se le está asignando un valor a una variable

	`let rojo = 150`

* **Función `console.log()`**

	Sirve para imprimir en la consola información util para ver el estado de la ejecucución del sketch

	`console.log(rojo);`

Ahora sí, al ejemplo:

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

Las variables tienen un alcance global o local. Por ejemplo, las variables declaradas dentro de las funciones `setup()` o `draw()` solamente pueden ser usadas dentro de esas funciones. 

Las variables globales, esto es, variables declaradas fuera de `setup()` y `draw()`, pueden ser usadas en cualquier parte del programa. 

Si una variable local es declarada con el mismo nombre que una variable global, el programa usará el valor local para hacer sus cálculos dentro de la función. Las variables son localizadas dentro de cada bloque, el espacio entre llaves { y }.

## Estructura de los ciclos `for()`

![Ciclo For](https://raw.githubusercontent.com/daniels13ca/Intro_Programacion/master/images/CicloFor.jpg)

```javascript
for( let i =0; i< 10; i++){
	//Instrucciones
}	

```

### Ejemplo 1

```javascript
function setup() {
	createCanvas(windowWidth, windowHeight);
	background(246, 102, 121);   //'#F26DF9'
}

function draw() {

	for(let x=0; x<width ; x=x+40){
		stroke(254, 193, 149);
		strokeWeight(8);
		line(x,0,x,height);
	}
}
```

### Ejercicio 1:

Modificar el sketch anterior para crear el siguiente patrón:

![Ejercicio 1](https://raw.githubusercontent.com/daniels13ca/Intro_Programacion/master/images/Ejercicio%201.JPG)

### Ejemplo 2

```javascript
function setup() {
	createCanvas(windowHeight, windowHeight);
	background(255);
}

function draw() {
	background(255);
	for(let i=0;i<width;i=i+20){
		stroke('#D24646');
		strokeWeight(4);
		line(0,i,i,0);
	}

}
```
### Ejercicio 2:

Modificar el sketch anterior para crear el siguiente patrón:

![Ejercicio 2](https://raw.githubusercontent.com/daniels13ca/Intro_Programacion/master/images/Ejercicio%201.JPG)

