## 🐞 Bug 1 – Error 500 al registrar usuario con campo STATE vacío

Descripción:
Al intentar registrar un usuario sin completar el campo "STATE", el sistema lanza un error HTTP 500 (Internal Server Error).

Pasos:
1. Ir a la página de registro
2. Completar todos los campos obligatorios excepto "STATE"
3. Hacer clic en "Save Account Information"

Resultado esperado:
El sistema debería validar el campo "STATE" y mostrar un mensaje indicando que es obligatorio.

Resultado actual:
El sistema muestra un error HTTP 500 con información técnica del backend.

Severidad:
Alta

Prioridad:
Alta

Impacto:
- El usuario no puede completar el registro
- Mala experiencia de usuario
- Exposición de detalles internos del sistema (stacktrace)

## 🐞 Bug 2 – Pantalla corrupta después de intento fallido de registro

Descripción:
Luego de intentar registrarse y recibir un error, la aplicación muestra una pantalla visualmente corrupta (glitch gráfico).

Pasos:
1. Intentar registrarse sin completar todos los campos obligatorios
2. Recibir error en el registro
3. Volver a la pantalla principal

Resultado esperado:
La aplicación debería redirigir correctamente o mostrar una pantalla funcional.

Resultado actual:
La interfaz se muestra rota y no usable.

Severidad:
Alta

Impacto:
- El usuario no puede continuar navegando
- Mala experiencia de usuario
- Pérdida de confianza en la aplicación

## 🚨 Riesgo – Usuario bloqueado sin posibilidad de acceso

Descripción:
Debido a errores en el registro, un usuario nuevo no puede crear cuenta ni acceder al sistema.

Impacto:
- Bloqueo total del flujo de usuario
- Pérdida de potenciales clientes
- Impacto directo en el negocio