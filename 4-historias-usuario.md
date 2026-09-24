# Historias de usuario

## HU-01: Planificación mediante Horario Interactivo
Como **estudiante**, quiero **armar una simulación de mi horario semestral en una grilla interactiva visualizando directamente asignaturas, secciones y horas**, para **evaluar de forma clara mi carga académica sin recurrir a cálculos manuales**.
**Actividad TO-BE asociada:** Simular horario y revisar métricas de dificultad
**Criterios de aceptación:**
- CA1: El sistema permite agregar y quitar secciones de la grilla mediante selección visual o drag-and-drop.
- CA2: El total de créditos se recalcula automáticamente cada vez que se modifica una sección en el horario.
- CA3: El sistema bloquea de inmediato la adición de una sección si esta genera un choque de horario con otra previamente agregada.

## HU-02: Visualización de Referencias Docentes y Dificultad
Como **estudiante**, quiero **ver la puntuación promedio de dificultad de una materia y la valoración asignada a sus docentes**, para **tomar decisiones informadas al elegir en qué sección inscribirme**.
**Actividad TO-BE asociada:** Simular horario y revisar métricas de dificultad
**Criterios de aceptación:**
- CA1: Cada sección dentro del planificador muestra una calificación con estrellas (1 a 5) del profesor y un indicador del nivel de dificultad.
- CA2: Las puntuaciones se calculan dinámicamente según el promedio de evaluaciones registradas por alumnos en semestres anteriores.
- CA3: La interfaz no expone en ningún apartado la identidad ni los datos personales de los estudiantes que emitieron la valoración.

## HU-03: Malla Interactiva de Cadena Crítica
Como **estudiante**, quiero **seleccionar una asignatura en la malla interactiva y ver destacadas todas las materias vinculadas en la cadena de prerequisitos e imprevistos**, para **entender el impacto curricular global de mis cursos**.
**Actividad TO-BE asociada:** Consultar malla interactiva de cadena crítica
**Criterios de aceptación:**
- CA1: Al hacer clic en una asignatura, la malla resalta gráficamente todos sus prerequisitos (pasados) y todas las asignaturas que dependen directamente de ella (futuras).
- CA2: El sistema utiliza un código de colores diferenciado para distinguir asignaturas aprobadas, pendientes y bloqueadas.

## HU-04: Estimación del Tiempo Restante de Carrera
Como **estudiante**, quiero **visualizar la cantidad mínima estimada de semestres que me restan para titularme**, para **planificar estratégicamente mi avance académico a largo plazo**.
**Actividad TO-BE asociada:** Consultar malla interactiva de cadena crítica
**Criterios de aceptación:**
- CA1: El sistema analiza los ramos aprobados y calcula la ruta crítica óptima de prerrequisitos pendientes.
- CA2: Se despliega en pantalla un indicador con el número mínimo de semestres requeridos para egresar.
- CA3: Si el estudiante simula reprobar o postergar una asignatura, el contador de semestres estimados se actualiza instantáneamente reflejando el potencial retraso.