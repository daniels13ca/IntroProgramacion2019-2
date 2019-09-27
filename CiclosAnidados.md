# Ciclos anidados

En muchos casos se requiere controlar el valor de paso de dos o más variables a la vez, en este caso es necesario "anidar" ciclos:

```javascript

for (let i = 0; i< 10; i++){ //Ciclo que controla la variable 1

  for (let j = 0; j < 10; j++){ //Ciclo que controla la variable 2
  
    //Conjunto de instrucciones que involucran a las variables 1 y 2
  }

}

```

### Ejemplo 1:

![Anidados 1](https://raw.githubusercontent.com/daniels13ca/Intro_Programacion/master/images/Anidado1.JPG)

```javascript

function setup(){
  createCanvas(windowWidth,windowHeight);
}

function draw(){
  background(0);
	
  for(let i=40;i<width-10;i=i+(width/18)){
    for(let j=40;j<height-30;j=j+(height/9)){
      
      noStroke();
      fill(180, 8+2*(i/30)+2*(j/30) , 0);
      ellipse(i,j,8+2*(i/120)+2*(j/120),8+2*(i/120)+2*(j/120));
    
    }
  }
}

```

### Ejemplo 2:

```javascript

var diameter = 50;
var red;
var green;
var blue;

function setup() {
	createCanvas(windowWidth, windowHeight);
	frameRate(2); //Nueva función
	background('#F4EDDD');
}

function draw() {

	noStroke();
	for (let i=0; i<width; i=i+diameter) {
		
		for (let j=0; j<height; j=j+diameter) {
      
                        red = random(240,255);
 			green = random(100,255);    
 			blue = random(0,190);
      
                        fill(red,green,blue);
                        ellipse(  i ,  j , 100, 100 );
		}
	}
}

```
![Anidados 2](https://raw.githubusercontent.com/daniels13ca/Intro_Programacion/master/images/Anidado2.gif)

Taller:

Utilizando lo visto hasta el momento crear un patrón similar a los siguientes:

[![Anidados 3](https://raw.githubusercontent.com/daniels13ca/Intro_Programacion/master/images/Anidado3.JPG)](https://www.pinterest.es/pin/557601997597674030/)

El resultado se debe subir en OpenProcessing a más tardar a las 11:00 a.m. (Se dan puntos adicionales por mejoras a lo propuesto).
