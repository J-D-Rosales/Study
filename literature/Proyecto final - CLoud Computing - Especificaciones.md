created: 2025-10-26
**source:** [[2. Proyecto Final (Entrega Semana 15) V4.00 (1).pdf]]
**tags:** #proyecto
## Resumen 
Implementar un Sistema de Gestión de Pedidos

Las especificaciones del proyecto son:
- Diagrama de arquitectura de solución
- Frontend (Página web de dodne se hace el workflow)
- Backend (Gestión de los pedidos)
- Arquitectura: Multitenancy, Serverless, Basada en eventos
Existe una guía de la arquitectura en el video de taco bell
https://www.youtube.com/watch?v=sezX7CSbXTg 

La página web atiende de la siguiente manera:
- Aplicación se ordena
- Restaurante recibe el pedido dónde se atiende de acuerdo al orden de llegada
- Un cocinero toma el pedido y cocina
- Un despachador coloca la comida en los envases
- Un repartidor la lleva al cliente
- El cliente recibe la comida
La página web debe mostrar en cada momento el estado en dónde se encuentra el pedido.
Servicos de aws que se deben usar:
- Amplify
- Api Gateway
- EventBridge
- Step Functions
- Lambda
- DynamoDB
- S3
Es un trabajo en dónde se debe investigar cómo usar esos servicios
Nuestro proyecto es 6.200 millas[https://www.200millas.pe/]

Los entregables son el informe completo con el codigo fuente. Una presentación de ppt en dónde de manera sumisa se detalle lo que se realizó.

MI idea es el delivery da un ipnut, y esa lógica se extrapooal como un input para el step function y que se pueda realizar adecuadamente dependiendo al input que es lo que se debe hacer, cambiando el estado naturalmente. 

# Notas para el step function

1)  EL pedido trigerea al step fnction que manda al sqs se manda solo el id:
2) En base a un trigereo de la pagina web se popea el sqs el id del sqs (Tipo standard), 
3) EL evnet brignde al ver un cambio en el lambda, (solo apra el primero o para el delibery.) el lambda function se manda al event bridge que manda al step funcitons que cambia el historial de pedidos. , 
4) En base al trigger de las funciones, es que se manda al step funcitons para poder camiar el historial.
5) En la fase del empaquetado se envia al sqs, la pagina web le manda al otra vez, donde el event bridge al escuchar el lambda popea el sqs, y se manda al step funcions par aque pase al siguiente estado.
6) SE usan choices para determinar la ramificación que se necesita.

## Referencias a notas permanentes o etc
[[literature/Taco Bell Order Middleware - Enabling Delivery Orders at Massive Scale|Taco Bell Order Middleware - Enabling Delivery Orders at Massive Scale]]
