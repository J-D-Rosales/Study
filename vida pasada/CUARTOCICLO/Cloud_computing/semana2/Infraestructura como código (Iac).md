>[!note] Definición
>Capacidad de aprovisionar y respaldar  su infraestructura de computación a través de código en lugar de procesos y configuraciones manuales.

La infraestructura como código le permite definir el estado deseado de su infraestructura sin incluir todos los pasos para llegar a ese estado.
Es usado en gran medida por las empresas para controlar los costos y responder con tiempo a oportunidades.
## Beneficios de Infraestructura cómo código
El uso más común de la IaC es la creación, prueba e implementación de aplicaciones en el campo del desarrollo de software. Tradicionalmente era tedioso y con mucho código, pero ahora es más fácil administrarlo de manera eficiente. 
### Duplicación de entorno
Si quieres duplicar tu entorno, es simple, entonces, al escalada en otras áreas es rápida y fácil.
### Reducir los errores de configuración
Los humanos tienden a equivocarse en las configuraciones.
Si se producen errores debido a las actualizaciones del código de la IaC, puede solucionar rápidamente la situación trasladando el código base a los últimos archivos de configuración estables conocidos. También es posible revertir los entornos que utilizan versiones anteriores de los archivos de configuración de IaC por otros motivos, como la implementación de versiones anteriores de las aplicaciones.
### **Itere en entornos de prácticas recomendadas**

El control del código fuente permite a los desarrolladores de software crear entornos y ramificarlos fácilmente. Por ejemplo, imagine que una aplicación creció hasta incluir un módulo opcional de machine learning. Un desarrollador podría ramificar la IaC de la aplicación para iniciar, usar y detener una [instancia Trn1 de Amazon Elastic Compute Cloud (Amazon EC2)](https://aws.amazon.com/ec2/instance-types/trn1/) de alto rendimiento. Pueden configurar la región de implementación como dependiente de la región de implementación de la aplicación.
## Funcionamiento de IaC
la infraestructura como código (IaC) describe la arquitectura de un sistema y su funcionamiento. Una arquitectura de infraestructura contiene recursos como servidores, redes, sistemas operativos y almacenamiento. La IaC controla los recursos virtualizados al tratar los archivos de configuración como archivos de código fuente
Los archivos de la IaC se incluyen como parte de la base de código más amplia.
### Enfoques de la IaC
Los dos enfoques son 
#### Declarativa
El desarrollador describe los recursos que necesita en un código de infraestructura. El desarrollador debe saber que componentes y configuraciones necesita.
#### Imperativa.
Describe **los pasos** para configurar los recursos y llegar al sistema final de ejecución. Es desafiante, no obstante, es crítico si tu arquitectura es compleja.

## El papel de la Iac en DevOps
DevOps es el proceso de mejorar la colaboración entre los equipos de desarrollo de software y operaciones de TI.
La idea de esta integración es tener ciclos de lanzamiento extremadamente rápido.
Puede integrar la infraestructura como código (IaC) en las canalizaciones de integración y entrega continuas (CI/CD). Los principales propósitos son:
- Configurar rápidamente entornos completos, desde el desarrollo hasta la producción
- Ayudar a garantizar configuraciones reproducibles de manera uniforme entre entornos
- Integrar sistemas de forma integral con los proveedores de servicios en la nube y ampliar o reducir los recursos de infraestructura de manera eficiente en función de la demanda
## Publicidad de Aws
Los servicios en resumen son:
- Con [AWS Cloud Development Kit](https://aws.amazon.com/cdk/) (AWS CDK), los desarrolladores pueden definir los recursos de las aplicaciones en la nube con lenguajes de programación conocidos y herramientas de configuración interactivas, todo en el IDE. Esto evita la necesidad de aprender nuevos lenguajes y herramientas para manipular los recursos de la nube.
- Con [AWS CloudFormation](https://aws.amazon.com/cloudformation/), los desarrolladores pueden crear y escalar más allá de la infraestructura de AWS. Los desarrolladores pueden usar la IaC para definir y administrar los recursos en la nube publicados en el registro de CloudFormation, la comunidad de desarrolladores y las bibliotecas internas.
- Si desea obtener un control de origen completamente administrado de la IaC y de todo el código de su aplicación, [AWS CodeCommit](https://aws.amazon.com/codecommit/) es un servicio seguro y escalable para alojar sus repositorios Git privados.
