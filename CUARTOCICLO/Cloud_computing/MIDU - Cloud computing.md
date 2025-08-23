# Aws lo interesante
-> Liderazgo e importancia.
-> Amplia gama de servicios.
En el curso se aprenderá la UI de inicio.
El servicio de EC2.
Base de datos.
Cómo no quemar dinero, etc.
AWS Lambda.
S3 y AWS Cli.
Por donde continuar.
Otra cosa es instalar el cli de aws.
ACTIVAR EL MFA, el multiple factor authentication. Poruqe es un servicio muy peligroso que nos pueden hackear mucho dinero etc. Y crear un monitor con una alarma para los costes.
El cli de aws, es muy bueno para usar aws desde la terminal.
___
Al crear una web necesitas muchas cosas. Por ejemplo, hospedaje, base de datos, mailing, imágenes estáticas, transacciones, etc.
No obstante, si tu web se satura, por alguna tendencia existirá dos tipos de escalamiento.
**Escalamiento horizontal**: Es tener la misma máquina pero multiplicada. 
**Escalamiento vertical**: Sería hacer el servidor mucho más grande. Simplemente lo hacemos más grande. Ojo: También puede ser escalar para abajo.
No hay uno mejor, todo dependerá de tu situación. Por ejemplo, en el escalamiento vertical, vas a tener downtime. Pero multiplicar servidores es más complicado.
___
## EC2
Elastic cloud computing. 
Tienes la capacidad de crear una instancia. Puedes tener imágnees de distintos sistemas operativas.
Cuando entras a aws, ir a ec2. Luego crea una instancia
### Creando una instancia
Pasos:
1.- Colocar el nombre de tu instancia.
2.- Elegir el sistema operativo:
Esto es importante porque queremos saber en que sistema lo vamos a utilizar. 
Se puede crear una instancia a partir de una AMI. Es decir de una imagen. Una imagen es simplemente una instancia pero con algunos programas ya preinstalados.
3.- Elegir el tipo de instancia, que para la capa gratuita es la micro.
Al elegir el tipo de instancia, también es importante no solo el almacenamiento, los cpus y  y la memoria, sino también el rendimiento de la red.
4.- En la parte de creación de claves, es muy importante porque es una clave única que permitirá conectarte a ti al servidor. Es como un token único, donde tienes una llave y un candado, por eso es par de calves. Solo el servidor en la nube y tu computadora usando la clave pueden estar matemáticamente clickeados. 
Por temas, de aprendizaje yo crearé mi par de claves.
5.- En las configuraciones de red, tu puedes colocar el ssh desde tu ubicación ip, o desde cualquier lugar. Además, permitior el tráfico de http o https en tu instancia. Yo lo coloqué los 3. 
Un grupo de seguridad son un conjunto de reglas de firewall para controllar el tráfico de la instancia. Tanto el de entrada o el de salida y se crea grupos porque lo quieres reutilizar.
Hecho esto crea tu instancia y ya.
Consiguientemento podrás visualizar tu instancia en el apartado de instancias dónde verás información relevante. 
En nuestro caso, como queremos subir un servidor, tomaremos la IPv4 pública de la instancia.
En mi caso es: 54.152.5.4
Ahora simplemente le das a conectar y conecta. 
Ahora, hay algo interesante, porque en la parte de cliente ssh antes despues de darle al botón de conectar. Por medio de esto podrías conectarnos por medio de una terminal a aws. Para esto necesitaras el par de claves que habíamos creado en un inicio. 
Para hacerlo simplemente dirigete a la carpeta en dónde está el archivo de par de claves y ejecuta el siguiente comando. 
```bash
chmod 400 "[nombre].pem"
```
Ahora para utilizarlo, tendrías que ir a tu aws,  copiar el link en el cliente ssh. EN mi caso es:
```bash
ssh -i "par_de_claves_instancia_midu.pem" ubuntu@ec2-54-152-5-4.compute-1.amazonaws.com
```
En pocas palabras lo que hace es decir, usa esta llave para conectarte a este servidor.
Puedes hacer distintas cosas. EN pocas palabras puedes colocar un html. Puedes intalar node.js y hacer tu aplicación y verlo en el puerto público. 
Aquí dejaré como hacer un hola mundo en html.
**Haciendo un hola mundo en html con aws**:
1.- Entrar a tu terminal de la instancia con el boton de conectar. (yo lo haré con cliente ssh).
Al parecer en windows no deja hace el chmod, el cual solo funciona en linux/mac. En ese caso solo conectate con el último comando. El cual sería más que suficiente. 
Para obtener la última version de linux. solo haz este comando:
```bash
sudo apt update
```
Ahora para hacer tu hola mundo lo que debes hacer es:
```bash
mkdir prueba_html
cd prueba html
nano index.html
```
De esta manera se te abrira un editor de texto, donde podrás hacer tu html típico.
Ahora para levantar el servidor, lo que haremos es usar python.
```python
sudo python3 -m http.server 80
```
lo colocamos en el puerto 8080
Ahora si vas a las instancias y vas a esa dirección ip, encontraras tu aplicación.
Puedes hacer ahora coas con node.js etc.
# RDS
Existen muchas bases de batos. Entondes, tienes que tener en cuenta que hay más servicios de base de datos. En este caso estamos usan el relational database schema.
En este caso lo haremos en postgres. Amazon casi simepre tiene su propia forma. 
Nos vamos ya no al ec2, sino a la parte de Aurora and RDS de amazon. Dónde crearemos una base de datos.
Hay una opción que es super importante después que le des al botón de crear una base de datos. 
El cual dice *"Mostrar solo las versiones compatibles con el clúster de base de datos multi-AZ"*.
Es avalavility zone, esto permite tener mejor latencia. Pero, algo mejor, imagínate que tenemos una base de datos en estados unidos, y se destruye por un meteorito. lo que tengas con AZ tiens duplicada la base de datos pero en la misma region. En cada esquina de la región tenemos dos bases de datos. Así resguardas tu base de datos. 
Recuerda usar la capa gratuita, porque estas cosas cuestan como miércoles. 
1.- Colocamos el nombre del database. 
2.- Tu contraseña
AWS te da **dos formas** de manejar esas credenciales:
 Opción 1: **Administrado en AWS Secrets Manager**
