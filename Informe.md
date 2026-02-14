#  📄 Informe Técnico del Taller

## 🔖 Nombre del Taller

**Taller 1 - Modelado de Procesos con BPMN**

## 👥 Integrantes del equipo

- Isabela Díaz Acosta
- Sebastián Sánchez Sandoval
- Samuel Esteban López Huertas

## 🧠 Descripción general del trabajo

El presente taller tuvo como objetivo modelar un proceso de negocio utilizando la notación BPMN, partiendo del caso base de la Clínica Salud Viva y aplicando los conocimientos adquiridos a un cliente real.

Durante el desarrollo del trabajo se identificaron eventos, actividades, decisiones, actores involucrados y puntos críticos del flujo, con el fin de representar el proceso de manera clara, estructurada y comprensible tanto para usuarios técnicos como de negocio.

## 🔧 Proceso de desarrollo

El equipo inició analizando el caso base de la Clínica Salud Viva, identificando el flujo principal del proceso de agendamiento de citas médicas, así como los actores involucrados y las decisiones clave.

Posteriormente, se realizó el modelado del proceso utilizando herramientas digitales como draw.io, organizando el flujo de izquierda a derecha y separando los roles mediante lanes. A medida que se avanzaba en el diagrama, se realizaron ajustes para mejorar la claridad, eliminar ambigüedades y asegurar el uso correcto de los elementos BPMN.

Finalmente, se adaptó la metodología al proceso del cliente real, justificando las diferencias y aplicando buenas prácticas de modelado.

## 🧩 Análisis del modelo propuesto

### Estructura del modelo

El modelo BPMN se estructura mediante:

- **Evento de inicio** que representa la solicitud del servicio.
- **Actividades** que describen las tareas principales del proceso.
- **Gateways exclusivos** para decisiones críticas.
- **Evento de fin** que indica la finalización del proceso.
- **Lanes** que separan responsabilidades por actor.

### Representación de las necesidades del cliente

El modelo refleja las necesidades del cliente al mostrar de forma clara:

- Interacciones entre usuarios y sistemas.
- Validaciones necesarias antes de completar el proceso.
- Puntos donde pueden ocurrir demoras o errores.

### Supuestos tomados

- El sistema de información funciona correctamente.
- Los usuarios proporcionan datos válidos.
- Las notificaciones se envían de forma automática.

## 📈 Diagrama final entregado

*Inserte aquí una imagen o enlace al archivo modelo-final.drawio.*

## 📋 Tabla de actores, entidades o componentes

| Nombre del elemento | Tipo | Descripción | Responsable |
|---------------------|------|-------------|-------------|
| Paciente | Actor | Usuario que agenda una cita médica | Cliente |
| Sistema de citas | Sistema | Plataforma que gestiona disponibilidad | Organización |
| Médico | Actor | Profesional que atiende la cita | Clínica |
| Servicio de notificaciones | Sistema | Envía confirmaciones por correo o SMS | Sistema |

## 🔍 Investigación complementaria

**Tema investigado:**

Buenas prácticas BPMN y ejemplos en la industria

**Resumen:**

Durante el modelado del proceso se aplicaron buenas prácticas de BPMN con el fin de garantizar claridad, comprensión y utilidad del diagrama. Se mantuvo una secuencia lógica del flujo, se utilizaron correctamente los eventos de inicio, intermedios y fin, y se emplearon gateways exclusivos para representar decisiones críticas. Asimismo, se separaron los roles mediante lanes y se nombraron las actividades con la estructura verbo + objeto para evitar ambigüedades.

El uso de BPMN es ampliamente adoptado en diversos sectores. En el sector salud se utiliza para la gestión de citas médicas, optimizando la asignación de recursos y reduciendo tiempos de espera. En el sector bancario permite modelar procesos de aprobación de créditos, mejorando la trazabilidad y reduciendo errores. En el comercio electrónico, empresas como Amazon emplean BPMN para optimizar el procesamiento de pedidos y la logística, mejorando la experiencia del cliente.

Un caso real en el sector salud evidenció que la implementación de BPMN en el proceso de admisión hospitalaria permitió reducir tiempos de atención, disminuir errores en registros y mejorar la experiencia del paciente, demostrando su valor como herramienta para la mejora continua.

## 📚 Referencias

- Object Management Group. Business Process Model and Notation (BPMN) 2.0 Specification.
- Documentación oficial de BPMN — https://www.omg.org/spec/BPMN/
- Ejemplos de aplicación BPMN en sector salud y comercio electrónico.

---

*Este documento hace parte de la entrega del Taller 1 del curso de Arquitectura Empresarial - Universidad de La Sabana.*
