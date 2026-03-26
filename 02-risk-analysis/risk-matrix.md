# Risk Matrix

| ID | Categoría | Riesgo | Probabilidad | Impacto | Nivel | Mitigación (Pruebas) |
|----|-----------|--------|--------------|---------|-------|----------------------|
| R1 | Funcional | El pago funciona pero el pedido no se guarda | 3 | 5 | 15 | Probar el flujo completo de checkout y validar que el pedido se registre correctamente después del pago |
| R2 | Seguridad | Los datos del usuario pueden filtrarse | 2 | 5 | 10 | Verificar que los datos sensibles no se muestren en pantalla, logs o errores |
| R3 | Funcional | El carrito pierde productos | 4 | 4 | 16 | Probar agregar, quitar y mantener productos en el carrito al navegar o recargar |
| R4 | Performance | La app se vuelve lenta | 3 | 3 | 9 | Medir tiempos de respuesta en búsqueda, carrito y checkout |
| R5 | Fiabilidad | El stock no coincide | 3 | 4 | 12 | Probar compras con stock bajo y validación antes de confirmar pedido |