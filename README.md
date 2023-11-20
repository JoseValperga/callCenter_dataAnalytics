# PROYECTO INTEGRADOR CALL CENTER ANONYMOUS BANK
Integrantes
Gisele Salinas
Nilce Daparo
German Huber
Jose Valperga

## PRESENTACIÓN
De un call center se espera según la Corporación Financiera Internacional del Banco Mundial (Documento Measuring Call Center Performance Global Best Practices)
-	que el 80% de las llamadas sean atendidas en menos de 20” (Nivel de Servicio). Para esto analizamos las llamadas de un año completo.
-	que la tasa de abandono no supere el 8% de las llamadas
-	que la tasa promedio de asistencia para servicios financieros y empresarios sea de 282 segundos.
Para explicar mejor cómo funciona el call center, la persona llama y atiende el denominado VRU (Voice Response Unit) que es el Bot que oficia de contestador automático. Allí se le pide a la persona que se identifique de alguna manera (Customer ID) y que seleccione el servicio que necesita (“Presione 1 para…”).  Hecho esto, normalmente ingresa en cola de espera (“Todos nuestros representantes están ocupados…”), se escucha algún tema musical (en los 90 “Para Elisa” de Beethoven era un clásico) hasta ser atendida por un operador.
Nuestra tarea consiste en analizar el Call Center del Banco “Anonymous Bank”, en Israel. El dataset contiene las llamadas registradas durante 12 meses (desde el 01/01/99 hasta el 31/12/99.
El call center está conformado por:
• 8 posiciones de operadores para recibir llamadas de clientes actuales y potenciales.
• 1 posición de supervisor
• 5 posiciones de operadores para llamadas para soporte de internet home banking
En cuanto a los horarios de atención, y por tratarse de un banco en Israel, se debe tener en cuenta el respeto del sabath, lo que marca que el Domingo sea el primer día laborable, de la semana, y el viernes, el último.
Durante los días de semana (Domingos a Jueves), el call center opera desde las 7:00 de la mañana hasta la medianoche. Cierra a las 14 hs del Viernes y reabre a las 20:00 del Sábado. El servicio automático (VRU) opera los 7 días de la semana, 24 horas al día (7x24).
Aunque existen 3 niveles de prioridad para los clientes, la política del banco establece que las prioridades marcadas como 0 (Clientes Potenciales) y 1 (Clientes Regulares) sean tratadas indistintamente con prioridad 1 (Cliente Regular). Existe también la prioridad 2 para los Clientes Prioritarios. Para el análisis vamos a adoptar esos 2 niveles de tratamiento, Prioridad 1 para potenciales y regulares y 2 para prioritarios.
Finalmente, existen tres posibles finalizaciones para cada llamada: cliente abandonó la llamada, cliente fue atendido por un operador, se ignora lo que sucedió con dicha llamada. Al ser muy escasas estas últimas, no las hemos tomado en cuenta en el análisis.

## DATOS ANUALES

Estamos frente a un banco con unos 13.000 clientes que realizan más de 440 mil llamadas al año, donde prácticamente el 20% de las mismas son abandonadas por parte de quien llama. Un poco más del 5% abandona en el contestador automático y el resto, un poco más del 14%, lo hace en la cola de espera. INSIGHT: Tenemos un 18% de llamadas repetidas, que se contrasta con el 20% de abandonos. Al estar ambas calculadas sobre el total de llamadas, podemos suponer que el 90% de los que abandona llama, por lo menos, una segunda vez.
Con estos datos advertimos que hay una alta tasa de abandonos, la que supera ampliamente el máximo del 8% esperado, y el hecho de que estén abandonando en cola de espera nos indica que la misma es muy larga y puede estar excediendo los 20” 

## ATENCION AL CLIENTE

### El call center posee casi 6.000 clientes prioritarios y tiene como política no hacerlos esperar más de 90 segundos. Mirando un poco más en detalle, por motivo del llamado, vemos que el 68% de los llamados solicita un servicio regular del banco (Actividad Regular) y un 15% es un cliente potencial solicitando información. El motivo de bajas consultas de home banking se debe a que, debido al año del dataset, sea muy reciente su implementación y pocos clientes tienen acceso a internet.
### Observando las llamadas anuales por mes y prioridad, vemos que mensualmente entre un 5% y un 7% del total anual de llamados se los llevan los clientes no prioritarios, y entre un 2% y un 3% se los llevan los clientes prioritarios. Para los días de la semana, vemos la misma relación. INSIGHT: Los clientes No Prioritarios llaman más del doble de los clientes Prioritarios. 69% contra 31%

## LLAMADAS Y ABANDONOS EN GENERAL

### Una vez en la cola de espera, vemos que prácticamente el 15% de los clientes abandona el llamado en esa etapa, siendo el 80 restante (recordar que en el VRU quedó el 5%) atendidos por un agente del call center. Esto sobre todo ocurre en los horarios pico lo cual nos podría estar indicando que faltan operadores en ciertas franjas horarias. Observamos también que el pico de llamadas ocurre a las 10 de la mañana.
### Entrando en detalle, el 55% de los abandonos llamó por una actividad regular, mientras que el 32% lo hizo por una consulta de cliente potencial. Recordar que al 15% de los llamados los hizo un cliente potencial (gráfico de torta de la hoja anterior), y se llevan el 32% de los abandonos.


## ESPERAS Y ABANDONOS POR FRANJA HORARIA
### Entramos ahora en detalle sobre lo que ocurre en la cola de espera. Si observamos los tiempos de espera que se generan, vemos dos picos: uno en la franja de las 10 de la mañana (108 segundos) y el restante en la franja de las 3 de la tarde (129 segundos). Durante dichos picos, el tiempo de espera promedio para el cliente prioritario es de 88 segundos, lo que indica la política de atenderlos antes de los 90 segundos se respeta, mientras que para el resto de los clientes el tiempo de espera promedio es de 110 segundos 
### En dichas franjas se produce la mayor cantidad de abandonos (ver gráfica de al lado): a las 10 de la mañana se produce el 7% del total diario de abandonos de cliente regulares, y el 5% de los prioritarios (12% total), mientras que entre las 3 y las 4 de la tarde ese porcentaje refleja el 20%. INSIGHT: Tenemos dos cuellos de botella, uno en la franja de las 10 de la mañana y otro en la franja de las 3 a las 4 de la tarde, donde se generan los mayores tiempos de espera (108 segundos y 129 segundos respectivamente) y una tasa total de abandonos del 32%.

### ¿Cuánto tiempo esperan los clientes? El 23% espera hasta 15 segundos y el 21% más de 2 minutos (extremos de la gráfica). Un 14% espera hasta 30 segundos. Observando en detalle, la composición de los abandonos prácticamente respeta la composición de los llamados, ya que abandona el doble de clientes regulares respecto a los prioritarios. INSIGHT: La política de atender antes de los 90 segundos a los clientes prioritarios debe ser revisada.
### El promedio del tiempo de atención del call center es de 191 segundos (ver línea del promedio del primer gráfico) y observamos que a los clientes prioritarios se les brinda durante toda la jornada un tiempo de atención mayor o cercano al promedio. El tiempo promedio de atención para los clientes prioritarios es de 211 segundos, mientras que para el resto de los clientes es de 182 segundos. También observamos dos picos en los tiempos de atención, tanto a los clientes regulares como a los clientes prioritarios: unos a las 9 de la mañana y el otro a las 3 de la tarde. 
### El call center tiene el más 92% de sus agentes atendiendo en los horarios pico de las 10 de la mañana y las 3 de la tarde. En el gráfico observamos cómo se distribuyen las llamadas y operadores a lo largo del día y notamos que la máxima cantidad de operadores no coincide con los horarios pico, pues se encuentra presente en las franjas que toman la 1 de la tarde y las 2 de la tarde. La máxima cantidad de operadores comienza a atender cuando las llamadas han bajado (después del pico de las 11 de la mañana) y se reduce antes del pico de las 3 de la tarde.

## ANALISIS DE PARAMETROS EN FORMA CONJUNTA
### El call center cuenta con 52 operadores en total, que se distribuyen a lo largo del año, pero por turno operan 14 personas simultáneamente, de acuerdo a lo informado al comienzo.
### Consolidando ahora la información de tiempos de atención, tiempos de espera y porcentaje de abandonos, observamos claramente que los picos de espera se producen a las 10 de la mañana, donde la baja en el tiempo de atención no es suficiente para afrontar el pico de llamadas, y a las tres de la tarde, coincidiendo este último con el mayor tiempo de atención brindado en ese horario y la baja en la cantidad de operadores, a pesar de que los llamados ya han disminuido. Durante ambos picos de espera se disparan los abandonos 
### En la siguiente gráfica podemos observar la cantidad de operadores, la cantidad de llamadas y la cantidad de abandonos, donde se observa el pico de abandonos ante la baja en la cantidad de personal que atienda las llamadas.

### INSIGHT: La cantidad de llamadas atendidas durante los cuellos de botella de las 10 de la mañana y las 3 de la tarde podrían mejorar aumentando la cantidad de operadores antes de las 10 de la mañana y manteniéndola hasta después de las 3 de la tarde, visto que el tiempo de atención es bajo en comparación con el estándar internacional.

## CONCLUSIONES
### •	El 44% de las llamadas es atendida antes de los 20 segundos de cola de espera, mientras que el estándar internacional marca un mínimo del 80%, por lo que no se cumple.
### •	La tasa de abandono es del 19,89%, mientras que el estándar internacional marca un máximo del 8% y un mínimo del 5%, los que no se cumplen.
### •	El tiempo de asistencia promedio es de 191 segundos, con picos de 243 segundos para los clientes prioritarios, mientras que el estándar internacional marca un promedio de 282 segundos. Si bien es cierto que cumple con el parámetro, sería necesario evaluar si no es demasiado bajo.
### •	Se debe reevaluar la política de atender antes de los 90 segundos a los clientes prioritarios, dado que transcurrido ese tiempo ya ha abandonado más del 70% de los clientes.
### •	Por último, se hace indispensable incrementar la cantidad de operadores y mantenerlos en sus puestos desde antes de las 10 de la mañana y hasta después de las 3 de la tarde, y así suavizar los cuellos de botella y bajar la tasa de abandono.

