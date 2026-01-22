```markdown
# Ejercicios Prácticos del Módulo 1: Fundamentos y Sintaxis Básica - JavaScript

## Ejercicio 1: Variables y Ámbito (Scope)

### Enunciado:
Implementa un programa que use `let` para declarar tres variables dentro de una función. Cada variable debe representar el estado de un jugador en un juego simple. Una para la vida (`vida`), otra para la energía (`energia`) y otra para el nivel (`nivel`). Asegúrate de cambiar el valor de cada variable en diferentes puntos del programa, pero no permitas que los valores se modifiquen fuera del ámbito de la función.

### Ejercicio Resuelto:
```javascript
function actualizarJugador() {
  let vida = 100;
  let energia = 75;
  let nivel = 1;

  // Modificar los valores según las condiciones del juego
  if (energia < 50) {
    energia += 25;
  }

  if (nivel === 3) {
    nivel++;
    vida += 20; // Bonificación de vida
  }

  console.log({ vida, energia, nivel });
}

actualizarJugador();
```

---

## Ejercicio 2: Operadores y Estructuras de Control

### Enunciado:
Escribe una función que tome un número como parámetro y verifique si es positivo, negativo o cero. Utiliza `if`, `else if` y `else` para la lógica condicional. Luego, calcula el valor absoluto del número sin usar la función `Math.abs()`.

### Ejercicio Resuelto:
```javascript
function verificarNumero(num) {
  if (num > 0) {
    console.log("El número es positivo.");
  } else if (num < 0) {
    console.log("El número es negativo.");
  } else {
    console.log("El número es cero.");
  }

  // Calcular el valor absoluto del número
  let valorAbsoluto = num < 0 ? -num : num;
  console.log(`Valor absoluto: ${valorAbsoluto}`);
}

verificarNumero(-5);
verificarNumero(10);
verificarNumero(0);
```

---

## Ejercicio 3: Funciones y Lógica de Programación

### Enunciado:
Crea una función que tome un array de números como parámetro. Esta función debe devolver `true` si todos los elementos del array son pares, o `false` en caso contrario. Utiliza el operador lógico `&&` y la estructura de control `for`.

### Ejercicio Resuelto:
```javascript
function sonTodosPares(arr) {
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] % 2 !== 0) {
      return false;
    }
  }
  return true;
}

console.log(sonTodosPares([2, 4, 6, 8])); // Debe devolver true
console.log(sonTodosPares([1, 3, 5, 7])); // Debe devolver false
```
```