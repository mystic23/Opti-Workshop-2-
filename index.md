
# **Matrices Dispersas**

## **Definición**
- Matrices donde la mayoría de sus elementos son ceros

## **Caracteristicas**
- ==**Ahorro de Memoria**== Solo se guardan los valores no cero
- ==**Eficiencia**== Uso de memoria depende
 del número de valores no cero
- ==**El patrón de dispersión**== (distribución de los valores no cero)
 afecta la eficiencia de ciertos formatos

## **Aplicaciones**
- Resolución de sistemas de ecuaciones lineales
- Procesamiento de Imágenes
- Minado de Datos
- Sistemas de Recomendación
- Redes Neuronales


<!-- - **Limitaciones** 

    - Calidad de aproximación
    - Precisión de la solución -->

<!-- ## Problemas con la Escasez
- Complejidad Espacial
  - Memoria alta para valores cero
- Complejidad Temporal
  - Operaciones ineficientes en matrices grandes -->

## **Caractateristicas de formato (Arreglos)**   

- **CSR**
    - **Ventajas**  
        - Rápido para acceder a 
    elementos en una fila específica
    - **Desventajas** 
        - Cortar columnas es lento
- **CSC**
    - **Ventajas**
        - Rápido para acceder a elementos
         en una columna específica
    - **Desventajas** 
        - Cortar filas es lento
 - **COO**
    - **Ventajas**
        - Bueno para construir y modificar matrices
    - **Desventajas** 
        - Menos eficiente para acceso rápido
         y operaciones aritméticas


## **Formatos**
- **Listas Enlazadas**
    - Simples
        - Cada nodo representa una celda no nula
        - Contiene valor, columna y referencia al siguiente nodo
    - Por Filas
        - Cada fila es una lista enlazada separada
        - Cada nodo en la lista representa una 
        celda no nula con valor y columna
        
**Arreglos**
- Fila Dispersa Comprimida **(CSR)**
    - **Almacena los elementos no nulos por filas usando tres arreglos:**
      valores, índices de columna y punteros a filas
    - **Ejemplo** <img src="https://docs.nvidia.com/nvpl/_static/sparse/_images/csr.png" alt="CSR" width="200" height="100"/>
- Columna Dispersa Comprimida **(CSC)**
    - Almacena los elementos no nulos por columnas usando tres arreglos:
      valores, índices de fila y punteros a columnas
    - **Ejemplo** <img src="https://docs.nvidia.com/nvpl/_static/sparse/_images/csc.png" alt="CSC" width="200" height="100"/>
- Lista de Coordenadas **(COO)**
    - Almacena elementos no nulos como tuplas de índices de fila, columna y valor
    - **Ejemplo** <img src="https://docs.nvidia.com/nvpl/_static/sparse/_images/coo.png" alt="COO" width="200" height="100"/>