**¿Qué pasa aquí?**
- AWS genera la contraseña del usuario maestro automáticamente.    
- No la ves directamente: se guarda en un **Secret** dentro de **AWS Secrets Manager**.   
- Tú, para conectarte, tienes que usar el Secrets Manager para leer esa contraseña.    
- **Ventajas:** más seguro, rotación automática de contraseñas.
- **Desventajas:** cuesta dinero extra (porque Secrets Manager se cobra por uso).
Opción 2: **Autoadministrado**
- **¿Qué pasa aquí?**
    - Tú eliges una contraseña maestra al momento de crear la DB.    
    - Escribes y guardas esa contraseña en algún lugar seguro (ej. tu PC, un gestor de contraseñas).
- **Ventajas:** gratis y sencillo (no pagas por Secrets Manager).
- **Desventajas:** si pierdes la contraseña, no hay cómo recuperarla fácilmente (tendrías que resetear el usuario).
La configuración de la instancia no toques nada. Porque solo puedes tener dos, los más pequeño.
3.- No tocar almacenamiento, aunque si lo necesitas administrar solo tienes que cambiar el espacio.
4.- Respecto a la conectividad. Esto es, para que podamos conectar la máquina virtual que hemos creado antes, con la base de datos que estamos creando en aws. No lo vamos a hacer pero lo podrías hacer.
La nube privada, imporatante, donde tengamos los mismos servicios que nos interesan que estén jutnos.
En el caso de acceso público, lo vamos a colocar sólo porque nos queremos conectar desde la terminal. En otro caso, si desde la máquian que habeís creado antes tenga un acceso interno, no hace falta que tenga acceso público.
6.- Lo siguiente sería la zona de disponibilidad, en donde te dicen dónde están disponibles.
7.-No olvidar la autenticación por contraseña.

... Aún no hemos temrinado, porque demora bastante. Mientras tanto, veremos s3
# S3
Sirve para almacenar archivos estáticos. Vídeos, documentos, etc.
Aquí la palabra clave es el bucket que es como un cajón dónde metes cosas, mejor dicho objetos.
>[!warning] Buckets
>Al crear un nombre de un bucket, toma en cuenta que tiene que ser un nombre único. Esto es debido a que el servicio es global.

Lo bueno de S3 es que es muy barato
Lo primero que tienes que hacer, es elegir el servicio de aws. En este caso en S3, el nombre como debe de ser único, tratar que sea largo.
Yo coloque PruebaDeBucketNombreDistinto2
2.- En propiedades de los objetos hayy algo llamado ACL, eso lo que hace es permitir que otras cuentas de aws puedan usar tu bucket. Pero cómo no es tan recomendado, no lo haremos. Pero, puede ser importante.
3.- En la parte de configuración de bloqueo de acceso público para este bucket. Se va a hacer público. Pero, tomar en cuenta que aws tiene otro servicio que es cloudfront, que es un CDN, que es más conveniente según midu. La idea de clodfront es que tu tengas un bucket de s3 y por delante le coloques un cloudfront. De esta manera lo que se hace es que cloudfront va  a recuperar ese S3 y lo va a servir de la manera más cercana al usuario y automáticamente no tenemos que preocuparnos, porque tenemos seguridad, eventos, todo, en pocas palabras.
Entonces, el s3 no sería de acceso público, porque le haría cloudfront.
Entonces deberías desbutonear el Bloquear el acceso público.
4.- En la parte de control de versiones, no necesitamos realmente un control de versiones, pero se puede tener, lo cual es genial, realmente.
5.- EN la parte de Cifrado predeterminado, vamos a quietar la clave de bucket porque no es importante en este caso. El cifrado solo es para protreger los objetes. 
6.-Luego de eso creas el bucket. Después puedes crear una carpeta entrando al bucket. Solo coloca el botón de crear bucket y ya está.
Luego puedes cargar una imagen en la carpeta.
Cuando lo haya colocado la imagen verás un apartado que dice Clase de almacenamiento. Esto hay, porque en los archivos estáticos, no todos son importantes. Por ejemplo, más importante es index.html. Es así que la necesidad de acceder a este recurso va a ser diferente. Cuando más rápido quieres que sea, porque es importnate. En cambio si no es importante, puedes oclocar algo más barato. 
Ahora, la imagen ya tiene su url en tu s3. No obstnat,e si te vas a l objeto y le das al link, lo que te va a aparecer es acceso denegado.  De quí dependería de cómo quieres usarlo o hacerlo.
Ahora, para solucionarlo vamos a los permisos de tu bucket. Cuando entres allí, verás que todo está correcto, pero entenderás que los buckets necesitan una política. Es así, que necesitas tener una política de bucket. El cual, solo política es un mundo la verdad. Hay plantilla sy ejemplos de políticas. 
Aws te da la posibilidad de buscar las acciones, y saber que acciones poder añadir. 
Yo dejo este por aquí:
```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "PublicRead",
            "Effect": "Allow",
            "Principal": "*",
            "Action": [
                "s3:GetObject",
                "s3:GetObjectVersion"
            ],
            "Resource": "arn:aws:s3:::prueba-de-bucket-nombre-distinto2/*"
        }
    ]
}
```
A veces es muy bueno que te ayude chatgpt.
