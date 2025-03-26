# Estructuras de control - Estructura de modularizaríon **Funciones**.

## Introducción:

En `JavaScript`, las funciones son bloques de códigos reautilizables que encapsulan una serie de instrucciones diseñadas para realizar una tarea específica. Son fundamentales para organizar y estructurar el código, permitiendo la reutilización, la modularización y la abstracción de la lógica de programación.


<hr>

## Clasificación de funciones en **JavaScript**.

- Declaración de funciones *(Funciones nombradas)*.

Es un tipo específico de función nombrada en `JavaScript`. Cuandp defines una función utilizando la palabra clave `function` seguida de un nombre, como en el siguiente ejemplo:

```JavaScript
    function saludar(nombre)    //defino la función.
        {
            console.log("Hola, "+nombre+"¿Cómo estás?");
        }                       //Llamada a la función.
    saludar("Juan");            // Output: Hola, Juan ¿Cómo estás?
```

- Expresión de función.

Asigna una función a una constante:

```JavaScript
    const sumar = function(a, b)
        {
            return a+b;
        }
```

Si utilizas `const`, estás indicando que la variable no cambiará de refencia a la función después de la inicialización. Esto significa que no podrás asignar otra función o valor a esa variable más adelante en tu código.

asigna una función a una variable:

```JavaScript
    let sumar = function()
        {
            return a+b;
        }
```

Si usas `let`, estás permitiendo que la variable pueda cambiar de referencia a otra función o valor más adelante en tu código si es necesario.

<hr>

- Funciones con y sin retorno. 

**Funciones con retorno.**

Una función con retorno devuelve un valor cuando es invocada. Esto se logra utilizando la palabra clave `return` dentro del cuerpo de la función para especificar qué valor debe devolverse.

*Ejemplo de función con retorno:*

```JavaScript
function sumar(a, b)
    {
        return a + b;
    }                   
    //Llamada a la función y uso del valor devuelto.
let resultado = sumar(5, 3);
console.log(resultado); // Output: 8
```
**Funciones sin retorno.**

Una función puede no tener un valor de retorno explícito, en cuyo caso la función simplemente realiza ciertas acciones o tareas sin devolver un valor específico usando `return`.

*Ejemplo de función sin retorno:*

```JavaScript
    function saludar(nombre)
        {
            console.log("Hola, "+nombre+"¿Cómo estás?");
        }
    //Llamada a la función (sin usar el valor de retorno).
    saludar("Juan"); // Output: Hola, Juan ¿Cómo estás?
```

<hr>

- Función Anónimas:

Funciones sin nombre, útiles para casos donde solo se necesitan una vez.

*Ejemplo:*

```JavaScript
// Función anónima asignada a una variable.
let saludar = function(nombre)
                {
                    console.log("Hola, "+nombre+"¿Comó estás?");
                }
//Llamada a la función anónima
saludar("Juan"); // Output: Hola, Juan ¿Comó estás?
```
<hr>

- Función flecha *(Arrow Function)*

Una sintaxis más concisa para definir funciones anónimas.

*Ejemplo:*

```JavaScript
    const multiplicar = (x, y) => {
        return x * y;
    }

console.log(multiplicar(6,2)); //Output: 12
```
<hr>

- Función como parámetro:

Pasando funciones como argumentos a otras funciones.

```JavaScript
function operar(a, b, operacion)
    {
        return operacion(a, b);
    }
const resultado  = operar(10, 5, function(a, b){
    return a - b;
        });
```

<hr>