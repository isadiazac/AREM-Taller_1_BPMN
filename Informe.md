# 📄 Informe Técnico del Taller

## 🔖 Nombre del Taller

**Taller 1 - Modelado de Procesos con BPMN**

## 👥 Integrantes del equipo

* Isabela Díaz Acosta
* Sebastián Sánchez Sandoval
* Samuel Esteban López Huertas

---

## 🧠 Descripción general del trabajo

El objetivo del taller fue modelar procesos de negocio utilizando la notación BPMN (Business Process Model and Notation), partiendo del caso base de la Clínica Salud Viva y aplicando los conocimientos adquiridos a un proceso real del cliente.

Durante el desarrollo del trabajo se identificaron eventos, actividades, decisiones (gateways), actores involucrados y puntos críticos del flujo, con el fin de representar los procesos de manera clara, estructurada y comprensible tanto para usuarios técnicos como de negocio.

El ejercicio permitió comprender la importancia de la estandarización en el modelado de procesos y su impacto en la trazabilidad, automatización y mejora continua dentro de una organización.

---

## 🔧 Proceso de desarrollo

El equipo inició con el análisis del caso base de la Clínica Salud Viva, identificando el flujo del proceso de agendamiento de citas médicas y los actores involucrados.

Se modeló el proceso utilizando **miro.com**, organizando el flujo de izquierda a derecha y separando los roles mediante lanes para mejorar la claridad visual y la asignación de responsabilidades.

Posteriormente, se revisó el diagrama para asegurar:

* Uso correcto de eventos de inicio y fin
* Aplicación adecuada de gateways exclusivos
* Coherencia en las actividades 
* Nivel de detalle apropiado

Finalmente, se aplicó la misma metodología al proceso del cliente real (proceso de cotización y venta basados en la empresa en la que pensamos trabajar el proyecto), incorporando decisiones adicionales, más actores y validaciones propias del contexto empresarial.

---

# 🧩 Análisis del modelo propuesto

---

## 🔹 Caso base: Clínica Salud Viva

### 📌 Estructura del modelo

El modelo se compone de:

* **Evento de inicio:** Paciente inicia el proceso de agendamiento.
* **Actividades del paciente:** Ingresar al sistema, seleccionar especialidad, médico y fecha.
* **Actividad del sistema:** Validar disponibilidad.
* **Gateway exclusivo (XOR):** ¿Cita disponible?
* **Actividades del sistema:** Registrar cita y notificar resultado.
* **Eventos de fin:** Confirmación o rechazo de la cita.

### 📌 Representación del proceso

El modelo refleja el proceso real de agendamiento digital, donde el paciente interactúa con el sistema para reservar una cita médica y recibe retroalimentación inmediata según la disponibilidad.

La estructura permite visualizar claramente el punto crítico del proceso: la validación de disponibilidad, que determina la continuidad o finalización del flujo.

### Supuestos

* El sistema funciona correctamente.
* La base de datos está actualizada.
* El paciente ingresa información válida.

### Puntos críticos identificados

* Dependencia de disponibilidad médica actualizada.
* Sincronización correcta entre plataforma y base de datos.
* Posibles fallas en notificaciones.
* Alta demanda en temporadas especiales.

---

## 📈 Diagrama final entregado – Caso base

<img width="1738" height="850" alt="image" src="https://github.com/user-attachments/assets/bfac1248-6dd4-4cfe-b082-e783ae687690" />

