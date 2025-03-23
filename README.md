# Artificial Immune Network Algorithm for the Multiple Sequence Alignment Problem of Alzheimer’s Disease Amyloid-Secretase-Pathway

Este proyecto implementa un **Algoritmo de Red Inmune Artificial (AiNet)** para resolver el **problema de alineación múltiple de secuencias (MSA)**, aplicado a la **vía amiloide-secretasa de la enfermedad de Alzheimer**. El objetivo es optimizar la alineación de secuencias genéticas, una tarea clave en bioinformática para el análisis de enfermedades genéticas como el Alzheimer.

## Descripción
El algoritmo de red inmune artificial aborda el problema MSA en el contexto de la investigación del Alzheimer. La implementación fue presentada en el **13th International Congress of Telematics and Computing (WITCOM 2024)**, celebrado en Mazatlán, México, del **4 al 8 de noviembre de 2024**.

## Contribución y Publicación
Este código fue desarrollado como proyecto de la materia *Seminario de Investigación* en colaboración con el **Dr. Ernesto Rios Willarx**.

**Detalles de la publicación:**  
- **Título:** *Artificial Immune Network Algorithm for the Multiple Sequence Alignment Problem of Alzheimer’s Disease Amyloid-Secretase-Pathway*  
- **Autores:** Ernesto Rios-Willars, María Magdalena Delabra-Salinas y Victor Cancino Herández  
- **Evento:** WITCOM 2024 (Springer)  
- **Enlace:** [Springer Link](https://link.springer.com/chapter/10.1007/978-3-031-77290-0_20)  

## Instalación

Para clonar el repositorio, ejecuta el siguiente comando en tu terminal:

```bash
git clone https://github.com/CancinoVictor/Artificial-Immune-Network-Algorithm.git
```

Este proyecto requiere tener **Python 3.x** instalado. Para instalar las dependencias necesarias, puedes usar `pip`:

```bash
pip install numpy
pip install blosum
```
## Uso
Para ejecutar el proyecto, simplemente corre el script principal `main.py` que implementa el algoritmo AiNet para resolver el problema de alineación múltiple de secuencias.

```bash
python main.py

```
## Explicación

### Archivos de entrada

El proyecto requiere archivos FASTA con secuencias de ADN. Asegúrate de que los siguientes archivos existan en el directorio de trabajo:

- **APP.FASTA**
- **MAPK3.FASTA**
- **PRKACA.FASTA**
- **PSEN2.FASTA**

Cada archivo debe contener una secuencia de ADN con el formato estándar de FASTA.

El script realiza las siguientes acciones:

- Lee las secuencias en formato FASTA.
- Crea una matriz de alineación de las secuencias.
- Aplica mutaciones y clona secuencias aleatorias.
- Evalúa la calidad de la alineación utilizando la matriz de puntuación BLOSUM62.
- Genera un reporte con la evolución de la población de secuencias a lo largo de las generaciones.

### Funciones Principales

- **leer_archivo_fasta(archivo):** Lee las secuencias en formato FASTA desde un archivo.
- **eliminar_columnas_con_guiones(matriz):** Elimina las columnas de la matriz que contienen solo guiones.
- **aplicar_mutacion_incremento(matriz, timer):** Aplica mutaciones aleatorias a las secuencias de la matriz.
- **calculaFitness(matriz_mutada):** Calcula la puntuación de la alineación utilizando la matriz de puntuación BLOSUM62.
- **calcular_puntuacion_blosum62(columna):** Calcula la puntuación de una columna utilizando la matriz de sustitución BLOSUM62.
- **generaReporte(nCorrida, generacion, popSize, puntos, fitnessProm, NFE, tfinal):** Genera un reporte CSV sobre la evolución de la población.

### Parámetros configurables

- **pobSize:** Tamaño de la población inicial.
- **clonRate:** Tasa de clonación, que define cuántos clones se generarán en cada ciclo.
- **threshold:** Valor de corte para eliminar individuos con puntuaciones bajas.
- **cycles:** Número de ciclos (generaciones) que se ejecutará el algoritmo.
- **maxPob:** Tamaño máximo de la población después de la reducción.
- **nClones:** Número de clones que se generarán en cada ciclo.
- **rClonInsert:** Tasa de inserción de clones aleatorios en la población.

## Salida esperada
Al ejecutar el script se generará:


✅ alignment_report.csv -> Evolución de las generaciones.  
✅ optimized_alignment.txt -> Mejor alineación encontrada.  

## Licencia

Este proyecto está bajo la Licencia MIT. Consulta el archivo LICENSE para más detalles.


