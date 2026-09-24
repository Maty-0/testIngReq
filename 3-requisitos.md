# Clasificación de requisitos

## Requisitos de producto

| ID | Requisito | Tipo (funcional/no funcional) | Actividad TO-BE asociada |
|----|-----------|--------------------------------|----------------------------|
| RP-01 | El sistema debe desplegar una grilla semanal interactiva que permita al estudiante simular combinaciones de horarios arrastrando o seleccionando secciones. | Funcional | Simular horario y revisar métricas de dificultad |
| RP-02 | El sistema debe validar de forma automática los cruces horarias y la carga máxima de créditos, notificando de inmediato las incoherencias al usuario. | Funcional | Validar automáticamente tope de horarios y créditos |
| RP-03 | El sistema debe mostrar dentro de la oferta académica la puntuación de dificultad de la asignatura y la valoración del profesor otorgada por otros estudiantes. | Funcional | Simular horario y revisar métricas de dificultad |
| RP-04 | La malla interactiva debe resaltar la cadena crítica completa (todas las asignaturas dependientes anteriores y posteriores) al seleccionar una materia. | Funcional | Consultar malla interactiva de cadena crítica |
| RP-05 | El sistema debe calcular y mostrar el estimado en semestres para terminar la carrera según la ruta académica seleccionada por el estudiante. | Funcional | Consultar malla interactiva de cadena crítica |
| RP-06 | La interfaz de la grilla horaria interactiva debe responder a las acciones del usuario en un tiempo menor a 1 segundo. | No funcional | Simular horario y revisar métricas de dificultad |
| RP-07 | La plataforma debe garantizar el acceso simultáneo de al menos 5.000 usuarios en los períodos de alta demanda de inscripción sin caídas del servicio. | No funcional | Confirmar e inscribir horario predeterminado |
| RP-08 | Las evaluaciones y comentarios sobre profesores deben procesarse de forma anónima para resguardar la privacidad de los estudiantes. | No funcional | Simular horario y revisar métricas de dificultad |

## Requisitos de proyecto

| ID | Requisito |
|----|-----------|
| RY-01 | El código fuente del proyecto debe entregarse en un repositorio de la organización oficial en GitHub, incluyendo historial de commits de todos los integrantes. |
| RY-02 | El proyecto debe incluir diagramas de procesos de negocio desarrollados bajo el estándar BPMN 2.0 utilizando herramientas como Camunda Modeler o draw.io. |
| RY-03 | La especificación e implementación inicial deben completarse respetando la fecha límite establecida para la Entrega 1. |

## Requisito derivado
**Requisito origen:** RP-03 (Despliegue de puntuaciones de dificultad y valoraciones de profesores)
**Requisito derivado:** RP-08 (Anonimización estricta de las evaluaciones estudiantiles)
**Justificación:** Para garantizar que los estudiantes califiquen libremente a los docentes y evalúen la dificultad de las asignaturas sin temor a represalias académicas, se deriva la necesidad técnica de enmascarar los identificadores de usuario al guardar o consultar cualquier valoración en el módulo de métricas.