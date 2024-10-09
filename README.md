## Titulo

Busqueda Semantia de Peliculas.

## Pre-requisitos 📋

* Para iniciar con la ejecución del siguiente proyecto deberás contar con lo siguiente
a) Equipo de cómputo con buenos recursos físicos ara correr los programas como minimo 12 en RAM y un buen procesador
b) Visual Estudio Code
c) Anaconda Navigator - Jupiter
d) Instalador de Git GUI
e) Repositorio código fuente de Keaggle






## Instalación 🔧

# Primer Paso 

    a) Primer paso instalar el entorno de visual estudio code o Jupyter atra ves de anaconda.https://www.anaconda.com/products/navigator
    b) Para el siguiente caso se utilizó Jupyter a traves de Anaconda Navigator el cual tiene embebidos diferentes ambientes de lenguaje de programación.
    c) Descargamos el repositorio de Keaggle a traves de la URL: https://www.kaggle.com/datasets/omarhanyy/imdb-top-1000?resource=download
    d) Se descarga el instalador de GIT a través de la URL: https://git-scm.com/ para luego subir los repositorios a Github
    e) Se procede a crear una cuenta de Gihub para luego subir los repositorios del proyecto.
    
![ANACONDA](https://github.com/user-attachments/assets/c27ef3f4-75b2-42f3-80bb-3acf095928d8)

# Importante y tener en cuenta

    a) Para poder Iniciar este proyecto es importante definir el entorno dono trabajaras.
    b) Instalar los programas adecuados de acuerdo lo requerido para poner en marcha el proyecto.
    c) Es importante tener todos los programas en el equipo de cómputo para realizar un buen trabajo. Sobre todo realizar las pruebas necesarias.

Ejemplo de cómo obtener datos del sistema o como usarlos

   a) Caso de bueno uso y practica para desarrollar el proyecto es importante utilizar las versiones de acuerdo a tu sistema operativo para no generar conflictos. Para caso particular se utilizaron versiones de 64 para la instalación de Git para subir los repositorios.

# Ejecucion de pruebas ⚙️

    a) Iniciamos en el Jupyer  y creamos una nueva carpeta con el nombre del proyecto  dentro del repositorio de Jupyter "Home" 
    b) Descargamos el repositorio del datase de Keaggle con el que se va trabajar. archivo "Pelis1000.cvs" para este paso le cambie el nombre al archivo .cvs
    c) Dentro de la misma carpeta creamos el notebook .ipynb y copiamos el archivo "Pelis1000.cvs"
    e) Creamos el notebok de Búsqueda dentro de la misma carpeta del proyecto Jupyter "Home"

#####JUPYTER####

# Instalando Dependencias Necesarias:

%%capture
%pip install -U sentence-transformers pandas

# Se importan la librerias necesarias:

import pandas as pd

# Se lee el datasep que esta dentro de la carpeta del proyecto y se miran los primerp eleentos del dataframe

df = pd.read_csv('Pelis1000.csv')
df.head()

# Muestre la información de los datos de cada Columna

df.info()

<class 'pandas.core.frame.DataFrame'>
RangeIndex: 1000 entries, 0 to 999
Data columns (total 10 columns):
 #   Column       Non-Null Count  Dtype  
---  ------       --------------  -----  
 0   Unnamed: 0   1000 non-null   int64  
 1   Title        1000 non-null   object 
 2   Certificate  973 non-null    object 
 3   Duration     1000 non-null   object 
 4   Genre        1000 non-null   object 
 5   Rate         1000 non-null   float64
 6   Metascore    712 non-null    float64
 7   Description  1000 non-null   object 
 8   Cast         1000 non-null   object 
 9   Info         1000 non-null   object 
dtypes: float64(2), int64(1), object(7)
memory usage: 78.3+ KB

# Muestre la información de las columnas categoricas
df.describe()

 	Unnamed: 0 	Rate 	Metascore
count 	1000.000000 	1000.000000 	712.000000
mean 	499.500000 	8.097500 	81.001404
std 	288.819436 	0.169566 	9.811801
min 	0.000000 	8.000000 	61.000000
25% 	249.750000 	8.000000 	73.000000
50% 	499.500000 	8.000000 	82.000000
75% 	749.250000 	8.100000 	88.250000
max 	999.000000 	9.300000 	100.000000


Con esta prueba de escritorio evidenciamos que se cargo bien el dataset ('Pelis1000.csv') y conocemos de la informacion.

# Muestre los tipos de datos que existen en las columnas
df.dtypes

Unnamed: 0       int64
Title           object
Certificate     object
Duration        object
Genre           object
Rate           float64
Metascore      float64
Description     object
Cast            object
Info            object
embeddings      object
dtype: object

# Analis de las pruebas 🔩

Se realiza una lectura; posteriormente que muestre del dataset con el fin de conocer la información que el archivo Pelis1000.cvs y su contenido para los cual ejecutaremos una pruebas de inicio, dentro de los cuales se analizaron los datos de las filas y columnas con el fin de realizar una búsqueda en particular de un tema específico, ejemplo de código :  

import pandas as pd

def main(query):
    df = pd.read_csv('./Pelis1000.csv')
    print(df.head())
    # TODO: Completar esta función para realizar búsquedas semánticas con base en el código del archivo test.ipynb



if __name__ == '__main__':
    query = input('ingresa el termino de busqueda')
    main(query)

Se realizo búsqueda de una película en particular "Matrix" pero en el caso hizo la búsqueda en los primeros 5 elementos del dataframe y no de los 1000 datos.

# Ejecucion de las librerias: 

Para la ejecución del código es necesario la instalacion de lo siguiente: 
#!pip install sentence-transformers y 
#from sentence_transformers import SentenceTransformer, util


## Construido con herraiemtas🛠️

las herramientas qutilzadas se podran consultar en las siguietes url:

* (https://www.anaconda.com/products/navigator/) - entorno de programacion.
* (https://www.kaggle.com/datasets/omarhanyy/imdb-top-1000?resource=download) - dataset
* (https://git-scm.com/) - Usado para generar RSS
* (https://github.com/dalquinones/semantic_search)


## Contribuyendo 🖇️

Por favor lee el [CONTRIBUTING.md]https://github.com/elvin854/Proyecto1.git 

## Autores ✒️

* **David Alejandro Quiñonez Mosqueraa** - *Trabajo Inicial
* **Elvin Torres Cervantes** - *Documentado

## Licencia 📄

Este proyecto está bajo la Licencia (Tu Licencia) - mira el archivo [LICENSE.md](LICENSE.md) para detalles

## Expresiones de Gratitud 🎁

* Comenta a otros sobre este proyecto 📢
* Interesante como subir los archivos de repositrios a este proyecto a traves de Git, primera experiencia en el tema y  fue de muchas expectativas para crear proyectos.
