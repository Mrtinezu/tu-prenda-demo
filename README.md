# Tu prenda

Demo móvil de información de prendas por QR, con descripciones de voz, fotos y preguntas frecuentes.

**[Abrir la demo](https://mrtinezu.github.io/tu-prenda-demo/)** · Desarrollado por [Mrtinezu](https://github.com/Mrtinezu)

## Cómo probarla

1. Abre uno de los enlaces de prendas o escanea su QR.
2. En modo general, toca la esfera para escuchar la descripción y el botón del micrófono para preguntar.
3. Toca la tarjeta de la prenda para ver sus fotos y consultar por texto.
4. En Accesibilidad puedes cambiar de modo en cualquier momento.

| Prenda piloto | Enlace |
| --- | --- |
| Varsity Perú roja | [Ver prenda](https://mrtinezu.github.io/tu-prenda-demo/?prenda=pieta-varsity-peru-rojo) |
| Polo PLAY blanco | [Ver prenda](https://mrtinezu.github.io/tu-prenda-demo/?prenda=pieta-cdg-basic-heart-blanco) |
| Casaca Stüssy azul | [Ver prenda](https://mrtinezu.github.io/tu-prenda-demo/?prenda=pieta-stussy-capucha-azul) |

## Modos de accesibilidad

- **General:** asistente de voz y ficha con fotos y consultas por texto.
- **Personas ciegas:** una pantalla de voz. Una vez terminada la descripción, tocar la pantalla activa el micrófono. La descripción inicial queda protegida frente a esos toques para evitar cortes accidentales.
- **Personas sordas:** acceso directo a la ficha visual y consultas por texto, sin reproducción de voz.

La compatibilidad con lectores de pantalla, permisos, audio y reconocimiento de voz depende del navegador y dispositivo. El prototipo todavía requiere pruebas de accesibilidad con usuarios; no declara una certificación de conformidad.

## Qué hace esta versión

Las respuestas se seleccionan a partir de preguntas frecuentes e identificación local de palabras e intenciones, con algunas variantes y preguntas de seguimiento. Los audios están pregrabados e incluidos en el HTML. No hay un modelo generativo conectado ni una API de IA de pago.

La talla M es una selección de demostración. Las fotos y los datos del catálogo son referencias para el piloto; no representan disponibilidad, stock ni precios vigentes. Para comprar, verifica los datos de la pieza concreta con el vendedor.

## Estructura y publicación

- `index.html`: demo autocontenida; incluye los estilos, JavaScript, fotos y audios.
- `.nojekyll`: indica que GitHub Pages debe servir los archivos sin procesarlos con Jekyll.
- `.gitignore`: excluye credenciales y archivos locales de futuras incorporaciones.
- `LICENSE`: reserva de derechos sobre las contribuciones originales.
- `THIRD_PARTY_NOTICES.md`: procedencia de fotos, datos, marcas y otros recursos.
- `SECURITY.md`: manejo de credenciales y comunicación de problemas de seguridad.

La publicación utiliza GitHub Pages desde `main`, en la raíz del repositorio. Puedes descargar `index.html` para ver la interfaz; para probar el micrófono, usa la URL HTTPS y concede el permiso cuando el navegador lo solicite.

## Privacidad y credenciales

- Esta versión no incorpora claves de API ni un backend propio.
- Las consultas y respuestas no se guardan de forma persistente por el código de la demo. La preferencia de accesibilidad se conserva localmente mediante `localStorage`.
- El reconocimiento de voz lo proporciona el navegador y puede procesar el audio en servicios de su proveedor. No debe asumirse que funciona sin conexión.
- La tipografía se solicita a Google Fonts y el alojamiento lo proporciona GitHub Pages; estas solicitudes están sujetas a las políticas de sus proveedores.
- El código y los recursos de este repositorio son públicos. Nunca debe colocarse una clave privada en HTML, JavaScript ni archivos publicados. Una futura API de IA deberá usar un backend con las credenciales del lado del servidor.

Consulta [SECURITY.md](SECURITY.md) para las precauciones de mantenimiento.

## Autoría y uso

© 2026 Mrtinezu. Todos los derechos reservados sobre las contribuciones originales que correspondan al autor. Este repositorio público se comparte para mostrar y evaluar el prototipo; no se concede una licencia abierta de reutilización. Consulta [LICENSE](LICENSE).

Las fotos, nombres comerciales, marcas y materiales de terceros conservan sus respectivos titulares y condiciones. Su presencia no implica afiliación ni autorización comercial. Los detalles de procedencia y alcance están en [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).

