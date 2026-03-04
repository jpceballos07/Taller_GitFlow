# Taller_GitFlow
Aplicar el modelo de ramas GitFlow (main, develop y feature) para gestionar cambios en documentación técnica, diseñando casos de prueba a partir del análisis de requerimientos utilizando técnicas de prueba de caja negra.

# Descripción del Sistema

El sistema permite gestionar eventos académicos y la participación de estudiantes en ellos.  
Los estudiantes pueden registrarse en el sistema, consultar eventos disponibles e inscribirse si cumplen ciertas condiciones.  
El sistema controla la disponibilidad de cupos y evita inscripciones duplicadas.  
Además, valida que los estudiantes estén registrados antes de permitir cualquier inscripción.

# Requerimientos a Evaluar

- *RF-01:* Registro de estudiantes en el sistema.  
- *RF-02:* Creación y gestión de eventos con cupos disponibles.  
- *RF-03:* Inscripción de estudiantes a eventos, validando que el estudiante esté registrado, que haya cupos disponibles y que no esté inscrito previamente.

# Técnicas de Prueba Aplicadas

# RF-03
**Técnica seleccionada:** Tabla de decisión  

*Justificación:*  
La inscripción depende de la combinación de varias condiciones (registro del estudiante, disponibilidad de cupos y no estar inscrito previamente). La tabla de decisión permite evaluar todas las combinaciones posibles.
# Casos de Prueba Diseñados
## RF-03

| Caso | Registrado | Cupos disponibles | Ya inscrito | Resultado esperado |
|----|----|----|----|----|
| CP-05 | Sí | Sí | No | Inscripción exitosa |
| CP-06 | Sí | No | No | Inscripción rechazada |

