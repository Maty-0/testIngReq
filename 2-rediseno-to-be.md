# Análisis de rediseño y propuesta TO-BE

## Mejoras identificadas por participante
| Participante | Objetivo | Problema | Mejora deseada |
|----------------|----------|----------|-----------------|
| Dirección Docente | Difundir la oferta académica eficientemente. | La publicación mediante Excel desarticulado exige procesamiento manual del alumno y genera consultas posteriores por errores. | Integrar la oferta académica directamente en una base de datos centralizada consumible de forma dinámica por la plataforma. |
| Estudiante | Planificar un horario funcional y tomar decisiones académicas informadas. | Proceso manual propenso a choques de horario, cálculo de créditos erróneo, malla estática limitada y falta de referencias docentes. | Planificador interactivo de horario, estimación de tiempo real de carrera, visualización completa de la red de prerequisitos/correquisitos y puntuación comunitaria de dificultad/docentes. |

## Iniciativas de rediseño

### Iniciativa 1: Automatización e Integración de Oferta Académica (SGAI)
- **Actividad(es) del AS-IS que afecta:** Publicar archivo Excel con oferta académica / Descargar oferta en Excel.
- **Heurística aplicada:** *Task Automation* (Automatización de tareas) & *Integral Technology* (Tecnología Integral).
- **Objetivo o mejora que resuelve:** Cargar la oferta académica directamente en la base de datos del sistema, eliminando la generación e intercambio de archivos Excel independientes.
- **Efecto esperado:** Reducción drástica del tiempo de preparación, eliminación del procesamiento manual por parte del estudiante y disponibilidad inmediata de la oferta actualizada en tiempo real.

### Iniciativa 2: Diseñador y Simulador Interactivo de Horarios con Puntuación Docente
- **Actividad(es) del AS-IS que afecta:** Buscar referencias de docentes y materias / Calcular créditos y detectar choques de horario.
- **Heurística aplicada:** *Task Composition* (Composición de tareas) & *Empower* (Empoderamiento al usuario).
- **Objetivo o mejora que resuelve:** Consolidar en una única interfaz interactiva la construcción de horario por drag-and-drop, la validación automática de choques horarios y créditos, y el despliegue de métricas comunitarias de dificultad y calificaciones de profesores.
- **Efecto esperado:** Aumento exponencial en la calidad de la planificación, cero choques de horario inadvertidos y toma de decisiones fundamentada en retroalimentación objetiva de la comunidad estudiantil.

### Iniciativa 3: Malla Interactiva Multinivel y Calculadora de Tiempo Real de Carrera
- **Actividad(es) del AS-IS que afecta:** Revisar malla curricular estática.
- **Heurística aplicada:** *Control Relocation* / *Informational Integration* (Aumento de visibilidad de datos).
- **Objetivo o mejora que resuelve:** Reemplazar el gráfico estático por un grafo multinivel que resalte toda la cadena crítica de asignaturas (dependencias previas y posteriores) y calcule automáticamente la duración mínima estimada para finalizar la carrera (semestres restantes).
- **Efecto esperado:** Incremento sustancial en la flexibilidad y planificación académica del estudiante a mediano y largo plazo.

## Diagrama TO-BE
![Proceso TO-BE](./diagramas/to-be.png)
Archivo fuente: [`./diagramas/to-be.bpmn`](./diagramas/to-be.bpmn)

### Descripción de Tareas en el Modelo TO-BE
- **Sincronizar y publicar oferta académica** (*Service Task*): El sistema carga y valida automáticamente la base de datos de asignaturas, cupos, secciones y horarios para el periodo correspondiente.
- **Consultar malla interactiva de cadena crítica** (*User Task*): El estudiante selecciona asignaturas en el grafo dinámico, proyectando la ruta curricular completa y calculando el estimado de tiempo mínimo restante para la titulación.
- **Simular horario y revisar métricas de dificultad** (*User Task*): El estudiante arrastra secciones a una grilla semanal interactiva; el sistema muestra calificaciones estudiantiles de profesores y dificultad percibida.
- **Validar automáticamente tope de horarios y créditos** (*Service Task*): El sistema evalúa en tiempo real que la combinación simulada no contenga cruces horarias ni exceda los límites de créditos permitidos.
- **Confirmar e inscribir horario predeterminado** (*User Task*): El estudiante envía la combinación óptima verificada con un único clic al abrirse el proceso oficial.
- **Registrar inscripción y actualizar vacantes** (*Service Task*): El sistema efectúa el registro, confirma la carga académica y actualiza los cupos disponibles de forma inmediata.

## Actividades que cambian del AS-IS al TO-BE
| Actividad en el AS-IS | Actividad en el TO-BE | Qué cambia |
|-------------------------|--------------------------|------------|
| Publicar archivo Excel con oferta académica / Descargar oferta en Excel | Sincronizar y publicar oferta académica | Se elimina el archivo Excel estático; el sistema procesa y publica la oferta en la base de datos centralizada. |
| Revisar malla curricular estática | Consultar malla interactiva de cadena crítica | Pasa de mostrar dependencias de 1er grado a desplegar toda la red de prerequisitos/correquisitos y estimar los semestres mínimos restantes. |
| Buscar referencias de docentes y materias | Simular horario y revisar métricas de dificultad | La información de docentes y grado de dificultad se integra directamente dentro del simulador desde valoraciones estudiantiles. |
| Calcular créditos y detectar choques de horario | Validar automáticamente tope de horarios y créditos | La validación matemática de créditos y traslapes horarias la realiza el sistema en tiempo real, bloqueando selecciones inválidas. |
| Ingresar asignaturas en sistema web | Confirmar e inscribir horario predeterminado | Se reemplaza la digitación individual y manual por la confirmación directa de un diseño simulado previo. |