# 📄 Informe Técnico del Taller

## 🔖 Nombre del Taller

**Taller 1 - Modelado de Procesos con BPMN**

## 👥 Integrantes del equipo

- Isabela Díaz Acosta
- Sebastián Sánchez Sandoval
- Samuel Esteban López Huertas

## 🧠 Descripción general del trabajo

El objetivo del taller fue modelar procesos de negocio utilizando la notación BPMN, partiendo del caso base de la Clínica Salud Viva y aplicando los conocimientos adquiridos a un proceso real del cliente.

Durante el desarrollo del trabajo se identificaron eventos, actividades, decisiones, actores involucrados y puntos críticos del flujo, con el fin de representar los procesos de manera clara, estructurada y comprensible tanto para usuarios técnicos como de negocio.

## 🔧 Proceso de desarrollo

El equipo inició con el análisis del caso base de la Clínica Salud Viva, identificando el flujo del proceso de agendamiento de citas médicas y los actores involucrados. Se modeló el proceso utilizando draw.io, organizando el flujo de izquierda a derecha y separando los roles mediante lanes para mejorar la claridad.

Posteriormente, se revisó el diagrama para asegurar el uso correcto de eventos, actividades y gateways, eliminando ambigüedades y manteniendo un nivel adecuado de detalle.

Finalmente, se aplicó la misma metodología al proceso del cliente real (proceso de cotización y venta), incorporando decisiones adicionales, más actores y validaciones propias del contexto empresarial.

## 🧩 Análisis del modelo propuesto

### 🔹 Caso base: Clínica Salud Viva

#### Estructura del modelo

El modelo se compone de:

- **Evento de inicio** (paciente inicia el proceso).
- **Actividades del paciente**: ingresar al sistema, seleccionar especialidad, médico y fecha.
- **Actividad del sistema**: validar disponibilidad.
- **Gateway exclusivo**: ¿cita disponible?
- **Actividades del sistema**: registrar cita y mostrar mensaje.
- **Eventos de fin** según disponibilidad.

#### Representación del proceso

El modelo refleja el proceso real de agendamiento digital, donde el paciente interactúa con el sistema para reservar una cita médica y recibe retroalimentación inmediata según la disponibilidad.

#### Supuestos

- El sistema funciona correctamente.
- La base de datos está actualizada.
- El paciente ingresa información válida.

## 📈 Diagrama final entregado Caso base: Clínica Salud Viva

