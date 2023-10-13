  * Estado del Arte
    * Castellano 3 a 4 páginas
  * Short Paper
    * 4 páginas doble columna
    * Inglés
  * # Diferencias
    * Ingeniería
      * Aplicación de conocimiento
    * Investigación
      * Buscar nuevos métodos y técnicas
      * Crear conocimiento
      * Búsqueda sistematica
        * Para descubrir o revisar teorías
  * Investigación
    * ¿Reinventar la rueda?
    * En computer science
    * ¿Por qué no reinventar la rueda?
      * No proponer lo que ya existe
      * No proponer algo menos eficiente
      * Pero!, depende del contexto
  * Crear nuevos conocimientos
    * Nuevas técnicas
    * Nuevos Algoritmos
    * Nuevas teorías
    * Mejorar cosas ya existentes
    * Adaptar técnicas a un contexto diferente
  * Donde empezar
    * Entado del arte
  * Donde encontrarlo
    * Enciclopedias
    * Biblioteca
    * Librerías Digitales
      * dl.acm.org
      * ieeexplore.ieee.org
      * springerlink.com
      * sciencedirect.com
      * CCSB (Colection of computer science)
      * CiteSeeer.x (CiteSeer)
      * Google Scholar (GS)
      * Arxiv
      * researchgate.net
  * # Estado del Arte
    * ## Leer papers
      * Leer de forma crítica
      * Leer de forma creativa
    * ### Tips
      * Leer paper
        * Identificar el contexto
          * Abstract
        * Autores
        * Institución ó que conferencia
        * Hay que saber que hay nuevo, la contribución
          * Ideas claves
      * Tomar notas
    * ## Proceso critico
      * No asumir que los autores tienen la razón
      * ¿Están resolviendo que corresponde?
      * ¿Existen soluciones más simples que los autores publican?
      * ¿Cuales son las limitaciones que se proponen en el paper?
        * Limitaciones
          * Problemas especificos
          * Noob???
      * ¿Lo que asumen los autores es razonable?
      * ¿Interpretan los datos de manera razonable?
      * ¿Qué es lo que hacen realmente?
      * ¿Cuales son las contribuciones?
        * Una frase
      * ¿Cuales son los métodos que están usando?
      * ¿Todas las piezas encajan?

    * ## Lectura creativa
      * ¿Cuales son las ideas buenas?
      * ¿Tienen otras aplicaciones o extensiones?
      * ¿Se puede generalizar más allá del método?
      * ¿Cuales son las mejoras posibles?
      * ### Tips
        * Leer titulo
        * Leer abstract
        * Leer introducción
          * Motivación, relación con otros trabajos
        * Mirar la estructura
          * Formalización
          * Experimentos / Resultados
          * Discución
        * Leer el trabajo previo hecho
        * Leer las conclusiones
        * Leer el cuerpo del paper
        * Referencias son importantes (Zotero)
          * Manejo del tema
          * Contexto general
          * Buen punto de partida para el problema
        * Tratar de hacer un resumen del paper en dos frases
        * Comparar papers
          * ¿Nueva idea?
        * Escribir el informe del paper
          * Es como escribir un short paper (1 página)
          * ¿Cuál es el título?
          * Autores
          * De que revista/conferencia
          * ¿Qué año?
          * Resumen 2 ó 3 frases
          * Ideas principales
          * ¿Cuál es el problema?
          * ¿Cuál es la solución?
          * ¿Cuál es la tasa de error?, ¿Cuales son los resultados?
          * ¿Qué tipo de algoritmo usa?
          * ¿Se puede mejorar?
          * Debilidades
          * Fortalezas
    * 1. Algoritmo en general -> Implementación
      * Especificaciones
        * Datos de entrada/salida
          * ¿Existe un formato normalizado? (Benchmark)
      * Partir de un pseudo-código
        * Generar una implementación (sin optimización)
    * 2. Probar el algoritmo
      * Usar ejemplos pequeños para cada prueba
        * Hay que usar varios problemas:
          * Donde se conocen una o la solución (óptimo)
        * Verificar solución factible
      * Lista de propiedades deseadas o requeridas
        * Cuantitativa
          * Tiempo de ejecución
          * Uso de memoria
          * Cantidad de problemas resueltos
          * Complejidad
    * ## Ejemplo de paper
      * In this paper, we propose a ==new== sorting algorithm called Pancake sorting with a complexity of $$O(log n)$$. Moreover, our solution uses less memory than existing solutions. We provide a full set of experiments to validate our solution and a comparison with calims the state of the art.
      * Introduction
        * 1. What is the problem?
          * Sorting data + type of data
        * 2. Why is it interesting?
          * Several applications, DB, SC, DM, VG
          * Major concern in programing
        * 3. Why is it a difficult task?
          * Complexity  -> Feasibility for large (huge) problems
          * Example: LHC, ...
          * Memory use
        * 4. Example of sorting (small problem)
        * 5. Our solution
          * Design -> What is the key idea?
          * Give a global idea of how it works
          * What are the benefits of the solution
            * O(log n)
            * Memory -> how much?
            * Stability
        * 6. Constributions
          * New sorting algorithm
          * A low complexity of O(log n)
          * A low memory use
          * A stable algorithm
      * Formalización del problema
        * Let $$ A = {a_o, a_1, ..., a_n}$$ a set of $$n+1$$ elements, and $$B=f(A)$$ where $$f$$ is a sorting algorithm if exists $$\leq$$ and order relation between two elements of $$A$$ such that, if $$a_i \leq a_j $$ then $$a_i$$ is less or equal than $$a_j$$, then $$B=f(A)={a_0, a_1, a_i, ... a_j, a_n}$$ is sorted iff. $$\forall i \leq j, a_i, a_j \in B, a_i \leq a_j$$
        * $$ B = f(A) = F(A)$$
      * Solution
        * 1. What is the key idea?
          * Pancake idea
        * 2. Give details
          * Where to move the stack
            * How to choose the index for the pancake move
          * How de we implement the move?
            * What data structure is the most suited for this move
        * 3. Give the pseudocode of the algorithm
        * 4. Give the complexity
          * Without doing a theorical demostration
            * References to experiments sections
            * Properties
            * Memory use
            * Stability
      * Experiments
        * 1. Complexity
          * a) Theorical computation of the complexity (formal)
            * Using pseudocode
          * b) Benchmark
            * Severals problems with increasing values of N (50 instances)
            * Result: Curve like $$ax \log(N) +b)$$
        * 2. Memory use
          * Metric: Amount of KB used by the process during execution
            * Linux; getrusage() / Valgrind
          * Result:
            * Curve, Memory = f(N)
            * Table
        * 3. Stability
          * Metric of orden: Entropy
          * ```cant=0
     ex:
          for(i=0;i<n;i++)
               if(a[i]>a[i+1]) cant++; 
 ```
          * Check with benchmark if the entropy decreases when given a pre-sorted set
            * With various problems, with different sizes

      * Discussion
        * Compare the experiments results with the state of art.
          * Give a quantification (how much) why?
      * Conclusion
        * Give again the list of contribution plus benefits  the solution
        * What else?
  * ## Resultados
    * Es importante
      * Tablas
        * 1. No debe ser demasiado grande
        * 2. Unidades
          * Tiempo(s), numero de interaciones
          * Número de decimales
          * Número alineados a la derecha
          * Poner si un resultado es mejor y por cuanto más lo es (%)
      * Barras
      * Gráficos
        * No hay que poner más de 4 gráficos y siempre comentar el gráfico y ¿por qué?¿Y qué significa que sea así?. Si tengo algo cual es la ventaja
        * Cada problema debe tener el mismo número de secuencia.
        * Curvas
        * Dibujos
          * No tiene que ser muy cargado y hay que comentar el dibujo
          * Leyendas claras
      * Textos
      * Imagen/Foto
      * Video
      * Yed: pasa grafos a diagrama de flujo
      * gnumeric -> formato eps o pdf (no bitmap)
    * Cualitativas
      * Solución factible
      * Encontrar el ótimo
    * Para cada propiedad
      * ¿Cuáles son las pruebas que debemos hacer?
        * ¿Qué resultados me permiten concluir?
      * ==Hay que hacer una sola prueba a la vez==
        * Variar un solo parámetro
    * ¿Cuales son los resultados esperados?
      * Algunas propiedades se pueden demostrar de la manera formal y otras de manera practica
    * Complejidad -> O(log(n)) -> $$ ax \log(n) + b$$
      * user = t0, sys = t1, elapes t2
      * t = t0+t1
  * ## Ejemplo paper
    * Titulo: Pancake String: A new approach for fast sorting
    * Abstract: Sorting data is a well know problem that apper in several applications sush that databases, scientific computation or data mining. The complexity of a sorting algorithm is then a major concern to make it scalable, as well of the fait use of the avariable memory. In this context, designing a good sorting algorithm is a difficult task.
  * Organizar resultados
    * Resultados
      * Propiedad 1
        * Prueba 1
          * Resultado 1
        * Prueba 2
          * Resultado 2
        * ...
      * P2
      * P3
    * Automatizar las pruebas
    * + Resumen resultados
    * + Producción de grafos o curvas