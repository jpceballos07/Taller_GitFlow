# Documento de Pruebas

## 1. Descripcion del Sistema

## 2. Requerimientos a Evaluar
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
ID	     Entrada 	Descripción	                                Resultado Esperado
CP-03	   E1234567	Código válido que cumple las 3 condiciones	Registro aceptado
CP-04	   12345678	No inicia con "E"	                          Registro rechazado
CP-05	   E123456	Menos de 8 caracteres	                      Registro rechazado
CP-06	   E12345678	Más de 8 caracteres	                      Registro rechazado
CP-07	   E1234A67	 Contiene una letra en la parte numérica	  Registro rechazado
CP-08	   e1234567	 Inicia con "e" minúscula	                  Registro rechazado

## 3. Tecnicas de Prueba Aplicadas

## 4. Casos de Prueba Diseñados

## 5. Trazabilidad

## 6. Gestion de Versiones (GitFlow)
