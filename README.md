# Preguntas y respuestas sobre fundamentos de programación

---

**¿Qué es un hash?**  
Un **hash** es una función que recibe una entrada y devuelve un valor fijo que sirve como identificador. No garantiza unicidad, pero distribuye bien los valores, lo cual es útil para estructuras como `HashMap` o `HashSet`.

---

**¿Por qué estaría mal conjunto desordenado?**  
Porque un conjunto, por definición matemática, no tiene orden. Decir "conjunto desordenado" es redundante. En estructuras como `Set`, los elementos no están ordenados.

---

**¿En qué se basa la complejidad?**  
La complejidad se basa en analizar el **peor caso**. Existen dos tipos principales: **temporal** (tiempo de ejecución) y **espacial** (uso de memoria).

---

**Inmutabilidad: ¿Qué aporta a la programación funcional?**  
Aporta **seguridad, facilidad para depurar, paralelismo seguro** y **predecibilidad**, ya que los datos no cambian una vez creados.

---

**¿Cómo se puede ordenar sin comparar?**  
Con algoritmos como `CountingSort`, `RadixSort`, y `BucketSort`, que usan propiedades de los datos sin compararlos directamente.

---

**¿Qué es el estado de un objeto?**  
Es el **conjunto de valores actuales de sus atributos**.

---

**¿Qué usa el backtracking?**  
Usa **recursividad, caso base, y criterios** como **elección, restricción, meta y retroceso** para explorar soluciones y retroceder cuando una no sirve.

---

**¿Qué es el caso base?**  
Es la **condición que detiene la recursión**, evitando un bucle infinito.

---

**¿Qué es el caso recursivo?**  
Es la parte de la función que se **llama a sí misma** con una versión reducida del problema.

---

**¿Cuándo un método recursivo se vuelve iterativo?**  
Cuando se reescribe usando **bucles** y estructuras auxiliares (como pilas).

---

**¿Cuándo un método iterativo se vuelve recursivo?**  
Cuando se reemplazan bucles por **llamadas recursivas**, definiendo un **caso base**.

---

**¿Qué es una interface?**  
Una **interfaz** define un conjunto de métodos que una clase debe implementar. No contiene lógica, solo la **firma de los métodos**.

---

**¿Qué es un mapeo?**  
Puede referirse a:
- Un **Map** (asociación clave-valor).
- La operación funcional `map`, que **transforma una colección** aplicando una función a cada elemento.

---

**¿Qué es el mapeo unidimensional?**  
Es **convertir estructuras como matrices en vectores**, accediendo a través de una fórmula de indexado lineal.

---

**¿Qué es el reduce?**  
Una operación que **reduce una colección a un solo valor**, aplicando una función acumuladora.

---

**Fases de iteración:**

1. **Inicialización**  
   Es el punto de partida de la iteración. Aquí se declara e inicializa la variable de control del ciclo (por ejemplo, `i = 0`). Esta fase se ejecuta una sola vez, justo antes de que empiece el bucle.

2. **Condición**  
   Es la expresión lógica que determina si el ciclo debe seguir ejecutándose. Se evalúa **antes** de cada repetición. Si la condición es verdadera, el cuerpo del bucle se ejecuta. Si es falsa, se termina el bucle.

3. **Ejecución del cuerpo del ciclo**  
   Es el bloque de instrucciones que se ejecuta cada vez que la condición es verdadera. Aquí se realiza la lógica principal de la iteración (como procesar un dato, modificar un arreglo, etc.).

4. **Actualización**  
   Modifica la variable de control (por ejemplo, `i++`). Esto es esencial para evitar bucles infinitos y para acercarse a la condición de salida.

5. **Fin o repetición**  
   Al terminar la ejecución del cuerpo y actualizar la variable, el ciclo **vuelve a evaluar la condición**. Si la condición se mantiene verdadera, el proceso se repite. Si no, el bucle finaliza.

---

**¿Qué hace o cómo se lee `Person::getName`?**  
Es una **referencia a método** que equivale a `p -> p.getName()` para cada objeto `Person`.

---

