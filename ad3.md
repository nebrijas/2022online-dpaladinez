# Actividad 3

Esta es la actividad dirigida 3 que consiste en hacer un ejercicio de programación literaria, aprovechando el código que hemos usado en programación con Python donde realizamos web scraping.

[ad3.ipynb](docs/ad4.ipynb)

A continuación pongo el código fuente.

## Código fuente

```
import requests
import time
import csv
import re
from bs4 import BeautifulSoup
import os
import pandas as pd
from termcolor import colored
 
resultados = []
 
req = requests.get("https://resultados.elpais.com")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup = BeautifulSoup(req.text, 'html.parser')
 
tags = soup.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req2 = requests.get("https://elpais.com/internacional")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup2 = BeautifulSoup(req2.text, 'html.parser')
 
tags = soup2.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req3 = requests.get("https://elpais.com/opinion")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup3 = BeautifulSoup(req3.text, 'html.parser')
 
tags = soup3.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req4 = requests.get("https://elpais.com/espana/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup4 = BeautifulSoup(req4.text, 'html.parser')
 
tags = soup4.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req5 = requests.get("https://elpais.com/economia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup5 = BeautifulSoup(req5.text, 'html.parser')
 
tags = soup5.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req6 = requests.get("https://elpais.com/sociedad/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup6 = BeautifulSoup(req6.text, 'html.parser')
 
tags = soup6.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req7 = requests.get("https://elpais.com/educacion/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup7 = BeautifulSoup(req7.text, 'html.parser')
 
tags = soup7.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req8 = requests.get("https://elpais.com/clima-y-medio-ambiente/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup8 = BeautifulSoup(req8.text, 'html.parser')
 
tags = soup8.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req9 = requests.get("https://elpais.com/ciencia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup9 = BeautifulSoup(req9.text, 'html.parser')
 
tags = soup9.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req10 = requests.get("https://elpais.com/cultura/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup10 = BeautifulSoup(req10.text, 'html.parser')
 
tags = soup10.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req11 = requests.get("https://elpais.com/babelia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup11 = BeautifulSoup(req11.text, 'html.parser')
 
tags = soup11.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req12 = requests.get("https://elpais.com/deportes/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup12 = BeautifulSoup(req12.text, 'html.parser')
 
tags = soup12.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req13 = requests.get("https://elpais.com/tecnologia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup13 = BeautifulSoup(req13.text, 'html.parser')
 
tags = soup13.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req14 = requests.get("https://elpais.com/tecnologia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup14 = BeautifulSoup(req14.text, 'html.parser')
 
tags = soup14.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req15 = requests.get("https://elpais.com/gente/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup15 = BeautifulSoup(req15.text, 'html.parser')
 
tags = soup15.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req16 = requests.get("https://elpais.com/television/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup16 = BeautifulSoup(req16.text, 'html.parser')
 
tags = soup16.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req17 = requests.get("https://elpais.com/eps/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup17 = BeautifulSoup(req17.text, 'html.parser')
 
tags = soup17.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
 
os.system("clear")
 
print(colored("A continuación se muestran los titulares de las páginas principales del diario El País que contienen las siguientes palabras:", 'blue', attrs=['bold']))
print(colored("Feminismo", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "feminismo" in s]
print("\n".join(str_match))
 
print(colored("Igualdad", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "igualdad" in s]
print("\n".join(str_match))
 
print(colored("Mujeres", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "mujeres" in s]
print("\n".join(str_match))
 
print(colored("Mujer", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "mujer" in s]
print("\n".join(str_match))
 
print(colored("Brecha salarial", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "brecha salarial" in s]
print("\n".join(str_match))
 
print(colored("Machismo", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "machismo" in s]
print("\n".join(str_match))
 
print(colored("Violencia", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "violencia" in s]
print("\n".join(str_match))
 
print(colored("Maltrato", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "maltrato" in s]
print("\n".join(str_match))
 
print(colored("Homicidio", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "homicidio" in s]
print("\n".join(str_match))
 
print(colored("Género", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "género" in s]
print("\n".join(str_match))
 
print(colored("Asesinato", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "asesinato" in s]
print("\n".join(str_match))
 
print(colored("Sexo", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "sexo" in s]
print("\n".join(str_match))
```

## Programación Literaria

Las librerías son un conjunto de funciones que permite llevar a cabo nuevas tareas 

### Librerías

#### Librerías internas

