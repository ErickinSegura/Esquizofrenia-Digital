Links: [[Multiagentes]]

##### 1. Elige y describe un fenómeno o problema de tu preferencia en el que participen dos o más agentes del mismo tipo.

El sistema consiste en una red de repartidores que reciben y entregan pedidos de comida de diferentes restaurantes a los clientes. Los repartidores deben coordinar la recogida de pedidos, optimizar rutas y garantizar entregas rápidas, mientras el sistema debe asignar pedidos de manera eficiente considerando ubicación, tiempo y carga de trabajo.

##### 2. Describe tanto los elementos PEAS como las acciones y percepciones de todos los agentes involucrados en el modelo.

| Performance                                  | Environment            | Actuators                      | Sensors                                   |
| -------------------------------------------- | ---------------------- | ------------------------------ | ----------------------------------------- |
| Tiempo de entrega                            | Calles y tráfico       | Vehículo (moto/bicicleta/auto) | GPS                                       |
| Número de pedidos completados                | Restaurantes           | App móvil para interacción     | App móvil (recibe pedidos/notificaciones) |
| Calificación del cliente                     | Clientes               | Sistema de comunicación        |                                           |
| Eficiencia en consumo de combustible/energía | Condiciones climáticas |                                |                                           |
|                                              | Otros repartidores     |                                |                                           |

##### 3. ¿Cuál es la naturaleza (tipo) del entorno? Justifica tu respuesta considerando si el entorno es dinámico, accesible, continuo o discreto, etc.

- Dinámico: Cambia constantemente (tráfico, nuevos pedidos, clima).
- Parcialmente observable: Los repartidores no pueden ver todo el entorno.
- Continuo: Variables como posición y tiempo son continuas.
- Estocástico: Hay incertidumbre en tiempos de viaje y preparación.
- Multi-agente: Múltiples repartidores, restaurantes y clientes interactuando.
<div class="page-break" style="page-break-before: always;"></div>

##### 4. ¿Qué tipo de agente es? Explica si es reactivo, deliberativo, benévolo o interesado.

Los repartidores son agentes deliberativos e interesados, deliberativos porque planifican rutas y gestionan múltiples pedidos, mientras que son interesados porque buscan maximizar sus propias ganancias mientras contribuyen al sistema. Utilizan un modelo híbrido que combina reactividad (respuesta a nuevos pedidos) con deliberación (planificación de rutas).

##### 5. Dibuja un diagrama del agente (o agentes) y su interacción con el entorno.

![[Pasted image 20241118032438.png]]
<div class="page-break" style="page-break-before: always;"></div>

##### 6. Explica cómo los agentes se comunican entre sí. ¿Estos utilizan un lenguaje estándar (como KQML o FIPA ACL)? Proporciona ejemplos concretos de performativos como informar o solicitar

Los agentes utilizan FIPA-ACL para la comunicación estandarizada. Ejemplos:
```
(INFORM
  :sender Repartidor1
  :receiver SistemaCentral
  :content "Pedido #123 entregado satisfactoriamente"
  :language FIPA-SL)

(REQUEST
  :sender SistemaCentral
  :receiver Repartidor2
  :content "Nuevo pedido disponible en Restaurante-A para Cliente-B"
  :language FIPA-SL)

(PROPOSE
  :sender Repartidor3
  :receiver SistemaCentral
  :content "Disponible para pedidos en zona norte"
  :language FIPA-SL)
```

##### 7. Detalla cómo se implementan los protocolos de reparto o la Resolución Cooperativa Distribuida de Problemas (CDPS) en el caso de estudio elegido.

a) Asignación de pedidos:

Se utilza el Protocolo de Red de Contactos para asignación de pedidos. Los repartidores pueden aceptar pedidos según su ubicación y capacidad. Sistema de puntuación basado en rendimiento histórico del repartidor y las opiniones del cliente.

b) Optimización de rutas:

Se utilizan algoritmos de planificación de rutas, algo muy importante es considerar la posibilidad de realizar varios pedidos por ruta, además que tenga una adaptación dinámica según las condiciones del tráfico por la ruta.
<div class="page-break" style="page-break-before: always;"></div>

c) Coordinación de recogidas:

Se utilza una sincronización con tiempos de preparación de restaurantes con la llegada a recolección de los repartidores de los pedidodos, además de una gestión de colas de recogida, así pudiendo tener un sistema de priorización basada en urgencia a los pedidos que ya tengan mayor tiempo de espera y tipo de pedido.

d) Gestión de incidencias:

Se utilza protocolo de reasignación de repartidor en caso de retrasos con la entrega, además de contar con un sistema de respaldo para pedidos problemáticos y busqueda de solución de los mismos, y de manera muy importante tener comunicación automática con clientes.

e) Mecanismos de incentivos:

Se utilizan bonificaciones por zonas de alta demanda además de recompensas por cumplimiento de objetivos para los repartidores así mejorando su eficiencia y aceptación de pedidos. Por el contrario penalizaciones por rechazos excesivos y bajas reseñas por parte de los clientes.