<img width="1738" height="850" alt="image" src="https://github.com/user-attachments/assets/bfac1248-6dd4-4cfe-b082-e783ae687690" />
[Ver diagrama en Miro](https://miro.com/welcomeonboard/SUJ0WUVJaGY5bEJUd01pb2ZRWGZrL3ZlRGhadlJUV0hvNzJJcEN5aWJETXM2RUs3OGtRL241a09HMlVXbGlTT0pid29mcEhaSlVvVWhDVTl6UitHRW1nTjdyT3h2ZytVTmFiZEtSdjFDMlZPcXh2bmk2YWdzS1lTbXpBVUdOZEhQdGo1ZEV3bUdPQWRZUHQzSGl6V2NBPT0hdjE=?share_link_id=10153609605)


### 🔹 Cliente real: Proceso de cotización y venta

#### Estructura del modelo

El modelo incluye:

- **Evento de inicio**: cliente solicita cotización.
- **Actividades del asesor comercial**: registrar solicitud y generar cotización.
- **Validación del sistema**: verificación de inventario.
- **Gateway**: disponibilidad de stock.
- **Actividad del sistema**: envío de cotización.
- **Decisión del cliente**: aceptación o rechazo.
- **Actividades del sistema**: generación de orden de venta, descuento de inventario y facturación.
- **Actividad del área contable**: registro del movimiento contable.
- **Evento final**: venta registrada y facturada.

#### Representación de las necesidades del cliente

El modelo muestra el flujo completo desde la solicitud de cotización hasta el registro contable de la venta, reflejando la interacción entre áreas comerciales, operativas y contables.

#### Supuestos

- El inventario del sistema está actualizado.
- El cliente responde oportunamente a la cotización.
- Los procesos contables están automatizados.

## 📈 Diagrama final entregado Cliente real: Proceso de cotización y venta

*<img width="1774" height="1143" alt="image" src="https://github.com/user-attachments/assets/72453266-3625-4419-94ed-5a3ecfae2329" />
[Ver diagrama en Miro](https://miro.com/welcomeonboard/SFZGYVI3RldmdGo5T0pxYTArYkNUVVFXTkRXelpkclM1cFBsK3dOZ0tvS0xpWDhPZzJ3OENab3ZlTzh1SVNxbVVidTN1V3Q0WlFQNkVQQ1FhQm0xWkdnTjdyT3h2ZytVTmFiZEtSdjFDMlV6V2Z5RURCM01vcE9oS0hlUkhZV1p0R2lncW1vRmFBVnlLcVJzTmdFdlNRPT0hdjE=?share_link_id=600125739103)


## 📋 Tabla de actores, entidades o componentes

| Nombre del elemento | Tipo | Descripción | Responsable |
|---------------------|------|-------------|-------------|
| Paciente | Actor | Usuario que agenda una cita médica | Cliente |
| Sistema de citas | Sistema | Valida disponibilidad y registra citas | Organización |
| Cliente | Actor | Persona que solicita una cotización | Empresa cliente |
| Asesor comercial | Actor | Gestiona solicitudes y genera cotizaciones | Área comercial |
| Sistema | Sistema | Verifica inventario, genera órdenes y facturas | Organización |
| Área contable | Actor | Registra el movimiento contable de la venta | Área financiera |

## 🔍 Investigación complementaria

**Tema investigado:**

Buenas prácticas BPMN y ejemplos en la industria

**Resumen:**

Durante el modelado se aplicaron buenas prácticas BPMN para garantizar claridad y comprensión. Se mantuvo un flujo lógico de izquierda a derecha, se utilizaron correctamente eventos de inicio y fin, y se emplearon gateways exclusivos para representar decisiones como disponibilidad de citas, stock y aceptación de cotizaciones. Asimismo, los roles se separaron mediante lanes para facilitar la identificación de responsabilidades y detectar posibles cuellos de botella.

El uso de BPMN es común en múltiples industrias. En el sector salud se utiliza para la gestión de citas médicas, permitiendo optimizar recursos y reducir tiempos de espera. En el sector bancario se emplea para procesos de aprobación de créditos, mejorando la trazabilidad y reduciendo errores. En el comercio electrónico, empresas como Amazon utilizan BPMN para optimizar el procesamiento de pedidos, la gestión de inventarios y la facturación, mejorando la eficiencia operativa y la experiencia del cliente.

Un caso real del sector salud evidenció que la implementación de BPMN en el proceso de admisión hospitalaria permitió reducir tiempos de atención, disminuir errores en registros y mejorar la experiencia del paciente, demostrando su valor como herramienta para la mejora continua y la automatización de procesos.

## 📊 Comparación entre el caso base y el cliente real

| Aspecto | Clínica Salud Viva | Cliente Real |
|---------|-------------------|--------------|
| Tipo de proceso | Agendamiento de citas | Cotización y venta |
| Actores | Paciente, Sistema | Cliente, Asesor, Sistema, Área contable |
| Decisiones | Disponibilidad de cita | Stock disponible y aceptación de cotización |
| Resultado final | Cita registrada | Venta facturada |
| Complejidad | Baja | Alta |

## 📚 Referencias

- Object Management Group. Business Process Model and Notation (BPMN) 2.0 Specification.
- OMG. BPMN Official Documentation: https://www.omg.org/spec/BPMN/
- Ejemplos de aplicación BPMN en sectores salud, comercio electrónico y financiero.

---

*Este documento hace parte de la entrega del Taller 1 del curso Arquitectura Empresarial - Universidad de La Sabana.*
