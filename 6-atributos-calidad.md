# Atributos de calidad (ISO 25010)

## Priorización de los 9 atributos de primer nivel
1. **Usabilidad (Usability):** Prioridad crítica para que la simulación horaria y la malla gráfica sean intuitivas y no requieran capacitación previa.
2. **Eficiencia de desempeño (Performance Efficiency):** Vital para mantener tiempos de respuesta inmediatos ante interacciones en la grilla horaria y soportar picos de concurrencia.
3. **Fiabilidad (Reliability):** Indispensable para evitar caídas del sistema o pérdida de preinscripciones en los momentos con más volumen de accesos.
4. **Seguridad (Security):** Necesaria para resguardar la identidad del alumnado y garantizar el anonimato de las puntuaciones emitidas.
5. **Mantenibilidad (Maintainability):** Requerida para modificar la oferta académica o reglas curriculares cada semestre sin rehacer la aplicación.
6. **Compatibilidad (Compatibility):** Deseable para operar de forma óptima en diversos navegadores web y dispositivos (escritorio y móviles).
7. **Flexibilidad (Flexibility / Adaptability):** Importante para ajustarse a cambios en los reglamentos de evaluación o variaciones en los cupos.
8. **Portabilidad (Portability):** Permitir el despliegue del sistema en infraestructuras locales o en la nube según la universidad.
9. **Funcionalidad (Functional Suitability):** Asegurar que las reglas del negocio de la inscripción se cumplan al 100%.

## Métricas de los 3 atributos más importantes

### 1. Usabilidad (Usability)
- **Métrica:** *Tiempo promedio para completar una simulación exitosa de horario.*
- **Descripción:** Se medirá el tiempo transcurrido desde que un estudiante entra al planificador hasta que arma un horario válido sin choques de horario. El objetivo es que el 90% de los usuarios logre armar un horario completo en **menos de 3 minutos** en su primer intento.

### 2. Eficiencia de desempeño (Performance Efficiency)
- **Métrica:** *Tiempo de respuesta en la grilla interactiva y latencia de renderizado.*
- **Descripción:** Al arrastrar, agregar o quitar una sección dentro de la grilla horaria, el tiempo de actualización visual y recalculo de créditos **no debe superar los 500 milisegundos** bajo pruebas de carga normales.

### 3. Fiabilidad (Reliability)
- **Métrica:** *Tasa de disponibilidad del sistema (Uptime) en periodo crítico.*
- **Descripción:** La plataforma debe garantizar una disponibilidad del **99.9%** durante la semana previa y el día oficial de inscripciones, soportando peticiones concurrentes simultáneas de hasta 5.000 usuarios sin caída de servicios.