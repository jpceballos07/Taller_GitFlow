# Documento de Pruebas
### RF-01 Registro de estudiante
### Análisis del enunciado
*   **Requerimiento:** RF-01 Registro de Estudiante (Edad).
*   **Regla de negocio:** El sistema debe permitir el registro de estudiantes cuya edad esté entre 16 y 65 años inclusive.
*   **Variable de entrada ($x$):** Edad del estudiante (valor numérico entero).
*   **Condición lógica:** $16 \le x \le 65$.

### Técnica de prueba más adecuada
La técnica más adecuada es el **Análisis de Valor Límite (AVL)** [1, 2].

### Justificación de la técnica
El requerimiento establece un **rango numérico definido** [1]. El Análisis de Valor Límite es idóneo porque se basa en probar los valores en las fronteras exactas del rango acotado ($a$ y $b$) y los valores justo arriba y justo abajo de estos [2], que es donde estadísticamente ocurren la mayoría de los defectos lógicos de programación.

### Diseño de los Casos de Prueba (AVL)
=======
| ID | Tipo de Límite | Valor (Edad) | Pasos de la Prueba | Resultado Esperado |
| :--- | :--- | :---: | :--- | :--- |
| **CP-01** | Límite Inferior - 1 (Inválido) | **15** | 1. Ingresar al formulario de registro.<br>2. Ingresar la edad: **15**.<br>3. Enviar el registro. | **Rechazado.** El sistema bloquea el registro y muestra error. |
| **CP-02** | Límite Inferior (Válido) | **16** | 1. Ingresar al formulario de registro.<br>2. Ingresar la edad: **16**.<br>3. Enviar el registro. | **Aceptado.** El sistema procesa el formulario y permite el registro. |
| **CP-03** | Límite Superior (Válido) | **65** | 1. Ingresar al formulario de registro.<br>2. Ingresar la edad: **65**.<br>3. Enviar el registro. | **Aceptado.** El sistema procesa el formulario y permite el registro. |
| **CP-04** | Límite Sup. + 1 (Inválido) | **66** | 1. Ingresar al formulario de registro.<br>2. Ingresar la edad: **66**.<br>3. Enviar el registro. | **Rechazado.** El sistema bloquea el registro y muestra error. |

### RF-02 Código de Estudiante
1. Análisis del requerimiento
El código del estudiante debe cumplir tres condiciones:
- Tener exactamente 8 caracteres
- Iniciar con la letra "E"
- Los 7 caracteres restantes deben ser numéricos
Esto significa que cualquier código que no cumpla alguna de esas reglas debe ser rechazado por el sistema.

### Técnica de Prueba Aplicada
Técnica seleccionada: Partición de equivalencia

### Justificación:
El requerimiento define reglas claras sobre el formato del código. Mediante partición de equivalencia se pueden dividir los datos de entrada en clases válidas e inválidas, reduciendo la cantidad de pruebas necesarias mientras se verifica el comportamiento del sistema.

### Casos de Prueba Diseñados
| ID    | Entrada   | Descripción                                | Resultado Esperado |
|-------|-----------|---------------------------------------------|--------------------|
| CP-03 | E1234567  | Código válido que cumple las 3 condiciones  | Registro aceptado  |
| CP-04 | 12345678  | No inicia con "E"                           | Registro rechazado |
| CP-05 | E123456   | Menos de 8 caracteres                       | Registro rechazado |
| CP-06 | E12345678 | Más de 8 caracteres                         | Registro rechazado |
| CP-07 | E1234A67  | Contiene una letra en la parte numérica     | Registro rechazado |
| CP-08 | e1234567  | Inicia con "e" minúscula                    | Registro rechazado |

=======
### 2. Técnica de prueba más adecuada
La técnica más adecuada es el **Análisis de Valor Límite (AVL)** [1, 2].

### 3. Justificación de la técnica
El requerimiento establece un **rango numérico definido** [1]. El Análisis de Valor Límite es idóneo porque se basa en probar los valores en las fronteras exactas del rango acotado ($a$ y $b$) y los valores justo arriba y justo abajo de estos [2], que es donde estadísticamente ocurren la mayoría de los defectos lógicos de programación.


## 5. Trazabilidad

## 6. Gestion de Versiones (GitFlow)

