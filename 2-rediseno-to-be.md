# Análisis de rediseño y propuesta TO-BE

## Mejoras identificadas por participante

| Participante | Objetivo | Problema | Mejora deseada |
|----------------|----------|----------|-----------------|
| Dirección Docente | Difundir la oferta académica semestral eficientemente. | La publicación mediante archivos Excel estáticos obliga al procesamiento manual y genera errores de consulta. | Cargar la oferta directamente en el sistema centralizado para ser consumida de forma dinámica. |
| Estudiante | Planificar un horario semestral válido y tomar decisiones informadas. | Proceso manual propenso a topes de hora/créditos, malla estática limitada a 1er grado y falta de datos de profesores/dificultad. | Simulador interactivo de horarios, malla multinivel con cadena crítica, tiempo estimado de egreso y métricas de dificultad docente. |

## Iniciativas de rediseño

### Iniciativa 1: Sincronización Automática de Oferta Académica
- **Actividad(es) del AS-IS que afecta:** Publica Excel de propuesta académica / Revisa la propuesta académica.
- **Heurística aplicada:** *Task Automation* & *Integral Technology*.
- **Objetivo o mejora que resuelve:** Reemplazar el archivo estático Excel por la sincronización directa en la base de datos del sistema universitario.
- **Efecto esperado:** Eliminación del procesamiento manual de archivos por parte del alumno y disponibilidad inmediata de la oferta actualizada en tiempo real.

### Iniciativa 2: Diseñador Interactivo de Horarios y Evaluación Docente
- **Actividad(es) del AS-IS que afecta:** Busca referencias de las asignaturas / Crea un horario en base a las asignaturas que puede cursar.
- **Heurística aplicada:** *Task Composition* & *Empower*.
- **Objetivo o mejora que resuelve:** Unificar en una sola interfaz interactiva la selección visual de secciones, la comprobación de dificultad/profesores y la validación inmediata de choques horarias y créditos.
- **Efecto esperado:** Reducción a cero de errores de sobrecarga o topes horarios, optimizando el tiempo de planificación del estudiante.

### Iniciativa 3: Malla Interactiva de Cadena Crítica y Calculadora de Tiempo de Egreso
- **Actividad(es) del AS-IS que afecta:** Revisa su avance curricular.
- **Heurística aplicada:** *Control Relocation* / *Informational Integration*.
- **Objetivo o mejora que resuelve:** Evolucionar la malla estática de 1er grado a un grafo dinámico que despliegue todos los prerrequisitos/correquisitos en cadena y estime el tiempo mínimo real restante de carrera.
- **Efecto esperado:** Mayor visibilidad estratégica para la toma de decisiones sobre qué ramos priorizar o botar semestralmente.

## Diagrama TO-BE
![Proceso TO-BE](./diagramas/to-be.png)
Archivo fuente: [`./diagramas/to-be.bpmn`](./diagramas/to-be.bpmn)

## Actividades que cambian del AS-IS al TO-BE

| Actividad en el AS-IS | Actividad en el TO-BE | Qué cambia |
|-------------------------|--------------------------|------------|
| Publica Excel de propuesta académica | Sincronizar y publicar oferta en BD | Pasa de la carga estática de una planilla Excel al procesamiento automático de la oferta en la base de datos del sistema. |
| Revisa su avance curricular | Consultar malla interactiva y tiempo restante | Pasa de un gráfico estático de 1er grado a un grafo multinivel con cálculo dinámico de semestres restantes para la titulación. |
| Busca referencias de las asignaturas | Simular horario y revisar métricas de dificultad | La búsqueda informal externa se reemplaza por métricas de dificultad y desempeño docente integradas en el simulador. |
| Crea un horario en base a las asignaturas que puede cursar | Validar automáticamente topes y créditos en simulador | El cálculo manual en papel/Excel es sustituido por una grilla interactiva que detecta e impide cruces horarias y excesos en tiempo real. |
| Guarda su horario | Confirmar e inscribir horario simulado | La digitación o inscripción manual se simplifica al envío directo del diseño simulado previamente guardado. |