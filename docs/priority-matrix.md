
# Matriz de Impacto, Urgencia y Prioridad

## 1. Descripción

Diseño e implementación de criterios de clasificación y priorización de incidentes y solicitudes de servicio mediante Jira Service Management.

El objetivo es establecer un modelo de atención basado en reglas de negocio que permita identificar los tickets que requieren mayor prioridad.

## 2. Criterios de evaluación

### Impacto

Representa el alcance de la afectación que genera un incidente en la operación.

Para determinarlo se consideran factores como:

- Cantidad de usuarios afectados.
- Servicios o sistemas involucrados.
- Afectación a procesos empresariales.
- Consecuencias operativas del incidente.

### Urgencia

Representa la rapidez con la que debe atenderse una solicitud.

Se consideran factores como:

- Necesidad de restablecimiento del servicio.
- Tiempo disponible para intervenir.
- Consecuencias de retrasar la atención.
- Continuidad de las actividades operativas.

## 3. Niveles de prioridad

Se establecieron cuatro niveles para organizar la atención de solicitudes.

| Prioridad | Clasificación | Descripción |
|-----------|---------------|-------------|
| P1 | Crítica | Incidentes con afectación operativa crítica. |
| P2 | Alta | Incidentes que requieren atención prioritaria. |
| P3 | Media | Solicitudes con impacto moderado. |
| P4 | Baja | Solicitudes de menor urgencia e impacto. |

## 4. Matriz de decisión

La prioridad se determina mediante la evaluación conjunta de impacto y urgencia.

La matriz permite establecer criterios consistentes y reducir la clasificación subjetiva de los incidentes.

### Ejemplo de clasificación

Impacto bajo + Urgencia baja = Prioridad P4.

Las demás combinaciones deben corresponder a los valores establecidos en la matriz operativa del sistema.

## 5. Relación con los SLA

La prioridad asignada determina los objetivos de primera respuesta y resolución correspondientes.

De esta manera, los tickets de diferente criticidad pueden tener tiempos objetivo distintos.

## 6. Gestión de incidentes críticos

Se contemplaron criterios para permitir la atención preferente de incidentes críticos cuando exista una actividad en curso.

Esto permite gestionar situaciones de mayor afectación operativa.

## 7. Validaciones funcionales

Durante la implementación se realizaron pruebas relacionadas con:

- Selección de impacto.
- Selección de urgencia.
- Clasificación de prioridades.
- Comportamiento de campos personalizados.
- Relación entre prioridad y SLA.
- Visualización y ordenamiento de tickets.

## 8. Competencias aplicadas

- Análisis de requerimientos.
- Diseño de matrices de decisión.
- Implementación de reglas de negocio.
- Gestión de prioridades.
- Gestión de incidentes.
- Pruebas funcionales.
- Estandarización de procesos.

---

**Autor:** Martín Ramos

**Tecnología:** Jira Service Management

**Proyecto:** IT Service Desk Implementation
