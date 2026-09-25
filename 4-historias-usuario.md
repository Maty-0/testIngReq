# Historias de usuario

## HU-01: Planificador e Historial en Grilla Interactiva
Como **estudiante**, quiero **simular combinaciones de horarios en una grilla interactiva semanal**, para **visualizar de forma clara mi carga académica y evitar choques de horario o sobrecarga de créditos**.
- **Actividad TO-BE asociada:** Simular horario y revisar métricas de dificultad
- **Criterios de aceptación:**
  - **CA1:** El sistema permite agregar y remover secciones de la grilla horaria mediante interacción visual (clic o drag-and-drop).
  - **CA2:** El contador de créditos totales se actualiza dinámicamente cada vez que se modifica una sección dentro de la simulación.
  - **CA3:** El sistema bloquea de inmediato la adición de una sección si esta genera un choque de horario o supera el tope crediticio permitido.

## HU-02: Consulta de Referencias y Dificultad Docente
Como **estudiante**, quiero **ver las calificaciones de profesores y el nivel de dificultad asignado por la comunidad a cada materia**, para **tomar decisiones informadas al momento de estructurar mi horario semestral**.
- **Actividad TO-BE asociada:** Simular horario y revisar métricas de dificultad
- **Criterios de aceptación:**
  - **CA1:** Cada sección despliega una valoración con estrellas (1 a 5) del docente y un indicador de exigencia/dificultad de la asignatura.
  - **CA2:** Las puntuaciones mostradas corresponden al promedio actualizado de las opiniones registradas por estudiantes en semestres anteriores.
  - **CA3:** La interfaz no expone en ningún apartado la identidad ni los datos personales de los estudiantes que emitieron las valoraciones.

## HU-03: Visualización Graph-based de Cadena Crítica Curricular
Como **estudiante**, quiero **seleccionar una asignatura en la malla interactiva y desplegar toda su cadena de prerrequisitos e imprevistos**, para **comprender el impacto curricular completo de aprobar o reprobar un curso**.
- **Actividad TO-BE asociada:** Consultar malla interactiva y tiempo restante
- **Criterios de aceptación:**
  - **CA1:** Al seleccionar un ramo, la malla resalta gráficamente la red completa de prerrequisitos hacia atrás y asignaturas dependientes hacia adelante.
  - **CA2:** El grafo aplica un código de colores estándar para distinguir materias aprobadas, inscritas, disponibles y bloqueadas.

## HU-04: Calculadora de Tiempo Estimado para la Titulación
Como **estudiante**, quiero **conocer la cantidad mínima estimada de semestres restantes para terminar mi carrera**, para **planificar estratégicamente mi avance académico a mediano y largo plazo**.
- **Actividad TO-BE asociada:** Consultar malla interactiva y tiempo restante
- **Criterios de aceptación:**
  - **CA1:** El sistema analiza el historial académico aprobado y calcula la ruta crítica mínima de semestres necesarios para egresar.
  - **CA2:** Si el usuario simula la desaprobación o postergación de un ramo en la malla, el indicador recalculado refleja el potencial retraso en semestres.

## HU-05: Confirmación e Inscripción Directa de Horario
Como **estudiante**, quiero **enviar directamente la simulación de horario previamente diseñada para mi inscripción oficial**, para **asegurar mis cupos en un solo clic sin reingresar datos**.
- **Actividad TO-BE asociada:** Confirmar e inscribir horario simulado
- **Criterios de aceptación:**
  - **CA1:** La interfaz dispone de un botón de confirmación directa activo durante la apertura del periodo oficial de inscripciones.
  - **CA2:** Al confirmar, el sistema registra la selección, actualiza la disponibilidad de cupos en tiempo real y emite un comprobante digital de inscripción.