# Ejemplos de Métodos de Arrays en JavaScript

Este repositorio contiene ejemplos prácticos de los métodos más comunes y modernos de arrays en JavaScript. Cada método incluye una breve descripción y un ejemplo de uso.

## Métodos Incluidos

- `at()`
- `concat()`
- `copyWithin()`
- `entries()`
- `every()`
- `fill()`
- `filter()`
- `find()`
- `flat()`
- `flatMap()`
- `map()`
- ... y muchos más.

# Métodos de Arrays y Principios SOLID

Este proyecto explora cómo los métodos nativos de JavaScript para trabajar con arrays implementan o reflejan los principios SOLID de diseño de software. A continuación, se describen brevemente cada principio y su relación con los métodos utilizados.

## Principios SOLID y su Relación con los Métodos de Arrays

### 1. S - Principio de Responsabilidad Única (Single Responsibility Principle)  
Cada método de array tiene una única responsabilidad bien definida:  
- **`Array.prototype.map()`**: transforma elementos según una función dada.  
- **`Array.prototype.filter()`**: selecciona elementos que cumplen una condición.  
- **`Array.prototype.reduce()`**: reduce el array a un único valor acumulado.  
Cada método realiza una tarea específica, evitando mezclar responsabilidades.

### 2. O - Principio Abierto/Cerrado (Open/Closed Principle)  
Los métodos nativos del array están abiertos a la extensión (se pueden combinar para realizar nuevas operaciones) pero cerrados a su modificación. Ejemplos:  
- **`Array.prototype.flatMap()`**: extiende la funcionalidad de `map()` y `flat()` sin modificar ninguno.  
- Los métodos pueden combinarse sin cambiar su comportamiento original.

### 3. L - Principio de Sustitución de Liskov (Liskov Substitution Principle)  
Los métodos de arrays pueden aplicarse a cualquier array sin alterar su funcionalidad. Ejemplos:  
- **`Array.prototype.find()`**: se comporta igual sin importar los valores del array.  
- **`Array.prototype.sort()`**: ordena cualquier conjunto de datos, siempre que el comparador sea válido.

### 4. I - Principio de Segregación de Interfaces (Interface Segregation Principle)  
Cada método es una interfaz específica para una operación concreta, evitando depender de métodos innecesarios. Ejemplos:  
- **`Array.prototype.findIndex()`**: se usa para encontrar índices en lugar de depender de métodos más complejos.  
- **`Array.prototype.keys()`**: permite iterar únicamente sobre los índices del array.

### 5. D - Principio de Inversión de Dependencia (Dependency Inversion Principle)  
Los métodos de array dependen de abstracciones bien definidas (como las funciones pasadas a `map()` o `reduce()`), no de implementaciones concretas. Ejemplos:  
- **`Array.prototype.reduce()`**: se basa en una función genérica para definir cómo acumular valores, permitiendo diversas implementaciones.  
- **`Array.prototype.sort()`**: depende de una función de comparación genérica, manteniéndose flexible.

## Uso

Clona el repositorio para explorar los ejemplos:
```bash
git clone https://github.com/Javigarcilop/js-metodos-array-ejemplos.git

