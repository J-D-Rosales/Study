Resumende lsa notas para fleeting notes.

Aws well architecture es una ayuda para que los arquitectos de la nube puedan construir su arquitecturas de manera fiable, bajo 6 pilares de la buena arquitectura. Mejor aruitectura, mejor creación de seguridad, carga de trabajo, etc. -> diseño escalable.

¿Cuales son los 6 pilares de Aws Well-Arquitectural?
Excelencia operativa
- seguridad
- fiabilidad
- eficiencia de rendimiento
- optimización de costos
- sostenibilidad

¿Qué incluye Aws Well-architecture Framework? 
Inclurye enfoques de dominio específico. Laboratorios específicos, laboratorios prácticos y AWS Well-architecture tool. Esto ayuda a monitoriar las cargas de trabajo, indentificar los problemas de alto riesgo y registrar las mejoras.
Copia uy pega es esto, que feo.

![[PIlares de AWS Well-architected.png]]
Análisis de los 6 pilares de AWS WA
## Excelencia operativa
Se concentra en mejorar los procesos operativos , la automatización de los sistemas y el monitoreo de las aplicaciones. La idea es mejroar constantemento lso procesos hechos por el sistema. 
Otra parte que se abduce de allí es la definició de estándares para administrar las operaciones diarias. y la respuesta a eventos junto con la automatización decambios
## Pilar de seguridad
Se basa en la seguridad de la aplicacón u de los usuarios, proteger la información y los sistemas.
Se tiene en cuenta la confidencialidad, el manejo correcto de los datos (integradad de la data), los permisos dados a los usarios y controles para detectar temas de seguridad.

## Pilar de la eficacia de rendimiento.
Se centra en asignar correctamente los recursos dado el sistema. En pocas palabras un buen escalamiento. Supervisar el rendimiento y el mantenimiento de la eficacia mientras se escala más la solución (a medida que laempresa crece)

## Pilar de optimización de costos.
Se centra en optimizar los costos, no hacer gastos inecesarios. 
Entre lo escencial es escojer bien los recursos para no dañar excesivamente los gastos de la empresa, escoger lo ideal y adecuado.

## Pilar de fiabilidad
SE centra en cómo recuperarse rápidamente ante un problema en las funciones o el sistema y en las cargas de trabajo que realizan las funciones previstas , tener sitemas distrbuidos, planificación de recuperación etc. Esto conlelva a una adaptación constante a los requisitos d ela empresa, y aún más al cambio necesario. 


## PIlar de sostenibilidad

No dañar al ambiente, con los recursos innecesarios , comprensión dle impacto en la uve de la saplicaciones que vamos a desarrollar etc. MInimizar el daño, maximizar ganancias.

¿Qué son los enfoces en AWS well-architecture?
amplían la orientación que brinda aws para abordar temas especíicos o tecnológicos, como Iot, Mahcine learning, data, severless, et.c

## Enfoque de serverless
The serverless enfoque and senecario gives you a track on how to impelemnt your system or what are the best preactices to do it.

We'll discussed the most common scenario.
## restFul Microservices
This is a well architecrure to build an aplication based on restful.
![[Restful Microservice - serverless.png]]

In a simple way it suses Amazon to store your endpoints, and Aws lambda that executes one task, but it executes well. FInally it can scale as the order of growth thanks to amazon ynamoDB (based on demand of course) it is often used the NOsql.
## Web application
![[Arquitecture serverless for web application - AWS Well architecture.png]]
It's veryuseful use this.
Amaxozn cognite helps with the user autentication it gives you tthe token to atuenticate the api calls, and provides administration on user managementr.
The s3, is to store the web static page, and the storage services, such as javascript, images, etc.
The api gateway just stores your links
THe aws lambda makes a fucniton call , usually CURD operations.
Amaon Dynamo Db provides a database that sacales ellastically with your web, being a good alternative.

## Event drives architecture
These is increasing in popularity thanks to the facility and of course the scalability it has. 

It is good for:
- Comunication between microservices.
- Integration ith third part applications
- Parallel event proccesing, fanout.
FOr the vent driven architecture consits of three main parts. 
- Event sources 
- Even routes 
- Event destinations

The most ocmmon event source ar other aws resources, microservices or applications. 
FOr routing that sources, we can use evnt bridge to make the logic between the routwe and soruce event. and provide the destinations on wher to send them.

![[Architecture of Event-Driven application.png]]


___
Laboratorio
Ver la arquitectura pub/sub -> Patrón de diseño. Pub/sub es publisher suscriber.

Ver los patornes del pptm normalmente sns, el mensaje a la persona,.
UNo decide una atquitecgura basada en eventos, cuando ese evento es relevante para más de una aplicación.