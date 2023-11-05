# call-center
Analisis de gestion laboral y atención al cliente

Con el objeto de aumentar la calidad de servicio, nos piden analizar el rendimiento de un call center perteneciente de la empresa "Anonymous Bank" en base a un dataset de 444 mil registros que comprende un periodo de 12 meses(01/01/99 - 31/12/99); determinaremos el rendimiento de los agentes de llamadas y ofreceremos recomendaciones para la mejora del servicio.

En el proceso de ETL solo se elimino una columna que solo tenia datos nulos, se sustituyo el el tipo de cliente 0 por 1 debido a que la empresa los considera como "No prioritarios", se cambio el tipo de dato de la columna call_id por texto.

Con respecto al Dashboard se estructuró de la siguiente manera, en la parte izquierda de colocaron los segmentadores de datos, en la parte superior se puede selecionar el tipo de cliente, de dabajo se encuentran los segmentadores de outcome y Type(tipo de servicio), en la parte superior central se colocaro las siguientes medidas: promedio VRU, AVG Q, AVG Ser, Clientes Únicos, AVG Tiempo en línea y AVG Tiempo de Espera, debajo se agregaron 4 graficos de anillos que permiten la comparación de dos medidas, los mismos son: Llamadas_Atendidas - Llamadas-no_Atendidas, Llamadas_clientes_VIP - Llamadas_Clientes_Regulares, %Llamadas<60 - %Llamadas>60 este indicador muestra las llamadas que tienen un tiempo de espera por debajo y por arriba de la meta de 60 segundos, Recurrentes - No_Recurrentes muestra los clientes que han usado el servicio mas de una vez, el medidor Empleados Necesarios muestra los agentes de llamadas que se necesitan para que el tiempo de espera sea igual o menor a 60 segundos.

El gráfico de barras call_id por type nos indica la relación del número de llamadas con respecto al tipo de servicio.

El gráfico de linea Llamadas_Atendidas por Mes muestra el número de llamadas que son atendidas por agente con respecto a los meses del año.

El gráfico de barras LlamadasXdia por Server hace una relacion entre los días trabajados y el total de número de días trabajados, de esta manera se obtiene una medición mas objetiva del desempeño de los empleados

el gráfico de línea de tiempo Recuento de Call_id por Horadeldia ejemplifica el volumen de llamada por hora recibidas durante el transcurso del día.

En la parte inferior derecha encontramos una comparativa mediante un gráfico de barras (AVG_Tiempo_espera por priority) contrastando el tiempo de espera por categoría de cliente.

Se respondieron las siguientes preguntas planteadas 

¿Cuál es el nivel de servicio para los clientes Prioritarios?

El tiempo en espera de los clientes prioritarios para ser atendidos por un agente tiene una media de 92,41 segundos, lo que representa un 54% por arriba de la meta de 60 segundos. Con respecto a este tipo de clientes solo en 49% de las llamadas tiene un tiempo de espera menor o igual a 60 segundos, en comparación con el 74% de los clientes no prioritarios.

¿Damos un mejor servicio que a los clientes normales?

Para un cliente normal el tiempo de espera para ser atendido por un agente tiene una media de 58,94 segundos, muy por de bajo de la media de los clientes prioritarios(92,41 segundos), el 74% de las llamadas estan por debajo de los 60 segundos, lo cual contrasta con el 49% de los clientes prioritarios.

¿Qué volumen de llamadas atendemos?

Durante todo el año, se recibieron 444.448 llamadas, con una media mensual de 37.037 y diaria de 14.337

¿Cuáles son los cuellos de botella? ¿En qué días? ¿En qué bandas horarias?

Se observa que los días de mas concurrencia de llamadas son los domingos(19,55%) y los días martes(18,27%), con respecto a la hora se puede decir que  las 10am es la hora del día mas saturada con 9,12% de llamadas recibidas; el "cuello de botella" comprende 3 horas del día, de 9am a 11am, en este bloque se atienden el 25.26% de las llamas del día.

¿Cómo es la eficiencia y productividad de nuestros agentes?

De los 53 agentes de llamada 27(50.9%) están por encima de la media diaria referente al promedio de llamadas atendidas por día, un valor a considerar es el números de llamadas diarias(266) que no son atendidas por un agente lo que representa un 21,71% del total de llamadas.

¿Hay clientes recurrentes en el uso del servicio?

La empresa cuenta con una cartera de 12910 clientes, de los cuales el 79%(10202) han requerido el servicio mas de una vez

¿Cuáles son los tipos de servicio más recurrentes?

PS (Actividad Regular) comprende el 68% de los tipos de servicios mas solicitados, seguidos por NW(Cliente Potencial) con 15,28%.

¿Podemos estimar la dotación necesaria para cumplir con una calidad de servicio determinada?  Ejemplo: si quiero que mi tiempo promedio de espera sea menor a 60 segundos?

El manejo de recursos humanos en cualquier organización es primordial para que dicha organización sea competitiva, en este estudio se detecto que el tiempo promedio de espera para para los clientes prioritarios es de 92 segundos, muy lejos de la meta; en base al rendimiento de los  agentes que actualmente laboran, se estimo que para ofrecer un mejor servicio a los clientes prioritarios de sebe incrementar el numero de agentes de llamada de 8 a 13.

Se estimaron las siguientes recomendaciones:

*Optimizar el sistema VRU es importante para reducir el tiempo de espera, por ejemplo, reducir el menú de opciones, es decir, un menú mas largo incrementara el tiempo de espera, hacer las grabaciones mas cortas y precisas.



*El número de empleados debe incrementarse para reducir tiempo de espera



*Es de suma importancia optimizar el tipo de servicio NW, observamos una media de espera de 88,48 segundos, priorizar este servicio permitirá la captura de nuevos clientes



*Facilitar nuevas métricas permitirá análisis mas exactos y profundos, por ejemplo números de nuevos clientes por mes, número de clientes que abandonaron la empresa, calificación de los usuarios a sus agentes de llamada, entre otros.