**¿Qué hace el método `.filter`?**  
Aplica un **predicado (función booleana)** y devuelve solo los elementos que lo cumplen.

---

**¿Cuáles son las 3 maneras de hacer bucles?**  
1. Iteración tradicional  
2. Recursividad  
3. Estilo funcional (`map`, `reduce`, `filter`)

---

**¿Cómo asegurar que un algoritmo recursivo no desborda la pila?**  
- Definir correctamente el **caso base**  
- Asegurar que cada llamada **reduce el problema**  
- Evitar ciclos infinitos

---

**¿Diferencia entre poner `final` a un atributo primitivo, un String, un objeto, un array, una clase o método?**  
- Primitivo: su valor no cambia.  
- String: no se puede cambiar la referencia.  
- Objeto: no cambia la referencia, pero sí su contenido.  
- Array: igual que objeto.  
- Método: no puede sobrescribirse.  
- Clase: no puede heredarse.

---

**¿En recursividad y operaciones no igualitarias, cómo se altera el resultado?**  
El orden importa. En operaciones **no conmutativas** como resta o división, cambiar el orden **altera el resultado**.

---

**¿Algoritmos de comparación vs algoritmos sin comparación para ordenamiento?**  
- Con comparación: usan `<`, `>`, mínimo `O(n log n)`  
- Sin comparación: como `CountingSort`, pueden ser `O(n)` con restricciones

---

**¿Qué es la fase de ida y fase de vuelta en recursividad?**  
- Ida: cuando las llamadas recursivas **se apilan**.  
- Vuelta: cuando el flujo **retorna hacia arriba**.

---

**¿Cuál es la diferencia de una ordenación estable vs inestable?**  
- Estable: elementos iguales **mantienen su orden**.  
- Inestable: pueden **reordenarse** arbitrariamente.

---

**¿Qué es un ArrayList, en qué se diferencia de los arrays tradicionales y qué ventajas tiene?**  
Es una lista dinámica que puede **crecer o disminuir** automáticamente. Ofrece más métodos que un array tradicional.

---

**Criterios del backtracking:**  

El backtracking es una técnica de **búsqueda sistemática** en la que se exploran todas las soluciones posibles y se retrocede (backtrack) cuando una opción no lleva a una solución válida. Se basa en los siguientes criterios:

1. **Elección**  
   En cada paso del algoritmo se elige una opción dentro de un conjunto de posibilidades. Estas elecciones representan una **rama en el árbol de soluciones**. Por ejemplo, elegir una letra en un problema de anagramas.

2. **Restricción**  
   Son las **condiciones que deben cumplirse** para que una solución parcial sea válida. Si una elección viola una restricción, se descarta esa rama y se vuelve atrás. Esto **acota la búsqueda** evitando recorrer caminos inútiles.

3. **Meta**  
   Es el **criterio de aceptación** que define si una solución parcial o total es válida o completa. Por ejemplo, si ya se colocaron todas las reinas en el problema de las 8 reinas sin atacar, se ha alcanzado la meta.

4. **Retroceso (backtrack)**  
   Cuando una solución parcial no puede llevar a una solución completa válida (por violar restricciones o no alcanzar la meta), se **deshace la última elección** y se prueba una alternativa. Este es el mecanismo que distingue al backtracking de una búsqueda por fuerza bruta.

---

**¿Diferencia entre eficiencia y complejidad temporal de un algoritmo?**  
- Complejidad temporal: medida teórica (en función de `n`)  
- Eficiencia: desempeño práctico, considerando implementación y recursos

---

**¿En qué teoría se basan los métodos de `enum`?**  
En la **teoría de conjuntos** y los **tipos algebraicos enumerados**, donde hay un conjunto finito y cerrado de valores.

---

**Clasificación de algoritmos de ordenación:**  
- Internos vs Externos  
- Estables vs Inestables  
- In-place vs con memoria extra  
- Naturales  
- Híbridos (como `TimSort`)

---

**Diferencia entre inorden, preorden y postorden:**  
- **Inorden**: izquierda → nodo → derecha  
- **Preorden**: nodo → izquierda → derecha  
- **Postorden**: izquierda → derecha → nodo

