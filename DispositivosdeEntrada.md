```javascript
setup()

draw()

createCanvas()

mousePressed()

line()
```

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

La función mouseReleased() es llamada cada vez que un botón del ratón es soltado.

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

https://p5js.org/es/reference/#/p5/keyIsPressed

https://p5js.org/es/reference/#/p5/key

https://p5js.org/es/reference/#/p5/keyCode

https://p5js.org/es/reference/#/p5/keyPressed

https://p5js.org/es/reference/#/p5/keyReleased

https://p5js.org/es/reference/#/p5/keyTyped

https://p5js.org/es/reference/#/p5/keyIsDown

## Dispositivos móviles

https://p5js.org/es/reference/#/p5/touches

https://p5js.org/es/reference/#/p5/touchStarted

https://p5js.org/es/reference/#/p5/touchMoved

https://p5js.org/es/reference/#/p5/touchEnded

## Otros

Ejemplos arduino