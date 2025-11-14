# Guía completa documentada.
Primero deberás abrir tu amazon web service. 
Debes tener la instancia ya abierta. Es decir, con el entorno virtual activado. 
___
Continuamente subirás tu aplicación en github para tener el repositorio publication y sea fácil copiarlo.
___
En la máquina virtual creas una carpeta en 
```bash
home/ubuntu/nombre_de_tu_app
```
De esa manera, haces git clone dentro de la app.
y te debe aparecer tu application. Como el html o la base de datos o el node. 
___
Descarga todo lo que tu proyecto pueda necesitar. Si haz creado tu instancia desde una AMI, solo ten asegurado que todo lo que necesitas para tu proyecto este allí.
___
Descarga las dependencias de tu proyecto con npm install. Y si todo está configurado, incluyendo tu .env, entonces debería poder hacerse npm start. Debería correr tu proyecto.
___
Si vas a postman, y colocas tu ip pública, junto con el puerto configurado para poder acceder a request te aparecerá una cola eterna y un tiempo eterno. Esto se debe a que no hemos configurado seguridad todavía. 
Para configurar nuestra instancia, nos vamos a nuestra instancia (XD), desde allí nos aparecerá algo como esto:

![[instancia_aws.png]]Nos vamos a seguridad.
![[seguridad_en_instancia.png]]
Aplastamos el boton de launch wizard.
![[reglas_de_entrada1.png]]Vete a reglas de entradas, y coloca editar reglas de entrada. 
![[reglas_de_entrada_agregar.png]]Agregamos regla. Colocamos nuestro puerto, en mi caso 3000. Esto dependiendo de dónde está escuchando tu aplicación. Luego colocamos el 0.0.0.0/0 que significa que cualquier persona puede entrar a esta aplicación. 
Finalmente,  guardar reglas. 
De esta manera, podrás hacer tus CRUD en tu base de datos con la ip pública. Recuerda, que hay muchos métodos y tienes que investigar más. Por ejemplo: en el 0.0.0.0/0 no deberíamos colocar cualquier persona, se debe estudiar los protocolos.