- [csv](https://docs.python.org/3/library/csv.html): de *comma separated values* o Valores Separados por Comas es el formato muy habitual importación y exportación de hojas de cálculo y bases de datos.
- [re](https://docs.python.org/3/library/re.html):Este módulo proporciona operaciones de coincidencia de expresiones regulares similares a las encontradas en Perl.
- [time](https://docs.python.org/es/3/library/time.html):Este módulo proporciona varias funciones relacionadas con el tiempo. Para la funcionalidad relacionada, consulte también los módulos datetime y calendar.
- [os](https://docs.python.org/3/library/os.html):Este módulo provee una manera versátil de usar funcionalidades dependientes del sistema operativo. 

#### Librerías externas 

- [requests](https://cosasdedevs.com/posts/web-scraping-con-requests-y-beautifulsoup-en-python/): e usa para hacer solicitudes y peticiones a la página de la que extraeremos datos.
- [bs4](https://es.acervolima.com/python-beautifulsoup-encontrar-todas-las-clases/):Beautiful Soup (bs4) es una biblioteca de la cual podemos obtener datos en formato HTML y XML.
- [Pandas](https://pypi.org/project/pandas/): Es una herramienta de análisis de datos de código, de lectura rápida en el lenguaje de programación de Python.
- [termcolor](https://pypi.org/project/termcolor/): Es una biblioteca que sirve para imprimir mensajes de colores en el terminal.

## Instalación librerías

La funcion `pip` es una forma simple de instalar una librería

Al insertar ` pip install requests bs4 pandas termcolor` le estamos pidiendo mediante el lenguaje Python que importe la librería de bs4, Pandas y termcolor


```python
pip install requests bs4 pandas termcolor
```

    Requirement already satisfied: requests in c:\users\gabri\anaconda3\lib\site-packages (2.28.1)
    Requirement already satisfied: bs4 in c:\users\gabri\anaconda3\lib\site-packages (0.0.1)
    Requirement already satisfied: pandas in c:\users\gabri\anaconda3\lib\site-packages (1.4.4)
    Requirement already satisfied: termcolor in c:\users\gabri\anaconda3\lib\site-packages (2.1.1)
    Requirement already satisfied: certifi>=2017.4.17 in c:\users\gabri\anaconda3\lib\site-packages (from requests) (2022.9.14)
    Requirement already satisfied: charset-normalizer<3,>=2 in c:\users\gabri\anaconda3\lib\site-packages (from requests) (2.0.4)
    Requirement already satisfied: urllib3<1.27,>=1.21.1 in c:\users\gabri\anaconda3\lib\site-packages (from requests) (1.26.11)
    Requirement already satisfied: idna<4,>=2.5 in c:\users\gabri\anaconda3\lib\site-packages (from requests) (3.3)
    Requirement already satisfied: beautifulsoup4 in c:\users\gabri\anaconda3\lib\site-packages (from bs4) (4.11.1)
    Requirement already satisfied: numpy>=1.18.5 in c:\users\gabri\anaconda3\lib\site-packages (from pandas) (1.21.5)
    Requirement already satisfied: python-dateutil>=2.8.1 in c:\users\gabri\anaconda3\lib\site-packages (from pandas) (2.8.2)
    Requirement already satisfied: pytz>=2020.1 in c:\users\gabri\anaconda3\lib\site-packages (from pandas) (2022.1)
    Requirement already satisfied: six>=1.5 in c:\users\gabri\anaconda3\lib\site-packages (from python-dateutil>=2.8.1->pandas) (1.16.0)
    Requirement already satisfied: soupsieve>1.2 in c:\users\gabri\anaconda3\lib\site-packages (from beautifulsoup4->bs4) (2.3.1)
    Note: you may need to restart the kernel to use updated packages.
    

El primer paso que se debe aplicar para la ejecución de este código es importar la librería necesaria para el guion. Las mostramos a continuación:


```python
import requests
import time
import csv
import re
from bs4 import BeautifulSoup
import os
import pandas as pd
from termcolor import colored 
```

Luego se debe colocar la variable llamada **resultado**, la cual es un objeto de tipo lista


```python
resultados = []
```

El paso siguiente es solicitar los datos de los titulares del **El PAÍS**

## Interpretación de resultados a través de las urls

Se realiza una petición `HTTP GET` a la url de la web. Esta petición devuelve la variable `req`.

`req`Es la abreviación de requests.get.
`requests` es peticiones
`get`es obtener
por lo que la variable significa dame la página de El País 


```python
req = requests.get("https://resultados.elpais.com")
```

`req` es una variable de tipo `requests.models.Response`

Luego se utiliza el atributo `status_code` para comprobar la petición. Si el valor es igual a 200, la petición se ha realizado con éxito


```python
if (req.status_code != 200):
    raise Exception("No se puede hacer Web Scraping en"+ URL)
```

Se interpreta todo el texto HTML de la página web con ayuda de una de las funciones de la librería bs4: `BeautifulSoup.` Este paso se realiza cuando secomprueba que la petición ha sido exitosa.


```python
soup = BeautifulSoup(req.text, 'html.parser')
```

Es necesario el texto de las etiquetas, para eso se utiliza una de las funciones de soup llamada `findAll.` Con esta función solo se almacenan en la variable tags el texto de los titulares de la web.


```python
tags = soup.findAll("h2")
```

En la variable tags se almacena todos los titulares obtenidos.

Se recorren con una sentencia for y se añaden al final en cada iteración.


```python
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
```

Este procedimiento se repite el número de veces

Ejemplo:


```python
req2 = requests.get("https://elpais.com/internacional")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup2 = BeautifulSoup(req2.text, 'html.parser')

tags = soup2.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req3 = requests.get("https://elpais.com/opinion")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup3 = BeautifulSoup(req3.text, 'html.parser')

tags = soup3.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req4 = requests.get("https://elpais.com/espana/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup4 = BeautifulSoup(req4.text, 'html.parser')

tags = soup4.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req5 = requests.get("https://elpais.com/economia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup5 = BeautifulSoup(req5.text, 'html.parser')

tags = soup5.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req6 = requests.get("https://elpais.com/sociedad/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup6 = BeautifulSoup(req6.text, 'html.parser')

tags = soup6.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req7 = requests.get("https://elpais.com/educacion/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup7 = BeautifulSoup(req7.text, 'html.parser')

tags = soup7.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req8 = requests.get("https://elpais.com/clima-y-medio-ambiente/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup8 = BeautifulSoup(req8.text, 'html.parser')

tags = soup8.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req9 = requests.get("https://elpais.com/ciencia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup9 = BeautifulSoup(req9.text, 'html.parser')

tags = soup9.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req10 = requests.get("https://elpais.com/cultura/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup10 = BeautifulSoup(req10.text, 'html.parser')

tags = soup10.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req11 = requests.get("https://elpais.com/babelia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup11 = BeautifulSoup(req11.text, 'html.parser')

tags = soup11.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req12 = requests.get("https://elpais.com/deportes/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup12 = BeautifulSoup(req12.text, 'html.parser')

tags = soup12.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req13 = requests.get("https://elpais.com/tecnologia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup13 = BeautifulSoup(req13.text, 'html.parser')

tags = soup13.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req14 = requests.get("https://elpais.com/tecnologia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup14 = BeautifulSoup(req14.text, 'html.parser')

tags = soup14.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req15 = requests.get("https://elpais.com/gente/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup15 = BeautifulSoup(req15.text, 'html.parser')

tags = soup15.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req16 = requests.get("https://elpais.com/television/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup16 = BeautifulSoup(req16.text, 'html.parser')

tags = soup16.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req17 = requests.get("https://elpais.com/eps/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup17 = BeautifulSoup(req17.text, 'html.parser')

tags = soup17.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
```

    Rusia cancela el primer encuentro previsto con EE UU desde el inicio de la guerra de Ucrania 
    China responde a las protestas con un fuerte despliegue de seguridad en Pekín y Shanghái
    Hartazgo, estragos económicos y accidentes mortales: claves para entender las protestas en China
    China: una protesta nacional
    Publicar no es un delito
    La vida bajo los bombardeos rusos
    Democracias a la defensiva
    La UE vista desde el G-20 de Bali 
    Las protestas se extienden en China contra la política de covid cero
    La OTAN acusa a Putin de usar el invierno como arma de guerra contra Ucrania
    El último iPhone, perfumes de Chanel o un Rolex: las marcas occidentales llenan los escaparates rusos pese a las sanciones
    China y Estados Unidos, condenadas a entenderse y a rivalizar
    Lecciones en Ucrania para ser reportero de guerra: explosiones de fogueo, torniquetes y campos de minas
    De la manifestación al patíbulo: el régimen iraní amenaza con la horca para sofocar las protestas
    Publicar no es un delito
    Los medios de los cables de WikiLeaks piden a EE UU que no persiga a Assange
    López Obrador saca músculo y marca el camino a los candidatos presidenciales de su partido
    Las autoridades elevan a ocho los muertos por el corrimiento de tierra en la isla italiana de Ischia
    La gestión del frío enfrenta a Zelenski y al alcalde de Kiev
    China y Estados Unidos, condenadas a entenderse y a rivalizar
    Bolsonaro reaparece en una ceremonia militar tras batallar su derrota desde la trastienda
    Justin Trudeau justifica el uso de la Ley de emergencia para desalojar a los camioneros antivacunas
    La nota del autor de la matanza del Walmart de Virginia: “Se reían de mí y decían que era un asesino en serie”
    La pobreza se ceba con los menores de 18 años en América Latina
    Sánchez al frente de la Internacional Socialista 
    La UE y la inmigración
    Publicar no es un delito
    Delitos contra la Constitución: rebelión y sedición 
    ‘A compás’
    La tertuliana de ultraderecha y el bulo tránsfobo contra Begoña Gómez, la mujer de Pedro Sánchez
    Lengua migrante 
    Autonomía estratégica: cómo se consigue
    Salud e ideología
    La caverna
    Alberto Núñez Feijóo, nacionalista
    Venezuela, que algo queda
    Violencia sexual 
    El acoso invernal de Putin 
    Los desposeídos
    El Roto
    Flavita Banana
    Riki Blanco
    Peridis
    Sciammarella
    Envía tu carta
    El desprestigio de la sanidad pública va calando
    Lucha feminista no solo en días mundiales
    Gamberros ilustrados
    Noticias positivas en tiempos caóticos
    Bomba nuclear en Barcelona
    Una maldita lista en tiempos airados
    El defensor del lector contesta
    La ‘ley trans’ enturbia el plan socialista para despejar de conflictos la campaña electoral de 2023
    El Constitucional aparca desde junio fallos clave por el bloqueo del PP en el Poder Judicial
    Hallan muertos a dos barranquistas atrapados por la lluvia en un torrente de Mallorca 
    Alberto Núñez Feijóo, nacionalista
    La caverna
    Aunque nos tiemble la barbilla
    Orfandad representativa
    Otra forma de violencia política
    El actor Luis Lorenzo en el ‘papelón’ de su vida: “Mi Oscar va a ser que se reconozca mi inocencia”
    Pedro Sánchez: “Una de las cosas por las que pasaré a la historia es por haber exhumado al dictador”
    El empresario Cursach quedará absuelto al retirarse la última acusación mantenida contra él
    La presidenta del Consejo de Estado discrepa de la “descalificación global” por parte de la ministra Montero del “machismo” de algunos jueces
    La Audiencia de Cádiz exculpa a los miembros del clan de Los Castaña del delito de pertenencia a organización criminal
    El Supremo dicta desde 2010 sentencias desiguales sobre revisiones de penas  
    Qué hay de cierto y qué no sobre una supuesta ola de frío en España
    ETA siempre vuelve cuando el PP vislumbra éxito electoral
    Las provocaciones de los ultras desbordan el vaso en el Congreso
    Tres años de exabruptos de Vox en el Congreso de los Diputados
    Memoria pétrea del franquismo 
    Hay casi 4.000 cervezas artesanas españolas. ¿Cómo probarlas todas?
    El cambio hacia un consumo sostenible empieza por los pies
    Escrivá plantea subir a 30 años el periodo de cálculo de la pensión descartando los dos peores 
    Lagarde cree que la inflación aún no ha tocado techo y seguirá subiendo los tipos de interés
    Calendario laboral 2022-2023: qué días son festivos y cuáles no en el último puente del año
    Se acabó el “modo avión”: por fin se podrá hablar por el móvil en los vuelos
    Sufrimientos evitables
    El coste de la vida
    La intermediación del ahorro y su evolución
    La Europa ganadora que necesitamos
    Ecos de una goleada histórica (en la patronal)
    Las Bolsas mundiales registran pérdidas tras las protestas en China
    La firma de criptomonedas BlockFi suspende pagos arrastrada por la caída de FTX
    Skoda aspira a lograr una cuota del 5% en España en 2028
    Las insolvencias en España aumentarán un 20% este año, según los Economistas
    La banca confía en tumbar en los tribunales el nuevo impuesto al sector
    El largo invierno nuclear francés
    Las redes agitan el debate sobre un nuevo producto de Mercadona: huevos a la plancha envasados
    Garamendi, la frialdad del ganador total
    Operación triunfo para directivos: así son las pruebas para entrar en el club de jefes más selecto del mundo
    Estos son los oportunistas fiscales en Europa
    Sufrimientos evitables
    Madrid, la nueva Miami: así se han hecho con la capital los ricos latinoamericanos
    Si no tiene ahorros, esta es una de las pocas alternativas para comprar casa
    Los efectos de una economía de andar por casa
    Caballos al galope: un negocio con un impacto económico de 7.400 millones de euros
    Los impuestos que se necesitan para construir la sociedad del futuro
    La vida de Pablo Isla tras Inditex: ocupa ocho cargos y alimenta su pasión por el cine
    Las grandes petroleras y gasísticas proponen al Gobierno ofrecer la TUR
    BBVA incorpora las ayudas hipotecarias a sus riesgos y abre la veda en toda la banca
    La inclusión, en el centro de la economía circular
    Por primera vez un juez declara nulo un contrato de alquiler por aplicación de la perspectiva de género
    Visitas a centros de acogida y muchas horas de estudio: así se forman los jueces en materia de género
    La justicia obliga a Iberia a controlar el peso de las maletas para que los azafatos no se lesionen
    La difícil tarea de recuperar el talento investigador que un día hizo las maletas
    Descubre las formaciones de marketing ‘online’ más buscadas (y económicas) de 2023
    La quinta edición de EnlightED aborda los retos del aprendizaje y la educación en la era digital  
    Logística de ida y vuelta, cuando la solución está en reciclar menos y reutilizar más
    Logística y digitalización, el manual de supervivencia para pymes
    Empleados satisfechos, empresas de éxito
    Diez claves del bienestar corporativo para empresas de éxito
    Las aventuras de un par de calcetines que dan empleo a todo un pueblo
    Cultura financiera como punto de partida para volver a empezar
    Las soluciones digitales que necesita mi negocio 
    Las fórmulas de financiación más adecuadas para mi negocio
    Alexia Putellas, un Balón de Oro a base de “esfuerzo, constancia, disciplina y saber reinventarse”
    El método Muñoz para triunfar en cada reto que se propone
    ¿Por qué muchos inversores están volviendo a confiar en Japón?
    ¿Por qué se está enfriando la economía china?
    Si tú lo imaginas, yo te lo imprimo
    Por qué tu casa puede ser tu radiografía además de tu biografía
    Cómo garantizar la seguridad en un mundo de amenazas híbridas
    ¿Cuáles son los dilemas éticos del uso de la inteligencia artificial?
    Cómo conseguir ayudas a la digitalización para autónomos y pymes con Kit Digital
    Un brindis con vino español por la sostenibilidad, la economía y el empleo
    Igualdad negocia a contra reloj con Interior y Justicia el texto de la ley de trata que irá mañana a Consejo de Ministros 
    La expulsión de una clase en un colegio de Palma tras colocar una bandera de España deriva en graves amenazas a una profesora 
    Los médicos privados se sienten “humillados” por las aseguradoras: los técnicos cobran 60 euros por arreglar una lavadora y los sanitarios, 10 por consulta
    La caja de resonancia de la angustia vital
    Para acabar con la violencia de género, necesitamos más mujeres en posiciones de poder 
    Los secretos atronadores del secretario general
    Balance de la COP27: un fondo para los más vulnerables mientras la meta de los 1,5 grados se aleja
    Los ayuntamientos de Madrid se sitúan un año más a la cola en servicios sociales
    Kelley Robinson: “Han declarado una guerra cultural contra nuestros hijos”
    La caja de resonancia de la angustia vital
    El teléfono, el gran aliado contra el suicidio
    La diócesis de Alicante y los maristas no aclaran el encubrimiento de un cura pederasta durante 35 años 
    La ley de familias da a los trabajadores hasta nueve días remunerados al año para atender urgencias y cuidados de familiares enfermos
    ¿Protege más a las mujeres elevar las penas?
    El Vaticano lamenta “con sorpresa y pesar” que China nombre a un obispo 
    La cuarta dosis de la vacuna contra la covid se estanca: menos de la mitad de los mayores de 60 la ha recibido
    Gobierno y Junta chocan por Doñana mientras se agrava el deterioro ecológico 
    El feminismo se fractura en Madrid en las protestas contra la violencia machista que recorren España
    Unas gafas que cambian la forma de ver el mundo
    Cambia tu relación con los papeles de la cocina
    Enfermería, los profesionales de las ‘curas invisibles’ en las personas con VIH
    Las ciudades marcan el objetivo: acabar con el VIH en 2030
    La huella de carbono, el rastro que marca el futuro del planeta
    El club de la eficiencia energética 
    Psoriasis, en las profundidades de la piel
    Contar para sanar
    La nueva revolución agrícola 
    Nuevos talentos de la economía circular
    Lo lejos que se puede llegar con otra metodología educativa 
    Cuando el empleo se convierte en la mejor terapia 
    A solas con la obesidad
    Freno y marcha atrás en la obesidad infantil
    ¿Hasta dónde puede llegar el ser humano? El viaje a la oscuridad más absoluta
    El viaje a uno de los paraísos más bellos de España. Por qué este paisaje cuelga de las paredes de medio mundo
    Acuicultura: la importancia de comer ‘azul’ para vivir en verde
    El cultivo de pescado español, a la vanguardia del planeta
    El futuro de la aviación verde
    En busca de la eficiencia energética en los aeropuertos
    Un día en el servicio de ayuda a domicilio
    Trabajadores esenciales. Los que nunca paran
    Consejos para alimentar correctamente a los animales de compañía
    Cuidados y necesidades de perros y gatos en su etapa sénior
    Combatir el desperdicio alimentario desde la cesta de la compra
    Kilómetro cero para llenar la despensa
    Acompañamiento, el modelo alternativo de acogida de refugiados
    El metro como refugio. De los andenes de Madrid en 1936 a los de Kiev en 2022
    Yogures con menos azúcar, paso firme hacia la alimentación infantil del futuro
    Invisible, pero vital: el ciclo de las aguas subterráneas
    La bomba de calor, el sistema de climatización más sostenible y eficiente
    El Gobierno dará un subsidio de 400 euros anuales a los alumnos con necesidades especiales
    La expulsión de una clase en un colegio de Palma tras colocar una bandera de España deriva en graves amenazas a una profesora 
    Pobreza en el Olimpo académico de EE UU: la huelga en la Universidad de California es ya una de las más grandes del país
    El primer Mundial en horario lectivo y con ‘smartphones’ se juega también en los institutos
    El cabecilla de los cánticos machistas del Elías Ahuja vuelve al colegio mayor pese a anunciarse su expulsión definitiva
    La nueva ley de enseñanzas artísticas endurecerá los requisitos para ser profesor y hará más homogéneas las pruebas de acceso del alumnado
    Una madre denuncia insultos homófobos a su hija en un colegio de Madrid: “Su tutor nos dijo que tenemos que respetar la opinión de los demás”
    Cataluña aprueba un complemento para ampliar la jornada a los profesores de informática de FP
    Más de 6.000 estudiantes de FP empezaron tarde el curso por el largo proceso de inscripción en Cataluña
    Cuando la escuela se convierte en un gueto: América Latina tiene las primarias más segregadas del mundo
    Ay, Lomloe
    Evaluar competencias
    La Selectividad a los 50: ¿cirugía mayor o estiramiento facial?
    La libertad de elección de centro educativo y los cheques escolares en Madrid
    Selectividad: Desatar el nudo gordiano
    El nuevo sistema para evaluar los conocimientos digitales de los profesores valdrá en toda España
    Ofrecer comedor gratis en todos los colegios públicos es “alcanzable y urgente”: costaría 1.664 millones al año, según la ONG Educo  
    Una fórmula para que la escuela pública compita mejor con la concertada
    La pérdida de alumnos por el descenso de la natalidad está afectando con más fuerza a la escuela pública que a la concertada
    La disparidad de resultados entre autonomías en la EVAU se origina en la escuela, no en el examen 
    Las autonomías del PP critican la nueva Selectividad porque no prevé un examen único para todo el Estado
    La escalada vertiginosa de notas en Bachillerato: los sobresalientes de los que llegan a Selectividad se doblan en seis años
    El caso de Georgia, en EE UU: becar sin importar la renta agranda la desigualdad
    El techo de cristal del grado medio de FP: candidatos demasiado preparados se quedan con los puestos
    César Rendueles: “Hay universidades privadas que son como academias de conducir con pretensiones”
    La fuga de miles de médicos agrava el déficit de especialistas en España
    Jóvenes tutelados en la Universidad: “Tu pasado no tiene por qué condicionar tu futuro”
    Si tu familia está desahogada estudiarás Medicina y dobles grados, si no, Óptica o Educación 
    Volver a empezar
    Borges, 'Funes el memorioso' y la neurona Jennifer Aniston
    ¿Contra qué se rebela la lectura?
    Gobierno y Junta chocan por Doñana mientras se agrava el deterioro ecológico 
    Linces y águilas imperiales se refugian en fincas privadas que se alían con conservacionistas  
    ¿Podré matar a una rata que entre en mi casa? Claves de la reforma del Código Penal para castigar más el maltrato animal
    El precio del Ave Madrid-Barcelona cae un 43% pero sube un 14% en las líneas sin competencia 
    El plan del Gobierno para las reservas de agua mantiene intacta la alta presión del regadío
    Operación ‘OS35’: cómo rescatar un gigante de 40.288 toneladas varado a la sombra de Gibraltar
    Balance de la COP27: un fondo para los más vulnerables mientras la meta de los 1,5 grados se aleja
    Clemente Álvarez, premio a la conservación de la biodiversidad de la Fundación BBVA: “Debemos difundir la voz de alarma de los científicos”
    Investigan la brutalidad en una montería en la Sierra de Segura de Jaén 
    La pandemia y los carriles bici impulsan que cada vez más españoles pedaleen por las ciudades 
    España sigue anclada en la sequía a pesar de las lluvias: así es el mapa desigual del agua y las restricciones
    El cambio climático perjudica su salud
    Por qué comer animales puede ayudar a luchar contra el cambio climático
    Por qué hay que dejar de comer animales para luchar contra el cambio climático
    Bombas de carbono 
    Crisis de los insectos: esto no es un armagedón sino una debacle provocada por los humanos
    El quebrantahuesos reconquista los cielos 
    Un año de crisis climática sin fin
    Ríos imposibles: las 171.000 barreras que rompen el curso de agua en España
    Volver a empezar
    Borges, 'Funes el memorioso' y la neurona Jennifer Aniston
    ¿Contra qué se rebela la lectura?
    “Houston, tenemos un nuevo récord”: ‘Orion’ llega más lejos que ninguna otra nave diseñada para llevar astronautas
    Un parásito ‘elige’ qué lobo será el líder de la manada
    Pobreza en el Olimpo académico de EE UU: la huelga en la Universidad de California es ya una de las más grandes del país
    Josefa Ros Velasco, filósofa: “Si alguien se aburre suele darse a la botella, cuando le pasa a un país suele darse una revuelta”
    La insólita historia de la mujer que descubrió el primer antibiótico español
    Hilda Hudson, la primera conferenciante en el gran congreso internacional de matemáticas
    De León al espacio, pasando por una pequeña universidad pública: “Invirtiendo en ciencia se puede llegar a lo más alto”
    “Soñamos con ir a la Luna, pero no llegaremos a Marte” 
    Pablo Álvarez y Sara García, primeros astronautas españoles de la ESA en 30 años
    Una vacuna universal contra la gripe que usa la tecnología de ARN, probada con éxito en ratones
    Palabras y árboles
    Europa resucita su misión para taladrar Marte en busca de vida en 2028  
    El aroma de la inspiración y la piedra de la locura
    ¿Por qué son rocosos los satélites de los planetas gaseosos?
    ¿Cómo nos afecta en la Tierra la formación de un agujero negro?: tres grandes físicos lo desvelan
    Los límites de la terapia hormonal de la menopausia: no se recomienda para prevenir enfermedades, pero sí para tratar sofocos severos
    ¿Cómo nos afecta en la Tierra la formación de un agujero negro?: tres grandes físicos lo desvelan
    Hilda Hudson, la primera conferenciante en el gran congreso internacional de matemáticas
    Por qué el entrelazamiento cuántico revoluciona nuestro entendimiento de la naturaleza
    La órbita del telescopio ‘James Webb’ y el problema de los tres cuerpos
    Cien años de las ecuaciones que expandieron el universo
    Sangaku
    El tamiz de Apolonio
    La respuesta a la gran pregunta
    El aroma de la inspiración y la piedra de la locura
    ‘Los hijos de Hansen’ y la marginación social provocada por la lepra
    Los fractales y su estructura narrativa como parte del relato
    El amanecer de todo y el dinosaurio como animal modernista
    Los universos paralelos de un visionario científico llamado Philip K. Dick
    ¿Por qué son rocosos los satélites de los planetas gaseosos?
    ¿Es nueva la producción de alimentos en macrogranjas? 
    ¿Cómo se ve el cielo nocturno desde el ecuador?
    ¿Por qué las olas van siempre hacia la playa?
    Listeria: el patógeno que trae de cabeza a la industria alimentaria
    Ciencia para derrumbar el mito de que la soja es mala para prevenir el cáncer de mama
    Cuidado con las conservas caseras: es importante hacerlas bien
    Una propuesta alternativa, barata y saludable a la nueva cesta de la compra
    Aditivos, propiedades saludables y fechas de caducidad: guía para entender las etiquetas alimentarias
    Bono se desnuda emocionalmente en Madrid en su concierto más atípico
    La encrucijada del Reina Sofía: ¿quién sucederá a Borja-Villel en la dirección de uno de los museos más importantes del mundo?
    Así era el rostro de san Isidro Labrador, muerto hace diez siglos   
    ‘Company’ y el olor de la gran manzana
    Charlie Watts: el bicho más raro de The Rolling Stones
    Meter la mano en la vaca 
    El hombre alegría
    La cultura abraza las historias trans 
    Momias a dos velas: la excavación estrella de la egiptología española afronta una crítica falta de fondos en su momento más decisivo
    El monasterio burgalés que falsificó en el siglo XII una herencia para quedarse con una valiosa iglesia
    La FIL pone una vela al libro y otra al balón
    Videoanálisis | La FIL mastodóntica y popular está de vuelta
    Carmen Machi: “Que te metieran mano en el metro nos parecía normal”
    Cómic y energía nuclear: el superventas francés que sacude el debate sobre el cambio climático
    ‘Argentina, 1985’, un debate nacional entre la ficción y la memoria
    Muere Irene Cara, actriz y cantante de ‘Fama’ y ‘Flashdance’, a los 63 años
    La Mano de Irulegi, más incógnitas que respuestas sobre el origen del euskera
    El periplo bajo las bombas de medio centenar de cuadros de artistas ucranios hasta llegar al Museo Thyssen de Madrid
    Otras mujeres
    Hermosa Márcia: el valor inquebrantable de una madre brasileña
    Santo Estevo, el monasterio al que todos le tienen fe
    La Calahorra de siempre, más viva que nunca
    La novela negra del siglo XXI no existe (sin Michael Connelly)
    'Company, el Musical' llega a Madrid
    Disfruta de 'El Cascanueces' en Cine Yelmo
    Fernando Cayo es Scrooge en 'Cuento de Navidad'
    'El Guardaespaldas, el musical' llega a tu ciudad
    La temida voltereta de la abolición de los toros en el sur de Francia quedó en un susto
    Las obras de mejora de la plaza de toros de Las Ventas comienzan en diciembre
    Actos a favor y en contra de los toros en Francia antes de que se debata su prohibición
    Luis Miguel Leiro, picador premiado y desencantado: “Amo y respeto a los animales, pero el toro ha nacido para la lidia”
    Cuando la furia de Twitter empaña un (interesante) debate narrativo
    La curva de la semana: sube Cristina Morales, está aquí Aldo Manucio, baja Rosalía
    Las nuevas coordenadas culturales de Latinoamérica
    Las más bellas cartas de amor en castellano, las memorias de Marguerite Duras y otros libros de la semana
    Amor mío queridísimo: la delicadeza sentimental de Felisberto Hernández
    Ellas fueron modernas: cuatro artistas alemanas en la vorágine del cambio de siglo
    Anacrónicas y audaces: las cantautoras latinas que renuevan la música de raíz
    Los mejores libros infantiles y juveniles de noviembre
    Palabra de Kafka
    Una ‘Yerma’ con poco nervio y zozobra
    Lo nuevo de Pablo Remón es una virguería teatral y la actriz Fernanda Orazi es un fenómeno
    Lo que jode es la respuesta: la diferencia entre crítica, cancelación y censura
    Edmonia, Frida y Amrita: tres mestizas
    La basura se lee con anteojos
    Mi otoño alemán
    ‘Percusión’: una novela del pasado para recordar el futuro
    Pere Gimferrer dentro del laberinto
    ‘La brecha’: cómo cambiar un mundo mal hecho
    ‘Tu sueño imperios han sido’: la historia boca arriba
    Nona Fernández: “En Chile intentan que conciliemos el sueño otra vez”
    Cristina Lucas: “Todo lo que se publicita está sobrevalorado”
    Enrique Gracián: “Hay infinitos más grandes que otros”
    Àlex Brendemühl: “La serie sobre el rey emérito no te deja indiferente”
    Marta Etura: “De no ser actriz, habría sido matrona”
    El calendario
    Universo Mundial
    La galería del día
    Las predicciones
    La ‘newsletter’
    Vinicius y Casemiro se alían contra Suiza
    Una noche feliz en el jardín de Neymar 
    Bruno Fernandes somete a Uruguay 
    La elevación del delito
    Educar en tiempos de Mundial
    España gana 1-1
    El Mundial de los valientes
    La España competente de Luis Enrique
    ¿Qué opciones tiene cada selección para pasar a octavos de final del Mundial?
    Un espontáneo con una bandera LGTBI salta al campo en mitad del Portugal-Uruguay
    Dimite la junta de la Juventus al completo
    Gol anulado
    Camerún y Serbia sobreviven al caos y empatan a tres
    Ghana deja a Corea en la cuerda floja
    España sabe competir
    Dani Olmo: “Nos faltó más control”
    Los 15 jugadores de España que han sellado el empate ante Alemania, uno por uno 
    Mundial de Qatar 2022, últimas noticias en directo | Benzema podría volver a la concentración francesa, según RMC
    Busquets descubre las carencias de Alemania
    Datos y gráficos | Alemania explota un error de España para empatar un partido equilibrado
    Última hora del Mundial de Qatar: vídeo en directo | Fútbol Sapiens
    Las razones por las que el portero de Camerún, Onana, se va del Mundial de Qatar 2022 
    Alfredo Relaño sobre Musiala: “Es un jugador de los que coges el coche para verle en Bilbao”
    Es nieta de un mito del Barça y arrasa en TikTok. El secreto de esta artista de 20 años que quiere emular a Rosalía
    Cómo no perderte ni un solo minuto del Mundial
    Las promesas del baloncesto español piden consejo a Sergio Scariolo
    A toda mecha hacia el mundial de la consagración
    Cómo disfrutar de la montaña con todas las garantías
    Rodrygo Goes, de niño hipnotizado por Neymar a heredero del 10
    Así hemos contado el Camerún - Serbia del Mundial de Qatar 
    Así le hemos contado el empate entre España y Alemania
    Reciclaje de escenarios
    Pomés, 9º del mundo (+65)
    Resumen de la jornada 8 del Mundial de Qatar 2022
    La elevación del delito
    Educar en tiempos de Mundial
    Adrian Hon, diseñador de videojuegos: “Las empresas y gobiernos usan juegos para controlarnos”
    Mastodon: qué es y cómo funciona la red social en la que los usuarios deciden qué está permitido
    Así serán las nuevas marcas de verificación en Twitter: azul, oro y gris
    Gafas con funciones de un móvil, ‘Photoshop’ instantáneo y otros inminentes avances gracias a los nuevos chips
    Elon Musk ya edita tuits y Twitter no se ha hundido aún, ¿qué hará en el futuro?
    Elon Musk declara una “amnistía general” en Twitter para las cuentas suspendidas
    Así está fallando Twitter: racismo, derechos de autor y desprotección en dictaduras
    Quo Vadis, Elon Musk: por qué el colapso de Twitter no es un divertimento
    Candid Wüest: “Si alguien ‘apaga’ Ucrania, probablemente haya una respuesta y eso no interesa porque todos los países son vulnerables”
    El reclutamiento de personal se reinventa en las redes: “Se crea una relación de confianza entre los candidatos y las empresas mucho antes de haber contacto directo”
    El biógrafo de Elon Musk: “Para él, el caos es el procedimiento operativo estándar”
    Aplicaciones, relojes y etiquetas QR ayudan a evitar la desaparición de personas con demencia
    Cómo acorazar el ‘router’ ante un ciberataque con estos sencillos pasos
    La confusa nueva política de Elon Musk en Twitter: permitir mensajes de odio, pero que se vean menos
    ¿Y si cierra Twitter? Cómo descargar el historial y borrar los mensajes directos
    La banca confía en tumbar en los tribunales el nuevo impuesto al sector
    Los cuatro coches que llegaron a España en el año de los Juegos y la Expo
    Ocho mil millones de cursis
    Guía de viaje a la nube: una aventura con escalas
    Árboles tuiteros contra la ceguera botánica
    De Baudelaire a Midjourney: los nuevos “enemigos mortales del arte”
    Adrian Hon, diseñador de videojuegos: “Las empresas y gobiernos usan juegos para controlarnos”
    Mastodon: qué es y cómo funciona la red social en la que los usuarios deciden qué está permitido
    Así serán las nuevas marcas de verificación en Twitter: azul, oro y gris
    Gafas con funciones de un móvil, ‘Photoshop’ instantáneo y otros inminentes avances gracias a los nuevos chips
    Elon Musk ya edita tuits y Twitter no se ha hundido aún, ¿qué hará en el futuro?
    Elon Musk declara una “amnistía general” en Twitter para las cuentas suspendidas
    Así está fallando Twitter: racismo, derechos de autor y desprotección en dictaduras
    Quo Vadis, Elon Musk: por qué el colapso de Twitter no es un divertimento
    Candid Wüest: “Si alguien ‘apaga’ Ucrania, probablemente haya una respuesta y eso no interesa porque todos los países son vulnerables”
    El reclutamiento de personal se reinventa en las redes: “Se crea una relación de confianza entre los candidatos y las empresas mucho antes de haber contacto directo”
    El biógrafo de Elon Musk: “Para él, el caos es el procedimiento operativo estándar”
    Aplicaciones, relojes y etiquetas QR ayudan a evitar la desaparición de personas con demencia
    Cómo acorazar el ‘router’ ante un ciberataque con estos sencillos pasos
    La confusa nueva política de Elon Musk en Twitter: permitir mensajes de odio, pero que se vean menos
    ¿Y si cierra Twitter? Cómo descargar el historial y borrar los mensajes directos
    La banca confía en tumbar en los tribunales el nuevo impuesto al sector
    Los cuatro coches que llegaron a España en el año de los Juegos y la Expo
    Ocho mil millones de cursis
    Guía de viaje a la nube: una aventura con escalas
    Árboles tuiteros contra la ceguera botánica
    De Baudelaire a Midjourney: los nuevos “enemigos mortales del arte”
    Camila rompe una de las tradiciones históricas de la monarquía: no tendrá damas de compañía 
    Helena Bonham Carter defiende a su amigo Johnny Depp y critica la cultura de la cancelación: “Hay una caza de brujas”
    El silencio es el nuevo lujo: cómo vivir en un mundo cada vez más ruidoso nos ha hecho pagar por algo gratuito
    Confesiones de la mujer que lleva 40 años decidiendo quién será James Bond
    Atún rojo: el inesperado nexo cultural que une a Japón con el Mediterráneo
    Las excentricidades imposibles de las Kardashian: de escáneres cerebrales a 700 dólares en gominolas de cannabis
    Mis séptimos Premios Icon
    Los 12 patios del palacio de Viana en Córdoba: una muñeca rusa llena de plantas
    Arnau Griso, el adiós de un grupo que empezó como una broma y acabó creando el pop ‘buenrollero’: “Tenemos la necesidad de matar al padre”
    De Kim Kardashian en la cárcel a Selena Gómez con los Beckham: así celebran Acción de Gracias de los famosos
    Windsor desvela su decoración navideña en las primeras festividades sin Isabel II y con Carlos III como rey
    Una gran fiesta en el pequeño mundo ideal de ICON
    Sumer, el ‘kebab’ artesano de barrio en Madrid que acoge tertulias filosóficas
    Achilles Ion Gabriel, el surrealista de Camper: “No hago zapatos para museos, sino para la gente” 
    El regreso discreto de Mario Testino: “A mi edad, no creo que mi percepción de la moda sea la correcta ni la que el mundo necesita”
    Manuel Outumuro toca cumbre
    Diane de Beauvau-Craon, la última princesa rebelde: “Me drogué mucho, bebí mucho alcohol, me acosté con muchos gais y aquí sigo”
    Marta Ortega reúne en A Coruña a grandes protagonistas de la moda internacional en la inauguración de la muestra sobre Steven Meisel
    Las abuelas que han viralizado el arte de elaborar la pasta italiana 
    Humaredas mediáticas, monotonía, discursos vacíos y otras amenazas y retos de la gastronomía 
    Sumer, el ‘kebab’ artesano de barrio en Madrid que acoge tertulias filosóficas
    Los guardianes de la ensaladilla rusa, la tapa popular que subió a los altares ‘gourmet’ 
    El robot de cocina más famoso del mundo ha conquistado ya tres millones de hogares españoles
    Radiografía de ‘El hormiguero’: entretenimiento blanco de éxito… y polémicas por machismo
    ‘The Peripheral’, realidad, ficción y un futuro ciberpunk con los creadores de ‘Westworld’
    El ‘bon vivant’ acorralado de la FIFA que grabó a sus amigos
    ‘Ummo’, un guirigay intergaláctico
    Adiós a Ellen Pompeo, la funcionaria de la tele
    ‘This England’
    El gol a Infantino de dos ministras europeas
    Leonor Lavado: “Somos como hablamos: la voz es nuestro ADN psicológico”
    ¿Qué ocurre tras la edad de oro de la televisión? El mismo oro, aunque enterrado bajo una oferta masiva
    ‘La ruta’: por qué nos invade la nostalgia del ‘after’
    La veteranía de María del Monte y Francisco se mide con la juventud de María Terremoto y Juanlu Montoya en los premios Radiolé  
    La violencia machista entre los adolescentes, el drama que ni ellos quieren reconocer
    ‘La Sagrada Familia’ rescata el mito Pujol y disecciona su caída
    Álex Pina, creador de ‘La casa de papel’, encierra a ricos en un búnker de lujo durante el fin del mundo en su nueva serie en Netflix
    Regreso al hospital terrorífico de Lars von Trier
    Ander Puig, el fichaje trans de ‘Élite’: “Voy a recibir mucho amor y mucho odio”
    Cómo ‘Amar es para siempre’ se convirtió en un icono televisivo
    ¿Qué ver hoy en TV? Lunes 28 de noviembre de 2022
    Las series de agosto de 2022: ‘La casa del dragón’ en HBO Max; ‘Sandman’ en Netflix y otras
    Nueve capítulos para recordar ‘The Wire’ en su 20º aniversario
    Harry Palmer: el tercer vértice del mágico triángulo de espías británicos
    Las series de junio de 2022: ‘The Boys’ en Amazon Prime Video; ‘Peaky Blinders’ en Netflix y otras
    Llega la nueva serie de Jeff Bridges, que no da un minuto de tregua
    Las abuelas que han viralizado el arte de elaborar la pasta italiana 
    El misterio de Manuel Carrasco: cómo salir de una barriada de pescadores y acabar siendo un cantante que llena estadios
    Muchos hombres, una sola mujer
    Ishida, los ‘dioses’ de la cocina japonesa: “Tenemos que dejar de desear tantas cosas, y hay que hacerlo ya”  
    Humaredas mediáticas, monotonía, discursos vacíos y otras amenazas y retos de la gastronomía 
    Los guardianes de la ensaladilla rusa, la tapa popular que subió a los altares ‘gourmet’ 
    Cerdo pío negro, el inesperado rival del ibérico
    Narcisistas, ansiosos, pasivo-agresivos… Cinco claves para tratar con personas difíciles
    Al fondo, invisibles, las pirámides
    Viaje al sabor de la tradición
    Todo es mejor con chocolate y estas cinco recetas lo demuestran
    Crecer bajo las bombas
    El secreto del maíz gigante mexicano que bajó del volcán
    Por qué el R5 eléctrico abre un nuevo camino en Renault
    El milagro alemán
    Consuelo
    Sin tiempo
    La bióloga que se propuso repoblar los bosques de Brasil
    Un parche para conseguir que las vacunas sean más baratas y accesibles
    Cerdo pío negro, el inesperado rival del ibérico
    Ishida, los ‘dioses’ de la cocina japonesa: “Tenemos que dejar de desear tantas cosas, y hay que hacerlo ya”  
    El secreto del maíz gigante mexicano que bajó del volcán
    ‘Mis primeros recuerdos’, por Daniel Barenboim
    El indómito espíritu creativo de Picasso
    Medio siglo sin Picasso
    Paloma Picasso se confiesa con Nuccio Ordine
    El amigo de Picasso sin el que no estaría en España el ‘Guernica’
    Tommy Hilfiger: “Muchos de nuestros clientes van a vivir en el metaverso. De hecho, ya lo hacen”
    Storm Pablo: el estilista que convirtió a Bad Bunny en icono también de la moda
    El hombre que cultiva las flores más caras para los perfumes más especiales
    Una casa junto al lago Como que es pura diversión 
    Desayuno a la mexicana entre hípsters de mañaneo y polis con más apetito que buena fama
    El misterio Picasso
    Isabel II: el reinado de la imagen
    Un día en la vida de un país: San Sebastián-Cádiz en 16 horas
    Luces y sombras de Robert Mapplethorpe
    

Es importante mencionar que se utiliza el comando clear antes de mostrar los resultados por la termial para que la consola quede limpia y se vean bien los titulares extraídos con el código Python.


```python
os.system("clear")
```




    1



Las categorías por las que se van a clasificar los titulares extraídos se muestran


```python
print(colored("A continuación se muestran los titulares de las páginas principales del diario El País que contienen las siguientes palabras:", 'blue', attrs=['bold']))

```

    A continuación se muestran los titulares de las páginas principales del diario El País que contienen las siguientes palabras:
    

## Titulares extraídos por categorías


```python
Se muestra el título de la categoría en la consola.
```


```python
print(colored("Feminismo", 'green', attrs=['bold']))
```

    Feminismo
    

El bucle for se utiliza para filtrar los titulares por categoría. Este en ccomprueba si el titular contiene la palabra clave y queda guardado el titular en la variable `str_match`.


```python
str_match = [s for s in resultados if "feminismo" in s]
```

Finalmente, se muestran todos los titulares de la categoría en concreto.


```python
print("\n".join(str_match))
```

    Americanas: Reportajes y noticias sobre feminismo e historias con enfoque de género de la región
    El feminismo se fractura en Madrid en las protestas contra la violencia machista que recorren España
    El feminismo se fractura en Madrid en las protestas contra la violencia machista que recorren España
    

Este último bloque de código se repite tantas veces como categorías se definan.


```python
print(colored("Igualdad", 'green', attrs=['bold']))

str_match = [s for s in resultados if "igualdad" in s]
print("\n".join(str_match))

print(colored("Mujeres", 'green', attrs=['bold']))

str_match = [s for s in resultados if "mujeres" in s]
print("\n".join(str_match))

print(colored("Mujer", 'green', attrs=['bold']))

str_match = [s for s in resultados if "mujer" in s]
print("\n".join(str_match))

print(colored("Brecha salarial", 'green', attrs=['bold']))

str_match = [s for s in resultados if "brecha salarial" in s]
print("\n".join(str_match))

print(colored("Machismo", 'green', attrs=['bold']))

str_match = [s for s in resultados if "machismo" in s]
print("\n".join(str_match))

print(colored("Violencia", 'green', attrs=['bold']))

str_match = [s for s in resultados if "violencia" in s]
print("\n".join(str_match))

print(colored("Maltrato", 'green', attrs=['bold']))

str_match = [s for s in resultados if "maltrato" in s]
print("\n".join(str_match))

print(colored("Homicidio", 'green', attrs=['bold']))

str_match = [s for s in resultados if "homicidio" in s]
print("\n".join(str_match))

print(colored("Género", 'green', attrs=['bold']))

str_match = [s for s in resultados if "género" in s]
print("\n".join(str_match))

print(colored("Asesinato", 'green', attrs=['bold']))

str_match = [s for s in resultados if "asesinato" in s]
print("\n".join(str_match))

print(colored("Sexo", 'green', attrs=['bold']))

str_match = [s for s in resultados if "sexo" in s]
print("\n".join(str_match))
```

## Ejecución del código fuente 


```python
import requests
import time
import csv
import re
from bs4 import BeautifulSoup
import os
import pandas as pd
from termcolor import colored
 
resultados = []
 
req = requests.get("https://resultados.elpais.com")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup = BeautifulSoup(req.text, 'html.parser')
 
tags = soup.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req2 = requests.get("https://elpais.com/internacional")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup2 = BeautifulSoup(req2.text, 'html.parser')
 
tags = soup2.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req3 = requests.get("https://elpais.com/opinion")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup3 = BeautifulSoup(req3.text, 'html.parser')
 
tags = soup3.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req4 = requests.get("https://elpais.com/espana/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup4 = BeautifulSoup(req4.text, 'html.parser')
 
tags = soup4.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req5 = requests.get("https://elpais.com/economia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup5 = BeautifulSoup(req5.text, 'html.parser')
 
tags = soup5.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req6 = requests.get("https://elpais.com/sociedad/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup6 = BeautifulSoup(req6.text, 'html.parser')
 
tags = soup6.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req7 = requests.get("https://elpais.com/educacion/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup7 = BeautifulSoup(req7.text, 'html.parser')
 
tags = soup7.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req8 = requests.get("https://elpais.com/clima-y-medio-ambiente/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup8 = BeautifulSoup(req8.text, 'html.parser')
 
tags = soup8.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req9 = requests.get("https://elpais.com/ciencia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup9 = BeautifulSoup(req9.text, 'html.parser')
 
tags = soup9.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req10 = requests.get("https://elpais.com/cultura/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup10 = BeautifulSoup(req10.text, 'html.parser')
 
tags = soup10.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req11 = requests.get("https://elpais.com/babelia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup11 = BeautifulSoup(req11.text, 'html.parser')
 
tags = soup11.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req12 = requests.get("https://elpais.com/deportes/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup12 = BeautifulSoup(req12.text, 'html.parser')
 
tags = soup12.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req13 = requests.get("https://elpais.com/tecnologia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup13 = BeautifulSoup(req13.text, 'html.parser')
 
tags = soup13.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req14 = requests.get("https://elpais.com/tecnologia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup14 = BeautifulSoup(req14.text, 'html.parser')
 
tags = soup14.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req15 = requests.get("https://elpais.com/gente/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup15 = BeautifulSoup(req15.text, 'html.parser')
 
tags = soup15.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req16 = requests.get("https://elpais.com/television/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup16 = BeautifulSoup(req16.text, 'html.parser')
 
tags = soup16.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
req17 = requests.get("https://elpais.com/eps/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup17 = BeautifulSoup(req17.text, 'html.parser')
 
tags = soup17.findAll("h2")
 
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
 
 
os.system("clear")
 
print(colored("A continuación se muestran los titulares de las páginas principales del diario El País que contienen las siguientes palabras:", 'blue', attrs=['bold']))
print(colored("Feminismo", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "feminismo" in s]
print("\n".join(str_match))
 
print(colored("Igualdad", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "igualdad" in s]
print("\n".join(str_match))
 
print(colored("Mujeres", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "mujeres" in s]
print("\n".join(str_match))
 
print(colored("Mujer", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "mujer" in s]
print("\n".join(str_match))
 
print(colored("Brecha salarial", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "brecha salarial" in s]
print("\n".join(str_match))
 
print(colored("Machismo", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "machismo" in s]
print("\n".join(str_match))
 
print(colored("Violencia", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "violencia" in s]
print("\n".join(str_match))
 
print(colored("Maltrato", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "maltrato" in s]
print("\n".join(str_match))
 
print(colored("Homicidio", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "homicidio" in s]
print("\n".join(str_match))
 
print(colored("Género", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "género" in s]
print("\n".join(str_match))
 
print(colored("Asesinato", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "asesinato" in s]
print("\n".join(str_match))
 
print(colored("Sexo", 'green', attrs=['bold']))
 
str_match = [s for s in resultados if "sexo" in s]
print("\n".join(str_match))
```
