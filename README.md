# ConnectaTel  
**Objetivo del Proyecto:** identificar patrones de uso, detectar comportamientos atípicos y comprender qué segmentos de clientes muestran necesidades diferenciadas, con el fin de optimizar la oferta comercial y mejorar la experiencia del usuario.  
**Data Sets utilizados:** plans.csv: los planes actuales (precio, minutos incluidos, GB incluidos, costo por extra).  
users_latam.csv: información de clientes: edad, ciudad, fecha de registro, plan contratado.  
usage.csv: el detalle de uso real: llamadas (duración) y mensajes (longitud).  
**Herramientas utilizadas:** Python & Pandas  
**Etapas del análisis realizadas:**   
**Paso 1:** Cargar y explorar la estructura de los datasets  
**Paso 2:** Identificación de problemas de calidad de datos (Revisión de valores nulos, Detección de valores inválidos y sentinels, Revisión y estandarización de fechas  
**Paso 3:** Limpieza básica de datos (Corregir sentinels y fechas imposibles)  
**Paso 4:** Summary statistics de uso por usuario (Agrupación por comportamiento de uso, Resumen estadístico por usuario durante el 2024)  
**Paso 5:** Visualización de distribuciones (uso y clientes) y outliers (Visualización de Distribuciones, Identificación de Outliers)  
**Paso 6:** Segmentación de Clientes (Por Uso, Por Edad, Visualización)  
**Paso 7:** Insight Ejecutivo para Stakeholders  
**Problemas detectados en los datos**
En el data set users la columna city tiene un 11.73% de nulos y churn_date tiene un 88.35% de nulos pero esto se debe a que como es la fecha de cancelación se asume que dichos nulos corresponden a usuarios activos que no han cancelado el servicio. La columna age presentaba valores inválidos que fueron descartados, así como la columna city donde encontramos valores desconocidos que también fueron descartados. En reg_date 40 fechas corresponden al 2026 por lo que fueron descartadas del análisis  
En el data set de usage la columna "duration" tiene el 55.2% de nulos, pero se debe a que corresponde a mensajes de texto que no consumen minutos y "length" tiene el 44.7% de nulos, se debe a que corresponde a llamadas que no tienen longitud por lo que se dejan intactas  
"date" tiene el 0.125% de nulos por lo bajo que es, se ignora y deja como nulos  
Para cantidad de mensajes, cantidad de llamadas y cantidad de minutos por llamada hay valores que pueden considerarse como outliers por estar estadísticamente fuera del rango más alto pero desde la lógica del negocio son valores que se pueden presentar dada la naturaleza de los campos  
🔍 **Segmentos por Edad**  
El segmento con mayor cantidad de usuarios es el adulto con edades entre 31 y 59 años seguido del segmento de adultos mayores y el que menos usuarios tiene es el segmento de jóvenes menores de 30 años
📊 **Segmentos por Nivel de Uso**
La mayoría de los usuarios tienen un nivel de Uso Medio seguido por los usuarios de de Bajo Uso y muy pocos de Alto Uso  
➡️ **Esto sugiere que:**  
El segmento de jóvenes es un mercado potencial que podría crecer ya que al parecer no está siendo bien atendido  
Los usuarios del segmento de uso medio están contentos con el plan tarifario que tienen pero representan una oportunidad de negocio para ConnectaTel  
💡 **Recomendaciones**  
Se deberán implementar y promover planes más atractivos para captar más usuarios del segmento de jóvenes  
Hacer campañas en medios digitales en donde los jóvenes tienen más acceso y puedan contratar más fácilmente los planes y productos  
Diseñar programas de fidelidad y retención de usuarios para el segmento más grande que es el de adultos, así como atención personalizada  
Para el segmento de adultos mayores, diseñar también programas de lealtad y mejorar la experiencia de uso de los dispositivos, la adquisición de planes, etc.  
Diseñar e implementar una estrategia para promover planes más atractivos para que los usuarios del segmento de uso medio pasen a uso alto en donde se pueda cobrar más por dichos planes  
Analizar si el segmento de bajo uso puede caer en la pérdida de usuarios y de ser así analizar la posibilidad de crear planes alternativos que ayuden a retener a dichos clientes y por qué no a subir de nivel al medio  

**Ejecución del Notebook:** Ingresar a Google Colab, abrir archivo: "S7 Project-ConnectaTel.ipynb", <Ejecutar todo>
Los Data Sets arriba mencionados ya fueron cargados previamente también en Google Colab y la ruta de acceso ya fue cambiada para su ejecución
