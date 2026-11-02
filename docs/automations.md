
# Automatización de procesos y reglas de negocio

## 1. Descripción general

Diseño y configuración de reglas de negocio y automatizaciones mediante Jira Service Management para optimizar la gestión de incidentes y solicitudes de servicio.

El objetivo es reducir tareas manuales, estandarizar los procesos y mejorar la trazabilidad de las solicitudes.

## 2. Asignación automática de tickets

Se diseñaron reglas de asignación según el tipo de solicitud y el nivel de soporte correspondiente.

### Lógica funcional

1. El usuario registra una solicitud.
2. El sistema identifica el tipo de servicio.
3. Se determina el equipo o agente responsable.
4. Se asigna el ticket cuando existe un agente disponible y la automatización está habilitada.

La disponibilidad de estas reglas depende de los agentes configurados y del licenciamiento.

## 3. Gestión de estados

Se contemplaron reglas y transiciones para controlar el ciclo de vida de los tickets.

Estados considerados:

- Abierto / En cola
- Asignado
- En atención
- Esperando al cliente
- Requiere apoyo
- Escalamiento
- Resuelto
- Cerrado
- Reabierto

## 4. Espera de información del cliente

### Objetivo

Evitar que los tiempos de atención continúen acumulándose cuando se necesita información del solicitante.

### Lógica funcional

1. El ingeniero solicita información adicional.
2. El ticket pasa a "Esperando al cliente".
3. Se activa la condición de pausa del SLA.
4. El usuario proporciona la información.
5. El ticket puede regresar a "En atención".
6. El SLA se reanuda conforme al calendario laboral.

La pausa depende del estado del ticket, no solamente de que exista un comentario.

## 5. Escalamiento técnico

Se diseñaron procesos de escalamiento para niveles N1, N2 y N3.

### Nivel 1 (N1)

Atención inicial, diagnóstico y resolución de incidencias.

### Nivel 2 (N2)

Atención de solicitudes que requieren conocimientos técnicos adicionales o intervención especializada.

### Nivel 3 (N3)

Escalamiento hacia proveedores externos o especialistas.

En determinados servicios, N3 representa un periodo de espera de respuesta externa.

## 6. Reapertura de solicitudes

Se contemplaron transiciones y reglas para permitir la reapertura de tickets cuando el usuario reporta que el problema continúa o se requiere validación adicional.

## 7. Validaciones funcionales

Durante el proyecto se realizaron pruebas relacionadas con:

- Asignación automática.
- Cambios de estado.
- Pausas y reanudaciones de SLA.
- Escalamiento técnico.
- Resolución y cierre.
- Reapertura de tickets.
- Comportamiento de permisos y agentes.

## 8. Restricciones operativas

Las automatizaciones dependen de las funciones disponibles en el plan contratado.

Durante las pruebas se identificaron cambios en el comportamiento de determinadas reglas después de modificar el licenciamiento y la disponibilidad de agentes.

Por ello, las reglas descritas representan el diseño funcional y las configuraciones evaluadas, sin afirmar que todas permanecen activas en producción.

## 9. Competencias aplicadas

- Análisis de requerimientos.
- Diseño de reglas de negocio.
- Automatización de procesos.
- Lógica condicional.
- Modelado de estados y transiciones.
- Pruebas funcionales.
- Diagnóstico de incidencias de configuración.

---

**Autor:** Martín Ramos

**Tecnología:** Jira Service Management

**Tipo de proyecto:** Implementación y configuración de solución empresarial ITSM