[Ver diagrama en Miro](https://miro.com/welcomeonboard/SUJ0WUVJaGY5bEJUd01pb2ZRWGZrL3ZlRGhadlJUV0hvNzJJcEN5aWJETXM2RUs3OGtRL241a09HMlVXbGlTT0pid29mcEhaSlVvVWhDVTl6UitHRW1nTjdyT3h2ZytVTmFiZEtSdjFDMlZPcXh2bmk2YWdzS1lTbXpBVUdOZEhQdGo1ZEV3bUdPQWRZUHQzSGl6V2NBPT0hdjE=?share_link_id=10153609605)

---

# 🔹 Cliente real: Proceso de cotización y venta

### 📌 Estructura del modelo

El modelo incluye:

* **Evento de inicio:** Cliente solicita cotización.
* **Actividades del asesor comercial:** Registrar solicitud en CRM y generar cotización.
* **Validación del sistema:** Verificación de inventario.
* **Gateway exclusivo:** ¿Stock disponible?
* **Actividad del sistema:** Envío de cotización.
* **Gateway exclusivo:** ¿Acepta cotización?
* **Actividades del sistema:** Generación de orden de venta, descuento de inventario y facturación.
* **Actividad del área contable:** Registro del movimiento contable.
* **Evento final:** Venta registrada y facturada.

### 📌 Justificación del modelo

El modelo fue diseñado para representar la trazabilidad completa del proceso comercial, desde la solicitud inicial hasta el impacto financiero.

Se identificaron dos puntos críticos de decisión:

1. **Disponibilidad de inventario**, que determina la viabilidad operativa.
2. **Aceptación de la cotización**, que representa el punto de conversión comercial.

La inclusión del registro contable permite visualizar la integración entre áreas comerciales, operativas y financieras, evidenciando cómo un evento comercial impacta directamente en los sistemas contables de la organización.

### Supuestos

* Inventario actualizado en tiempo real.
* Cliente responde oportunamente.
* Sistemas CRM y contable integrados.

### Puntos críticos identificados

* Riesgo de sobreventa por inventario desactualizado.
* Demoras en respuesta del cliente.
* Integración deficiente entre sistemas.
* Errores en facturación o registro contable.

---

## 📈 Diagrama final entregado – Cliente real

<img width="1774" height="1143" alt="image" src="https://github.com/user-attachments/assets/72453266-3625-4419-94ed-5a3ecfae2329" />

[Ver diagrama en Miro](https://miro.com/welcomeonboard/SFZGYVI3RldmdGo5T0pxYTArYkNUVVFXTkRXelpkclM1cFBsK3dOZ0tvS0xpWDhPZzJ3OENab3ZlTzh1SVNxbVVidTN1V3Q0WlFQNkVQQ1FhQm0xWkdnTjdyT3h2ZytVTmFiZEtSdjFDMlV6V2Z5RURCM01vcE9oS0hlUkhZV1p0R2lncW1vRmFBVnlLcVJzTmdFdlNRPT0hdjE=?share_link_id=600125739103)

---

# 📋 Tabla de actores y componentes

| Nombre del elemento | Tipo    | Descripción                                    | Responsable     |
| ------------------- | ------- | ---------------------------------------------- | --------------- |
| Paciente            | Actor   | Usuario que agenda una cita médica             | Cliente         |
| Sistema de citas    | Sistema | Valida disponibilidad y registra citas         | Organización    |
| Cliente             | Actor   | Persona que solicita cotización                | Empresa cliente |
| Asesor comercial    | Actor   | Gestiona solicitudes y genera cotizaciones     | Área comercial  |
| Sistema ERP/CRM     | Sistema | Verifica inventario, genera órdenes y facturas | Organización    |
| Área contable       | Actor   | Registra movimiento contable                   | Área financiera |

---

# 🔍 Investigación complementaria

### 📌 Buenas prácticas BPMN

Según el **Object Management Group (OMG, 2011)**, BPMN 2.0 proporciona una notación estándar que facilita la comprensión de procesos tanto para analistas como para desarrolladores técnicos, permitiendo su posible automatización mediante motores de ejecución.

Durante el modelado se aplicaron buenas prácticas como:

* Flujo lógico de izquierda a derecha.
* Uso de verbo + objeto en actividades.
* Gateways exclusivos correctamente etiquetados.
* Separación de roles mediante lanes.
* Evitar sobrecargar el diagrama con detalles innecesarios.

### 📌 Aplicación en la industria

BPMN se utiliza ampliamente en:

* **Sector salud:** Gestión de citas y admisiones.
* **Sector bancario:** Aprobación de créditos y validación de riesgo.
* **Comercio electrónico:** Gestión de pedidos e inventarios.
* **Industria manufacturera:** Control de órdenes de producción y logística.

Su implementación permite optimizar tiempos, reducir errores y mejorar la trazabilidad de la información.

---

# 📊 Comparación entre caso base y cliente real

| Aspecto              | Clínica Salud Viva     | Cliente Real                            |
| -------------------- | ---------------------- | --------------------------------------- |
| Tipo de proceso      | Agendamiento de citas  | Cotización y venta                      |
| Actores              | Paciente, Sistema      | Cliente, Asesor, Sistema, Área contable |
| Decisiones           | Disponibilidad de cita | Stock disponible y aceptación           |
| Resultado final      | Cita registrada        | Venta facturada                         |
| Nivel de complejidad | Bajo                   | Medio-Alto                              |

---

# 📚 Referencias

Object Management Group (OMG). (2011). *Business Process Model and Notation (BPMN) Version 2.0*. [https://www.omg.org/spec/BPMN/2.0](https://www.omg.org/spec/BPMN/2.0)

White, S. A., & Miers, D. (2008). *BPMN Modeling and Reference Guide*. Future Strategies Inc.

Dumas, M., La Rosa, M., Mendling, J., & Reijers, H. A. (2018). *Fundamentals of Business Process Management*. Springer.

Camunda. (s.f.). *BPMN Best Practices*. Recuperado el 13 de febrero de 2026.

Bizagi. (s.f.). *Guía de Modelamiento BPMN*. Recuperado el 13 de febrero de 2026.

OpenAI. (2026). *ChatGPT* (versión febrero 2026). Utilizado como apoyo en redacción y organización del documento.

---

# 🏁 Conclusión

El taller permitió aplicar la notación BPMN a contextos de distinta complejidad, evidenciando cómo una herramienta estandarizada facilita la comprensión, análisis y mejora de procesos organizacionales.

Mientras el caso base representó un proceso sencillo de interacción usuario-sistema, el cliente real permitió modelar un flujo empresarial completo con integración de áreas comerciales, operativas y financieras, demostrando el valor estratégico de BPMN en entornos corporativos.

---

*Documento elaborado para el Taller 1 del curso Arquitectura Empresarial – Universidad de La Sabana.*