---

**¿Recursividad vs Iteración?**  
- **Recursividad**: se llama a sí misma hasta el caso base  
- **Iteración**: repite con bucles (`for`, `while`)

---

**¿Qué no es un algoritmo?**  
Algo que **no es claro, no tiene fin, o no es reproducible**. Si no tiene pasos definidos y termina, no es un algoritmo.

---

**¿Qué es un algoritmo?**  
Un conjunto **finito, ordenado y claro de pasos** para resolver un problema o realizar una tarea.

---

**Ordenación**

|Ordenación...|||
|-|-|-|
|**In-place**|Cuando el algoritmo de ordenación utiliza **espacio constante** para producir la salida (modifica únicamente el array dado).|Selection Sort, Bubble Sort, Insertion Sort y Heap Sort.|
|**Interna**|Cuando todos los datos se colocan en la **memoria principal** o **memoria interna**. En la ordenación interna, el problema no puede recibir entradas más allá del tamaño de memoria asignado.|La mayoría de los clásicos.

---

**Algoritmos**

|Algoritmo||Características|
|-|-|-|
|**[Bubble Sort]**|Compara pares adyacentes y los intercambia si están en desorden.|- Simple de entender<br>- Muy ineficiente para listas grandes<br>- Estable: mantiene el orden de elementos iguales|
|**[Selection Sort]**|Encuentra el mínimo y lo coloca al inicio de la lista no ordenada.|- No es eficiente para listas grandes<br>- Inestable en su forma básica<br>- Realiza menos intercambios que Bubble Sort|
|**[Insertion Sort]**|Construye la lista final un elemento a la vez, insertando cada nuevo elemento en su lugar correcto.|- Eficiente para listas pequeñas o parcialmente ordenadas<br>- Estable: mantiene el orden de elementos iguales<br>- Opción ideal para inserción en tiempo real|*rt]**|Divide la lista en mitades, ordena cada mitad y luego las fusiona.|- Eficiente y tiene una complejidad de tiempo constante \(O(n \log n)\)<br>- Estable: mantiene el orden de elementos iguales<br>- Utiliza memoria adici arreglo temporal|*rt]**|Selecciona un 'pivote' y particiona los elementos alrededor de él antes de ordenar las sublistas.|- Generalmente más rápido que otros \(O(n \log n)\), pero su rendimiento depende del pivote<br>- Inestable: puede cambiar el orden d>- Puede degradarse a \(O(n^2ige un mal pivote|
|**apSort.md)**|Utiliza una estructura de heap para ordenar los elementos.|- Complejidad de tiempo constante \(O(n \log n)\)<br>- Inestable: puede cambiar el orden de elementos iguales<br>- No requiere memoria adicional, a diferencia de Merge Sort|
|**[Counting Sort]**|Utiliza un arreglo de conteo para organizar los elementos según su clave.|- Lineal \(O(n)\) para rangos de claves pequeños<br>- Estable: puede mantener el orden de entrada de elementos iguales<br>- No adecuado para datos con claves numéricas muy dispersas|
|**[Radix Sort]**|Ordena los elementos digito por digito, empezando por el menos significativo.|- Lineal \(O(n)\) para números de dígitos fijos<br>- Estable: adecuado para datos con múltiples dígitos<br>- Requiere una función de conteo eficiente como Counting Sort para cada dígito|
|**[Bucket Sort])**|Distribuye los elementos en varios 'buckets' o contenedores y luego ordena cada bucket individualmente.|- Eficiente cuando los datos se distribuyen uniformemente<br>- Estable si el ordenador de buckets es estable<br>- Rendimiento depende de la distribución de los datos|
|**[Intro Sort]**|Abreviatura de *Introspective Sort*, representa un paradigma de ordenamiento híbrido que combina estratégicamente tres algoritmos fundamentales: QuickSort, HeapSort e Insertion Sort.|- Rendimiento predecible en todos los escenarios<br>- Optimización adaptativa<br>- Eficiencia para subconjuntos pequeños<br>- Robustez frente a ataques algorítmicos<br>- Balance óptimo entre complejidad teórica y práctica
