# Seguridad

## Alcance de la versión publicada

La versión actual es una demo estática con audios pregrabados y respuestas locales a preguntas frecuentes. No incluye una API de IA, autenticación, base de datos ni un servidor propio.

En la revisión del 12 de noviembre de 2026 de los archivos publicados y de las dos revisiones de publicación examinadas no se encontraron claves de API, tokens de acceso ni claves privadas mediante inspección del código y búsqueda de patrones habituales. Esto describe el alcance de esa revisión; no constituye una garantía de ausencia de cualquier vulnerabilidad.

## Manejo de credenciales

- Nunca introducir claves privadas en `index.html`, scripts del navegador, URLs, audios, imágenes, README ni archivos de configuración públicos.
- Mantener las credenciales futuras en variables de entorno de un backend o en un gestor de secretos.
- `.gitignore` excluye archivos comunes de credenciales, pero no oculta archivos ya rastreados, no borra el historial ni impide incrustar una clave dentro de otro archivo.
- Antes de publicar, revisar el resultado final del empaquetado, además del código fuente. Todo lo que recibe el navegador es accesible al visitante.
- No pegar tokens, claves o datos personales en issues, capturas ni registros de diagnóstico.

## Si se expone una credencial

1. Revocarla o rotarla de inmediato en el proveedor.
2. Retirarla de los archivos publicados y actualizar el despliegue.
3. Evaluar los accesos y el alcance de la exposición.
4. Si hace falta limpiar el historial, coordinarlo antes de reescribirlo. Quitar una línea del último commit no elimina las versiones anteriores.

Referencia: [Eliminar datos confidenciales de un repositorio](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/removing-sensitive-data-from-a-repository).

## Comunicar un problema

Contactar al responsable mediante una vía privada que figure en el perfil público de [Mrtinezu](https://github.com/Mrtinezu). Si no hay una vía privada disponible, abrir únicamente un issue solicitando un canal privado de contacto, sin publicar la vulnerabilidad, credenciales ni instrucciones de explotación.

Describir la página o archivo afectado, el comportamiento observado y cómo reproducirlo con datos de prueba.

