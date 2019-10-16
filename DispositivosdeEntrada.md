# Dispositivos de entrada

Es posible interactura con un sketch a través de diferentes dispositivos de entrada tanto en equipos de escritorio como móviles, veamos algunas posibilidades:

## Mouse

### Mouse pressed

La función `mousePressed()` es llamada cada vez que un botón del ratón está siendo presionado.

```javascript
let value = 0;
function draw() {
  fill(value);
  rect(25, 25, 50, 50);
}
function mousePressed() {
  if (value === 0) {
    value = 255;
  } else {
    value = 0;
  }
}
```
### Mouse released

La función `mouseReleased()` es llamada cada vez que un botón del ratón es soltado.

```javascript
let value = 0;
function draw() {
  fill(value);
  rect(25, 25, 50, 50);
}
function mouseReleased() {
  if (value === 0) {
    value = 255;
  } else {
    value = 0;
  }
}
```

### Double clicked

Esta función se ejecuta cada vez que se detecta un click doble.

```javascript
let value = 0;
function draw() {
  fill(value);
  rect(25, 25, 50, 50);
}

function doubleClicked() {
  if (value === 0) {
    value = 255;
  } else {
    value = 0;
  }
}
```

## Teclado

### Key Is Pressed

La variable boolean de sistema `keyIsPressed` es verdadera (true) cuando cualquier tecla es presionada y falsa (false) si no hay ninguna tecla presionada

```javascript
function draw() {
  if (keyIsPressed === true) {
    fill(0);
  } else {
    fill(255);
  }
  rect(25, 25, 50, 50);
}
```

### Key

La variable de sistema `key` siempre contiene el valor más reciente de la tecla del teclado presionada. 

```javascript
function setup() {
  fill(245, 123, 158);
  textSize(50);
}

function draw() {
  background(200);
  text(key, 33, 65);
}
```

### Key Code

La variable keyCode es usada para detectar teclas especiales, como `BACKSPACE, DELETE, ENTER, RETURN, ESCAPE, SHIFT, CONTROL, OPTION, ALT, UP_ARROW, DOWN_ARROW, LEFT_ARROW, RIGHT_ARROW`. También puedes revisar las teclas especiales buscando el código keyCode de cualquier tecla en internet.

```javascript
function draw() {}
function keyPressed() {
  background('yellow');
  text(`${key} ${keyCode}`, 10, 40);
  print(key, ' ', keyCode);
  return false; // prevent default
}
```

### Key Pressed

La función `keyPressed()` es llamada una vez cada vez que una tecla es presionada. El código `keyCode` de la tecla presionada es almacenado en la variable `keyCode`. 

```javascript
let value = 0;
function draw() {
  fill(value);
  rect(25, 25, 50, 50);
}
function keyPressed() {
  if (keyCode === LEFT_ARROW) {
    value = 255;
  } else if (keyCode === RIGHT_ARROW) {
    value = 0;
  }
}
```

### Key Is Released

La función `keyReleased()` es llamada una vez cada vez que una tecla es soltada. 

```javascript
let value = 0;
function draw() {
  fill(value);
  rect(25, 25, 50, 50);
}
function keyReleased() {
  if (value === 0) {
    value = 255;
  } else {
    value = 0;
  }
  return false; // prevent any default behavior
}
```

### Key Typed

La función `keyTyped` es llamada cava vez que una tecla es presionada, excepto cuando son presionadas las teclas de acción como `Ctrl, Shift y Alt`, que son ignoradas. La tecla presionada más reciente será almacenada en la variable key. Por la forma en que los sistemas operativos manejan la repetición de teclas, mantener presionada una tecla puede causar múltiples llamadas a `keyTyped()` (y también `keyReleased()`).

```javascript
let value = 0;
function draw() {
  fill(value);
  rect(25, 25, 50, 50);
}
function keyTyped() {
  if (key === 'a') {
    value = 255;
  } else if (key === 'b') {
    value = 0;
  }
  // uncomment to prevent any default behavior
  return false;
}
```

### Key Is Down

La función `keyIsDown()` comprueba si la tecla está presionada. Puede ser usada si tienes un objeto que se mueve, y quieres que varias teclas sean capaces de afectar este comportamiento de manera simultánea, como cuando mueves una imagen de forma diagonal. Puedes ingresar cualquier número representando el código de tecla `keyCode` de la tecla, o usar cualquier de los nombres de la variable `keyCode`.

```javascript
let diameter = 50;

function setup() {
  createCanvas(512, 512);
}

function draw() {
  // 107 and 187 are keyCodes for "+"
  if (keyIsDown(107) || keyIsDown(187)) {
    diameter += 1;
  }

  // 109 and 189 are keyCodes for "-"
  if (keyIsDown(109) || keyIsDown(189)) {
    diameter -= 1;
  }

  clear();
  fill(255, 0, 0);
  ellipse(50, 50, diameter, diameter);
}
```

## Dispositivos móviles

https://p5js.org/es/reference/#/p5/touches

https://p5js.org/es/reference/#/p5/touchStarted

https://p5js.org/es/reference/#/p5/touchMoved

https://p5js.org/es/reference/#/p5/touchEnded

## Otros

Ejemplos arduino