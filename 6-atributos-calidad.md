# Atributos de calidad (ISO 25010)

## Priorización de los 9 atributos de primer nivel
1. **Usabilidad (Usability):** Prioridad crítica para garantizar que la grilla interactiva, el simulador de horarios y el grafo de la malla curricular sean intuitivos y utilizables sin capacitación previa.
2. **Eficiencia de desempeño (Performance Efficiency):** Vital para mantener tiempos de respuesta inmediatos ante interacciones drag-and-drop y cambios en el simulador, soportando además picos de concurrencia.
3. **Fiabilidad (Reliability):** Indispensable para evitar caídas del servicio o pérdida de planificaciones guardadas durante los períodos con mayor volumen de accesos.
4. **Seguridad (Security):** Necesaria para resguardar los datos del estudiante y garantizar el anonimato estricto de las valoraciones de docentes y asignaturas.
5. **Mantenibilidad (Maintainability):** Requerida para modificar reglas académicas o la oferta curricular semestral sin reescribir componentes core del sistema.
6. **Compatibilidad (Compatibility):** Deseable para operar sin contratiempos en los principales navegadores web (Chrome, Firefox, Safari, Edge) y dispositivos.
7. **Flexibilidad (Flexibility / Adaptability):** Importante para responder a cambios en los reglamentos universitarios o variaciones de cupos.
8. **Portabilidad (Portability):** Permite el despliegue del sistema en infraestructuras locales institucionales o servicios en la nube.
9. **Adecuación funcional (Functional Suitability):** Asegura el cumplimiento estricto del 100% de las reglas de inscripción y prerrequisitos.

## Métricas de los 3 atributos más importantes

### Usabilidad (Usability)
- **Métrica:** *Tiempo de finalización de la simulación de horario en el primer intento.*
- **Descripción:** Se medirá el tiempo transcurrido desde que un estudiante ingresa al simulador hasta que construye un horario válido sin topes ni sobrecarga de créditos. El objetivo de calidad establece que al menos el **85% de los usuarios evaluados debe completar la simulación en menos de 3 minutos** en su primera interacción sin requerir asistencia.

### Eficiencia de desempeño (Performance Efficiency)
- **Métrica:** *Latencia de renderizado y recalculo en la grilla interactiva.*
- **Descripción:** Al agregar, arrastrar o remover una sección en la grilla del simulador, el tiempo de actualización visual del horario y el cálculo dinámico de créditos **no debe superar los 500 milisegundos (ms)** bajo condiciones de carga normal.

### Fiabilidad (Reliability)
- **Métrica:** *Disponibilidad del sistema (Uptime) en período de preinscripción e inscripción.*
- **Descripción:** La plataforma debe garantizar una **disponibilidad del 99.9%** durante la semana previa y el día oficial del proceso de inscripción, manteniendo la capacidad de atender solicitudes concurrentes de hasta **5.000 estudiantes simultáneos** sin degradación del servicio ni caídas del sistema.