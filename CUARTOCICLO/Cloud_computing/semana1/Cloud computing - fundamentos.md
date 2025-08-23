Proveedor AWS:
-> Una región es un lugar físico.

Para colocar un data center se tiene que tomar en cuenta la zona.
>[!note] Zona de disponibilidad
>En donde los datos centers están copiados en otros lugares.

AWS tiene muchos servicios. El que usaremos es EC2 Elastic compute cloud.
___
**Latencia**: La demora o tiempo que una petición llega de una petición a otra.

El modelo de servicio son.
- On premises
- Infrastructure as a Service
- Platform as a Service
- Software as a Service
Cuando tenemos On premises todo lo gestionas tú.
L a segunda forma era un poco complicada, por eso se lanza el tercero para que el usuario solo se preocupe en hacer la aplicación.
La última forma son plataformas con subscripción, en donde si pagas, te dan usuario y contraseña, y puedes usar el software.
Los ejemplos se encuentran en el ppt.
___
## Modelo de despliegue
En informática hay un concepto:
Cuando tienes un sistema en donde se cae, pero no afecta al core. Entonces el sistema no afecta a los clientes (que son normalmente el core)
**Core**: sistema centralizado que gestiona las operaciones principales de una organización
EL sistema core es el ser de la compañía (Preguntar).
### Nube Privada.
Es donde están el sistema core de la compañia. Cómo Rimac
Desventajas: Alta inversión, coste continuo de mantenimiento.
### Nube Pública
Esto es Aws, como Rimac que tienen aplicaciones, etc.  Sus páginas web, sus autoservicio. 
Aquí viene el concepto del frontend y el backend.
En la nube pública se necesita un Api.
Menor privacidad (No tan cierto)
### Nube Híbrida
Cuando la compañia tiene cosas en la nube privada y pública, se dice que son Híbrida.
### Nube comunitaria
Transferencia entrante de datos son gratis. Es decir, si alguien trae información a Aws , es gratis. 
Entonces, mientras más grande sea tu aplicación menor sea el precio por unidad. 

En aws. Tenemos AMI
Que es una plantilla, como una clase en programación orientada a objetos. EL cual tiene ya programas preinstalados.

___
**Par de claves**: 
Se deben tener dos tokens, uno en el servidor alejado, y otro que tenemos aca. Esto por razones de seguridad 