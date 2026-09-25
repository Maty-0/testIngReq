# Clasificación de requisitos

## Requisitos de producto

| ID | Requisito | Tipo (funcional/no funcional) | Actividad TO-BE asociada |
|----|-----------|--------------------------------|----------------------------|
| RP-01 | El sistema debe sincronizar y procesar automáticamente la oferta académica desde las bases de datos institucionales sin requerir archivos Excel. | Funcional | Sincronizar y publicar oferta en BD |
| RP-02 | El sistema debe desplegar un grafo dinámico de la malla curricular que resalte la cadena crítica completa de prerrequisitos y correquisitos de una asignatura seleccionada. | Funcional | Consultar malla interactiva y tiempo restante |
| RP-03 | El sistema debe calcular y mostrar el estimado en semestres para terminar la carrera según la ruta crítica de asignaturas pendientes. | Funcional | Consultar malla interactiva y tiempo restante |
| RP-04 | El sistema debe proporcionar una grilla interactiva semanal que permita al estudiante simular horarios agregando o eliminando secciones visualmente. | Funcional | Simular horario y revisar métricas de dificultad |
| RP-05 | El sistema debe desplegar la calificación de dificultad de las materias y la puntuación de los docentes asignados dentro del planificador de horarios. | Funcional | Simular horario y revisar métricas de dificultad |
| RP-06 | El sistema debe validar en tiempo real que las secciones seleccionadas no generen choques horarios ni excedan la carga máxima de créditos permitida. | Funcional | Validar automáticamente topes y créditos en simulador |
| RP-07 | El sistema debe permitir la inscripción directa y en un solo clic del horario previamente diseñado y validado en el simulador. | Funcional | Confirmar e inscribir horario simulado |
| RP-08 | La interfaz del simulador interactivo debe responder a las interacciones del usuario (drag-and-drop o selección) en un tiempo inferior a 1 segundo. | No funcional | Simular horario y revisar métricas de dificultad |
| RP-09 | El sistema debe garantizar la disponibilidad y soportar accesos concurrentes de al menos 5.000 estudiantes durante el período oficial de inscripción. | No funcional | Confirmar e inscribir horario simulado |
| RP-10 | Las valoraciones y comentarios sobre profesores y asignaturas deben almacenarse y desplegarse bajo estricto anonimato del estudiante. | No funcional | Simular horario y revisar métricas de dificultad |

## Requisitos de proyecto

| ID | Requisito |
|----|-----------|
| RY-01 | El proyecto debe alojarse en un repositorio de la organización oficial del equipo en GitHub, incluyendo la documentación en archivos Markdown (.md). |
| RY-02 | Los diagramas de procesos de negocio (AS-IS y TO-BE) deben modelarse bajo el estándar BPMN 2.0 y adjuntarse tanto en formato PNG como en archivo fuente .bpmn. |
| RY-03 | La Entrega 1 debe ser enviada y consolidada en GitHub antes de la fecha y hora límite establecida (Jueves 24 de septiembre a las 10:00 AM). |

## Requisito derivado
**Requisito origen:** RP-05 (Despliegue de puntuaciones de dificultad y valoraciones de docentes en el simulador)
**Requisito derivado:** RP-10 (Anonimización estricta de las evaluaciones y valoraciones estudiantiles)
**Justificación:** Para garantizar la objetividad y promover la participación activa de los alumnos al evaluar docentes y materias sin temor a represalias académicas, se deriva técnicamente la necesidad de enmascarar o desvincular cualquier identidad de usuario de los registros de valoración en la base de datos.