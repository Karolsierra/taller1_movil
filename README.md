# Documentacion

## Constantes:
Las constantes en Kotlin son valores inmutables que se definen utilizando la palabra clave const. Estas se evalúan en tiempo de compilación y su valor no puede cambiar una vez asignado. Las constantes se utilizan generalmente para valores que son verdaderamente constantes en el contexto del programa, como valores matemáticos, configuraciones, y otros valores que no cambian durante la ejecución del programa.

    class Constantes {
        companion object {
            const val PI = 3.14159
        }
    }

##### - const val:
Define una constante en tiempo de compilación. Debe ser utilizada en el contexto de un objeto 'companion', 'object' o a nivel de top-level (global).
##### - Tiempo de Compilación:
El valor de la constante se conoce y se establece en el momento en que el código es compilado, no durante la ejecución del programa.



## Variables 
En Kotlin, las variables se pueden definir como mutables o inmutables utilizando 'var' y 'val', respectivamente.

    val contador: Int = 10
    var nombre: String = "Juan"
    nombre = "Pedro"

##### - val:
Define una variable inmutable. Una vez asignado su valor, este no puede cambiar. Es similar a 'final' en Java.
##### - var:
Define una variable mutable. El valor de una variable mutable puede cambiar a lo largo del programa.

## Valores Opcionales
Kotlin tiene un sistema de tipos que permite declarar valores que pueden ser nulos utilizando el operador '?'. Esto ayuda a prevenir errores de tipo 'NullPointerException'.

    var edad: Int? = 87

##### - Nullable Type (Int?):
El signo de interrogación '?' indica que la variable puede contener un valor de tipo Int o null.
##### - Manejo Seguro de Nulos:
Kotlin proporciona varias características para manejar valores nulos de forma segura, como operadores seguros ('?.', '?:'), el operador !! para forzar un valor no nulo, y funciones estándar como 'let', 'apply', y 'run'.



# Manejo De Flujo
El manejo de flujo en Kotlin incluye la utilización de estructuras de control como 'if', 'when', bucles 'for', 'while', y 'do-while'.

###  Estructura if:

    if (edad != null) {
        println("El valor de edad es $edad")
    } else {
        println("El valor de edad es null")
    }

##### - if y else:
Estructuras de control que permiten ejecutar bloques de código basados en una condición booleana.


### Estructura When:

    val estado = "activa"
    when (estado) {
        "activa" -> println("La cuenta está activa")
        "inactiva" -> println("La cuenta está inactiva")
        else -> println("Estado desconocido")
    }

##### - when:
Similar a 'switch' en otros lenguajes, permite ejecutar diferentes bloques de código basados en el valor de una expresión.


- ##### Bucles for, while, y do-while: Bucles for, while, y do-while:

        for (i in 1..10) {
            println(i)
        }
        
        var i = 1
        while (i <= 10) {
            println(i)
            i++
        }
       
        i = 1
        do {
            println(i)
            i++
        } while (i <= 10)
    
##### - for:
Itera sobre un rango, una colección, o cualquier otro objeto que provea un iterador.
##### - while y do-while:
Permiten ejecutar un bloque de código repetidamente mientras una condición sea verdadera. La diferencia principal es que 'do-while' asegura que el bloque de código se ejecute al menos una vez.


