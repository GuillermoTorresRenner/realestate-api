# Workflows en github actions

# Equipo 2

## integrantes:

- **Francisco Leiva**
- **Guillermo Torres**

### ¿Qué importancia tiene probar en múltiples entornos de Node.js?

- Asegura compatibilidad con diferentes versiones utilizadas por los usuarios o entornos de producción.
- Permite detectar errores específicos de versiones antiguas o nuevas de Node.js que podrían pasar desapercibidos en pruebas locales.
- Garantiza mayor robustez y estabilidad del proyecto ante futuras actualizaciones.

### ¿Por qué es importante validar la salida de una API desde un workflow?

- Verifica que los cambios en el código no rompen las respuestas esperadas por los consumidores de la API.
- Asegura la integridad del contrato (por ejemplo, formato JSON, códigos de estado, headers) antes del despliegue.

### ¿Qué pasos podrías agregar si fueras a hacer despliegue a producción?

- Añadir un paso de aprobación manual para despliegues controlados.
- construir una build del proyecto
- containerizar el proyecto
- cambiar configuraciones de entorno con distintos archivcos de entornos (que luego serán secrets en github)
- aplicar pruebas de seguridad estáticas y dinámicas

### ¿Qué limitaciones tiene GitHub Actions y cómo las enfrentarías?

- **Tiempo de ejecución limitado en planes gratuitos:** reducir tiempos optimizando pasos, cacheando dependencias y paralelizando trabajos.
- **Recursos de ejecución limitados:** usar runners auto-hospedados si se necesita más control o capacidad.
- **Seguridad de acciones externas:** usar versiones fijas o validarlas con `SHA` para evitar código malicioso.

---

## Caso de éxito en una de las ejecuciones de la matrix

![success](/success.png)

## Error de testing si se hace un cambio en la ruta del test

![error](/error_cambio_ruta.png)
