
# Gestión de Acuerdos de Nivel de Servicio (SLA)

## 1. Descripción

Diseño y configuración de acuerdos de nivel de servicio (SLA) mediante Jira Service Management.

El objetivo es establecer mecanismos para medir los tiempos de atención de incidentes y solicitudes de servicio, considerando prioridades, horarios operativos y condiciones de suspensión.

## 2. Métricas principales

### Tiempo de primera respuesta

Mide el tiempo transcurrido desde la creación del ticket hasta la primera respuesta válida del equipo de soporte.

### Tiempo de resolución

Mide el tiempo de atención necesario para alcanzar la resolución del ticket, considerando las condiciones configuradas para el SLA.

Los objetivos de ambas métricas se establecen según la prioridad del servicio.

## 3. Clasificación por prioridad

Las solicitudes se clasifican mediante una matriz de impacto y urgencia.

| Prioridad | Clasificación |
|-----------|---------------|
| P1 | Crítica |
| P2 | Alta |
| P3 | Media |
| P4 | Baja |

Esta clasificación permite establecer diferentes objetivos de atención y resolución.

## 4. Calendario de servicio

El sistema utiliza un calendario laboral para calcular los tiempos de los SLA.

| Día | Horario |
|-----|---------|
| Lunes a jueves | 08:00 - 18:00 |
| Viernes | 08:00 - 13:00 |
| Sábado | Fuera de horario |
| Domingo | Fuera de horario |

Las horas fuera del calendario laboral no se contabilizan dentro del tiempo objetivo.

## 5. Condiciones de pausa

Se establecieron condiciones para suspender temporalmente el cálculo del SLA.

### Esperando al cliente

El tiempo se pausa cuando se requiere información adicional del solicitante y el ticket pasa al estado correspondiente.

### Escalamiento

Se contemplan pausas asociadas con estados de escalamiento y espera, conforme a las reglas específicas de cada flujo.

### Fuera del horario laboral

El contador del SLA deja de acumular tiempo fuera del calendario configurado.

## 6. Reanudación del SLA

El cálculo se reanuda cuando el ticket deja de cumplir las condiciones de pausa y se encuentra dentro del horario laboral.

## 7. Seguimiento y control

Los SLA permiten:

- Identificar tickets próximos a incumplir su objetivo.
- Consultar tiempos restantes de atención.
- Medir cumplimiento de primera respuesta.
- Medir cumplimiento de resolución.
- Identificar solicitudes que requieren seguimiento.
- Apoyar la generación de reportes operativos.

## 8. Validación funcional

Durante la implementación se realizaron pruebas de:

- Cálculo de SLA según prioridad.
- Comportamiento del calendario laboral.
- Suspensión del contador.
- Reanudación después de una pausa.
- Visualización de tiempos restantes.
- Comportamiento de los SLA ante cambios de estado.

## 9. Consideraciones técnicas

Los objetivos y condiciones de los SLA dependen de la configuración de cada servicio y de las capacidades disponibles en la licencia de Jira Service Management.

Este documento presenta el diseño funcional general y no expone información interna ni compromisos contractuales del cliente.

---

**Autor:** Martín Ramos

**Proyecto:** IT Service Desk Implementation

**Tecnología:** Jira Service Management
