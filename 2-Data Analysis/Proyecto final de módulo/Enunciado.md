# Proyecto de final de módulo  - Fecha de entrega sabado 29 de junio

En este proyecto final recopilaremos los conocimientos adquiridos durante este primer módulo y nos centraremos en las habilidades de los distintos roles implicados en la construcción y análisis de los conjuntos de datos. Dentro del ciclo de vida del dato nos hemos centrado en tres aspectos clave:

- **Data Engineering**: Construir conjuntos de datos acorde a las necesidades de nuestro negocio. Empleando herramientas como Python y todas sus extensiones, webscrapping y consultas de APIs. Junto con SQL y ser capaz de modelar tablas en nuestro destino, podemos organizar la información para que no solo sea util hoy sino en el futuro de nuestro negocio.
- **Data Scientist**: Ser capaz de analizar los datos para entender su correcta construcción, población que representan nuestras muestras. Posibles problemas y sesgos implicados en la recolección de los datos, etc. Empleando similares herramientas pero enfocado en paquetes clave (Jupyter, Pandas, Numpy, Plotly) podemos crear evidencias que nos lleven a una mejor comprensión del contexto de los datos.
- **Data Analyst**: Ser capaz de condensar toda la información presente en nuestro sistema y presentársela a usuarios clave de forma que el mensaje sea claro y conciso, atractivo y lo menos sesgado posible. Para ello, las herramientas clave serán las plataformas de BI y las bases de datos que soportarán las operaciones requeridas por estas soluciones.

Para poner a prueba nuestras habilidades en estos roles tomaremos como punto de partida los datos accesibles en multitud de plataformas sobre las **elecciones europeas**.

# **Nuestro empleador requiere que analicemos los datos obtenidos para entender el contexto político y las posibles tendencias que puedan surgir de cara a las próximas elecciones tanto europeas como locales.**

Disponéis de multitud de fuentes de las que poder extraer esta información en [la plataforma centralizadora del gobierno](https://datos.gob.es/es/catalogo?q=elecciones+europeas&sort=score+desc%2C+metadata_created+desc).

Lo importante será construir un modelo sólido tanto de entrada de datos como de salida de conclusiones y que estas sean presentadas de manera elocuente durante las presentaciones de final de módulo.

![dwarehouse](./img/deda_0402.png)

### Equipos

Se realizarán por grupos, pudiendo también realizarse de manera individual si así se quisiera.

### Infraestructura

Necesitaréis una base de datos a la que poder conectaros desde distintos puntos/ordenadores. Aquí os dejamos algunos servicios que os permitirán levantar bases de datos relacionales de manera gratuita:

- [Render](https://render.com/docs/databases)
- [Aiven](https://aiven.io/)

Estos elementos serán la pieza central de vuestro proyecto (el Data Warehouse).

### Tareas a Realizar

Existen tres fases que se retroalimentan unas a otras. No lo veáis como un flujo temporal 1,2 y 3 ya que los análisis de los DS o DA pueden ayudar a los DE a construir un modelo de datos más solido.

**Data Engineering**:  
Dilucidar el modelo de datos que os permita aunar fuentes. Si los datos refieren a elecciones, muy posiblemente habrá una entidad **PARTIDO** con información asociada, una entidad **MUNICIPIO** donde se realizaron las votaciones, y unos hechos medibles que son nuestros votos a una fecha dada. Los municipios pueden incluir información relativa a la **COMUNIDAD** si fueran de varias; o los partidos de **CORTE** (izquierda, centro, derecha,...) de cara a entender tendencias poblacionales de voto.

En un primer bloque se deberá:

- Construir el modelo lógico de tablas a emplear
- Obtener los datos y poblar los datos acorde al esquema
- Validar que este modelo es extensible (nuevos partidos, nuevas comunidades, nuevas elecciones en años futuros).
- [The Data Warehouse Toolkit](https://learning.oreilly.com/library/view/the-data-warehouse/9781118530801/9781118530801c03.xhtml#c03_level1_2)
- [Data Engineering with Python](https://learning.oreilly.com/library/view/data-engineering-with/9781839214189/)

**Data Science**:  
Bajo los datos a integrar puede haber distintas cuestiones a validar. Sobretodo nos interesa saber si los datos son correctos, existen datos faltantes o hay sesgos/errores en la recogida de los mismos. Imaginaros qué pasaría si los datos mostraran no proceder de una muestra aleatoria de la población.

En este segundo bloque se deberá:

- Analizar el contenido de los conjuntos de datos.
- Realizar validaciones de carácter estadístico
- Complementar la información inicial con posibles conjuntos de datos necesarios para una mejor representación (ubicaciones para colocar los datos en mapas, por ejemplo).
- [Making Sense of Data](https://learning.oreilly.com/library/view/making-sense-of/9780470074718/ch5-sec002.html#ch5-sec002)
- [SQL for Data Analysis](https://learning.oreilly.com/library/view/sql-for-data/9781492088776/)

**Data Analyst**:  
Por último, apoyado en el trabajo realizado por los dos roles anteriores, os pedimos que mostréis una historia sobre de dónde viene y a dónde va España, Europa o vuestro pueblo. Qué nos cuentan los datos ¿Crece la derecha? ¿La izquierda? ¿Aparecen partidos nuevos? ¿Qué nos cuentan los datos va a suceder?

En este tercer bloque se deberá:

- Construir un informe sobre la información obtenida. Visual y claro a poder ser.
- Mostrar conclusiones sobre los datos que sean entendibles por un público general
- Trabajar cierta interacción/estética de manera que no resulte un informe aséptico y poco atractivo.
- [Data Visualization with PowerBI](https://learning.oreilly.com/library/view/data-visualization-with/9781098152772/)
- [SQL for Data Analysis](https://learning.oreilly.com/library/view/sql-for-data/9781492088776/)

Os recomendamos seguir los pasos que estipula CRISP-DM en sus primeras etapas y emplear una herramienta de seguimiento para saber si todas las tareas clave están siendo acometidas.

- Fases clave CRISP-DM https://www.ibm.com/docs/es/spss-modeler/saas?topic=modeler-crisp-dm-project-tool
- Asana: https://asana.com/es
- Github Project
- Airtable: https://airtable.com/
- Trello: https://trello.com/es

# Evaluación

Cada fase o rol se evaluará con un tercio de la nota. Cada fase se evaluará hasta 1/3 y la suma de las partes harán que podamos llegar a los 10 puntos de la nota final en el ejercicio.

### Entregables

El entregable será la presentación de los tres bloques del trabajo (5 min cada bloque) finalizando con la presentación visual y conclusiones derivadas. Es importante que todos los miembros de un equipo cuenten sus tareas de cara a demostrar que a existido cierta cooperación de todos los integrantes.

# Herramientas

Como ayuda existen varias herramientas en las que os podéis ayudar. Recordad que todo lo podremos gestionar con Python pero existen soluciones que facilitan ciertas labores:

- Modelado E/R, Relacional o Estrella: [ERDPlus](https://erdplus.com/)
- Gestión de base de datos: [DBeaver](https://dbeaver.io/)
- Visualización: [PowerBI](https://powerbi.microsoft.com/es-es/desktop/) o [Astrato](https://astrato.io/)
