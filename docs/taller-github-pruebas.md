# Documento de Pruebas

### 1. Análisis del enunciado
*   **Requerimiento:** RF-01 Registro de Estudiante (Edad).
*   **Regla de negocio:** El sistema debe permitir el registro de estudiantes cuya edad esté entre 16 y 65 años inclusive.
*   **Variable de entrada ($x$):** Edad del estudiante (valor numérico entero).
*   **Condición lógica:** $16 \le x \le 65$.

### 2. Técnica de prueba más adecuada
La técnica más adecuada es el **Análisis de Valor Límite (AVL)** [1, 2].

### 3. Justificación de la técnica
El requerimiento establece un **rango numérico definido** [1]. El Análisis de Valor Límite es idóneo porque se basa en probar los valores en las fronteras exactas del rango acotado ($a$ y $b$) y los valores justo arriba y justo abajo de estos [2], que es donde estadísticamente ocurren la mayoría de los defectos lógicos de programación.

### 4. Diseño de los Casos de Prueba (AVL)

| ID | Tipo de Límite | Valor (Edad) | Pasos de la Prueba | Resultado Esperado |
| :--- | :--- | :---: | :--- | :--- |
| **CP-01** | Límite Inferior - 1 (Inválido) | **15** | 1. Ingresar al formulario de registro.<br>2. Ingresar la edad: **15**.<br>3. Enviar el registro. | **Rechazado.** El sistema bloquea el registro y muestra error. |
| **CP-02** | Límite Inferior (Válido) | **16** | 1. Ingresar al formulario de registro.<br>2. Ingresar la edad: **16**.<br>3. Enviar el registro. | **Aceptado.** El sistema procesa el formulario y permite el registro. |
| **CP-03** | Límite Superior (Válido) | **65** | 1. Ingresar al formulario de registro.<br>2. Ingresar la edad: **65**.<br>3. Enviar el registro. | **Aceptado.** El sistema procesa el formulario y permite el registro. |
| **CP-04** | Límite Sup. + 1 (Inválido) | **66** | 1. Ingresar al formulario de registro.<br>2. Ingresar la edad: **66**.<br>3. Enviar el registro. | **Rechazado.** El sistema bloquea el registro y muestra error. |