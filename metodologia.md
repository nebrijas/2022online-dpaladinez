
# Metodologia

La construcción de este sitio web fue solo posible gracias a las herramientas y plataformas de programación facilitadas por el profesor durante las clases de Periodismo de Datos II: Herramientas Digitales para la Visualización y Presentación de Datos. En donde nos familiarizamos con los lenguajes de programación Python y Markdown, lenguajes los que está baso la estructura de los ejércitos y las diferentes secciones de nuestra página. 

- [Actividad dirigida 1](ad1.md)
- [Actividad dirigida 2](ad2.md)
- [Actividad dirigida 3](ad3.md)
- [Actividad dirigida 4](ad4.md)

Esta actividad consistió en hacer un comentario crítico sobre una pieza de periodismo de datos, visualización de datos o infografía. Para hacer el anális usamos lo aprendido en Periodismo de Datos I. La pieza analizada fue esta.

Al principio esta actividad fue desafiante pues no conocía el lenguaje markdown y nunca había oido hablar de GitHub.

Usamos el editor de texto o "pad" que nos permitió escribir el texto de forma colaborativa. Este editor fue "riseup". Cada uno escribió su texto en lenguaje markdown, una lenguaje que se asemeja al "código fuente" de un texto y que se utiliza para componer páginas web, cuadernos de Python y para gráficos interactivos. También sirve para la transformación a cualquier formato estructurado como PDF, docx o HTML de los contenidos.

El codigo de markdown nos permitió phacer:

Encabezados de diferente nivel con almohadillas #.

Negrita, utilizando 2 asteriscos al principio y al final del texto.

Enlaces, con el texto a enlazar entre corchetes y la url entre paréntesis.

Eso al principio, luego aprendimos sobre el repositoria GitHub, que es un portal usado para alojar el código de las aplicaciones de cualquier desarrollador. En este guardamos el contenido que elaboramos en lenguaje markdown.

Cuando estuve más familiriazada pude añadir en el GitHub imágenes con atributos alt y links. La imágenes se pueden añadir como desde la url o subiendo directamente los archivos al repositorio.

En este caso añadí la infografía como una imagen desde la url poniendola entre paréntesis precedida por el atributo alt entre corchetes y el signo de admiración final.

La ad1 se puede ver aquí.

Cada uno desde su usuario en GitHub creo una pequeña página web compuesta por las carpetas de cada una de las actividades que desarrollamos durante el curso, nombrándolas de la misma forma pues es importante cuidar la unidad en la escritura para facilitar su ejecución.

Estos contenidos están disponibles y se pueden visualizar online gracias a "pages". Esta aplicación te permite publicar el código del sitio en vivo en la web.

Actividad 2 (ad2)
Esta actividad consistió en realizar un comentario de un artículo o reportaje de periodismo y visualización de datos. También fue escrito en markdown y subido al repositorio de Github.

En este caso fue, este reportaje sobre los mundiales, que contiene un gráfico que me llamó mucho la atención por la forma como está hecho. Es el que se muestra en la imagen destacada del comentario.

En este ejercicio ya estaba más familiarizada con el markdown y el GitHub entonces pude aprender más cosas, como que se puede cargar una imagen como archivo al repositorio. En este ejercicio añadí la infografía que analicé, precedida por un atributo alt que explica el contenido de la imagenen, y el signo de admiración final al inicio del código.

El comentario estuvo relacionado a lo aprendido en las clases sobre la forma correcta de hacer visualizaciones y el uso de los datos en estas. Este ejercició también se subió al repositorio de GitHub.

La ad2 se puede ver aquí.

Actividad 3 (ad3)
Acá transformamos un ejercicio de código de Python para lograr un scraping de una web. Esto significa sacar datos mediante algunas herramientas o librerías que leen el código.

En este ejercicio profundizamos un poco más en las herramientas para el análisis y la visualización de datos. Lo primero que hicimos fue instalar Anaconda, un sofware de procesamientos de datos que tiene diferentes lenguajes de programación. Una vez se instalado, pudimos acceder desde allí a jupyter, una aplicación web que permite generar cuadernos de Python y Markdown. Y desde jupyter comenzamos a hacer un ejercicio de programación literaria.

El archivo que desglosamos fue un código de python (py) y comentamos el paso a paso.

En este ejercicio aprendí que hay varias librerías que nos permiten leer código python. Entre ellas están: pandas, request, termcolor, BeautifulSoup, entre otras. Algunas de estas liberías son externas y otras vienen con la herramienta anaconda que anteriormente nos habíamos descargado a nuestro computador.

Me pareció un ejercicio muy util para sacar información muy específica por medio de etiquetas o "tags". La idea fue lograr un ejercicio en el que entendieramos lo que estábamos haciendo y luego, si lo veíamos después de un tiempo, pudieramos leer de igual forma. Es como un hilo argumental en un cuaderno de notas.

Lo más importante de la actividad fue descargar las librerías y ponerlas a correr para luego ejecutar las acciones en orden a obtener los datos.



Librerías que vienen instaladas:

csv: (valores separados por comas). Es el formato habitual de importación y exportación de hojas de cálculo y bases de datos.

re: esta nos ayuda para la coincidencia de expresiones regulares similares a las encontradas en Perl.

os: nos ayuda a usar funciones del sistema operativo.

time: tiene varias funciones relacionadas con el tiempo.

Librerías que hay que instalar:

requests: se usa para hacer solicitudes y peticiones a la página de la que extraeremos datos.

pandas: es una herramienta de análisis de datos de código en el lenguaje de python.

Termcolor: sirve para imprimir mensajes de colores en el terminal.

BeautifulSoup sirve para obtener datos en formato HTML y XML.

Luego buscamos obtener los resultados. Para esto llamamos a la libería request que nos ayudó a descargar los resultados de la página de El País en sus distintas secciones. Y así sucesivamente llamamos a las otras liberías para extraer los datos que necesitabamos en este caso lo títulos h2.

Con el código correcto se le puede ir dando valor a las distintas variables para que extraigan cualquier tipo de información como palabras, títulos, listas, números etc. Con Termcolor se pueden imprimir mensajes con color.

Al finalizar la actividad descargamos del jupyter dos archivos uno en formato jupyter y otro en formato markdown para subirlos respectivamente al GiyHub y al campusvirtual de Nebrija.

Actividad 4 (ad4)
La actividad consistió en conectar desde Jupyter a la API de datos del COVID19 a la que se puede acceder aquí.

Fue la actividad a mi modo de ver más interesante porque pudimos elaborar gráficos con datos relevantes sobre la pandemia de varios paises como Colombia, Ecuador, República Dominicana y España. Además hicimos el recorrido literario de cada una de las acciones mirando los diferentes usos de las variables y los códigos.

Aquí aprendí lo que es un dataframe, que es un marco de datos que sirve para encerrar, organizar e ilustrar la información. A este dataframe se le puede explorar de muchas formas y nos brinda la información que necesitamos para comparar los datos y obtenerlos ordenados, de forma que podamos hacer gráficos.

dataframe

Asímismo aprendí a sobre la función j_son que sirve para leer código JavaScript.

Finalmente, para elaborar un gráfico, el objetivo principal de esta actividad, seleccionamos los ejes, en este caso la fecha y el número de casos. Luego lo ilustramos con "plot" de plotear (df_co.set_index('Date')['Cases'].plot()) y por último lo nombramos añadiendo al final la función "title".

gráfico COVID19 en Colombia

La ad4 se puede ver aquí.

Y con eso terminamos las actividades de la materia pero no el aprendizaje :)
