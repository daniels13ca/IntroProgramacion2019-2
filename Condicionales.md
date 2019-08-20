# Condicionales

## Variables

La razón fundamental de las variables es evitar repetir código. Por ejemplo veamos el siguiente sketch:

![Variables 1](https://github.com/daniels13ca/Intro_Programacion/blob/master/images/Variables1.JPG "Variables 1")

```javascript
var y = 60;
var d = 80;

function setup(){
    createCanvas(480, 120);
}

function draw(){
    background(204);
    ellipse(75, y, d, d); //Izquierda
    ellipse(175, y, d, d); //Centro
    ellipse(275, y, d, d); //Derecha
}
```
Se puede modificar para que la posición en x sea dinámica:

```javascript
var x = 75;
var incre = 100;
var y = 60;
var d = 80;

function setup(){
    createCanvas(480, 120);
}

function draw(){
    background(204);
    ellipse(x, y, d, d); //Izquierda
    ellipse(x + incre, y, d, d); //Centro
    ellipse(x + incre*2, y, d, d); //Derecha
}
```

P5 ya tiene algunas variables predefinidas por ejemplo para crear el siguiente sketch:

![Variables 2](https://github.com/daniels13ca/Intro_Programacion/blob/master/images/Variables2.JPG "Variables 2")

```javascript
function setup() {
	createCanvas(480, 120);
}

function draw() {
	background(204);
	line(0, 0, width, height); // Línea desde (0,0) a (480, 120)
	line(width, 0, 0, height); // Línea desde (480,0) a (0, 120)
	ellipse(width/2, height/2, 60, 60);
}
```

No es necesario saber el tamaño del lienzo para ubicar los objetos (probar modificando los paramétros de `createCanvas(480, 120);`).

## Operadores

Al igual que en matématicas, en programación también existen operadores y entre ellos se tienen precedencias:
![Operadores](https://github.com/daniels13ca/Intro_Programacion/blob/master/images/Operadores.JPG "Operadores")

## Estructura `If`

![If](https://github.com/daniels13ca/Intro_Programacion/blob/master/images/Estructura%20If.png "If")

```javascript
var flag = 0;

function setup() {
	createCanvas(120, 120);
}

function draw() {
	background(204);
	
text('Flag:' + flag, 30, 30);
}

function mousePressed(){
	if(flag==0){
		flag=1;
	}else{
		flag=0;
	}
}
```

*Actividad*: Crear un sketch que modifique el color del fondo utilizando una bandera

La estructuras condicionales se pueden encadenar entre si:

![Múltiples If](https://github.com/daniels13ca/Intro_Programacion/blob/master/images/If_multiple.JPG "Múltiples If")

```javascript
var x;
var offset = 10;

function setup() {
	createCanvas(240, 120);
	x = width/2;
}

function draw() {
	background(204);
	if (mouseX > x) {
		x += 0.5;
		offset = -10;
	}
	if (mouseX < x) {
		x -= 0.5;
		offset = 10;
	}
	
	// Dibuja flecha izquierda o derecha según el valor "offset"
	line(x, 0, x, height);
	line(mouseX, mouseY, mouseX + offset, mouseY - 10);
	line(mouseX, mouseY, mouseX + offset, mouseY + 10);
	line(mouseX, mouseY, mouseX + offset*3, mouseY);
}
```

*Actividad*: Modificar el Sketch para que presente el mismo comportamiento pero sobre el eje y

*Ejemplo*: Si el mouse estra dentro de un círculo no hace nada, si el mouse se encuentra por fuera aumenta su radio y cambia de color:

![Círculos 1](https://github.com/daniels13ca/Intro_Programacion/blob/master/images/Circulos%201.JPG "Círculos 1")

Para este caso, se utiliza la función `dist()` que obtiene la distancia entre el centro del círculo y la posición del mouse:

![Círculos 2](https://github.com/daniels13ca/Intro_Programacion/blob/master/images/Circulos%202.JPG "Círculos 2")

```javascript
var x = 120;
var y = 120;
var radio = 12;

function setup() {
	createCanvas(240, 240);
	ellipseMode(RADIUS);
}

function draw() {
	background(204);
	var d = dist(mouseX, mouseY, x, y);
	if (d < radio) {
		radio++;
		fill(0);
	} else {
		fill(255);
	}
	ellipse(x, y, radio, radio);
}
```
*Actividad*: Modificar el Sketch para que el círculo detenga su crecimiento cuando llegué al borde del lienzo

**Tarea**: Modificar el Sketch del personaje para que reaccione al click, por ejemplo cambie de color, mueva un ojo, etc. Se evaluará cuando este subido en Open Processing.

### Proyecto (07 de Septiembre)

**Exposición (30%)**:
* Creative Aplications (https://www.creativeapplications.net/)
* Expirements with Google (https://experiments.withgoogle.com/)
* School for poetic computation (https://sfpc.io/projects/)
* DevArt - Art Made by Code (https://devart.withgoogle.com/)
* YesYesNo (http://www.yesyesno.com/)
* Art from Code (http://www.artfromcode.com/)

**Sketch (50%)**: Crear un sketch creativo aplicando todo lo visto hasta la clase del 31 de Agosto. Se evaluará el sketch en Open Processing antes de la clase.

**Sustentación sketch (20%)**: Presentar en clase el sketch creado y realizar una modificación a petición del profesor.