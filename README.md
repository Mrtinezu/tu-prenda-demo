# Pieta Tactil
### La información de una prenda, al alcance de más personas.

**Escanea. Escucha. Pregunta. Elige.**

Pieta Tactil es una experiencia móvil de moda accesible que convierte el QR de una prenda en un punto de acceso a sus detalles: diseño, colores, talla, materiales y cuidados. Combina fotografías, interacción por voz mediante **Web Speech API** y consultas por texto, con modos pensados para personas ciegas, personas sordas y público general.

El objetivo es sencillo: que más personas puedan explorar una prenda y tomar decisiones de compra con mayor autonomía, desde su propio teléfono.

**[Probar Pieta Tactil](https://mrtinezu.github.io/tu-prenda-demo/)** · [Explorar las prendas piloto](#tres-prendas-una-misma-experiencia) · Desarrollado por [Mrtinezu](https://github.com/Mrtinezu)

---

## Una etiqueta puede decir poco. Una experiencia accesible puede contar más.

El aspecto de una prenda suele comunicarse a través de fotografías, escaparates y detalles que no siempre son accesibles para todos. Una talla o una composición tampoco explican por sí solas dónde está un estampado, qué colores combina la prenda o cómo es su corte.

Pieta Tactil propone llevar esa información al canal que cada persona prefiera: **voz, texto o imagen**, dentro de una interfaz móvil que se abre al escanear el QR, sin instalar una aplicación.

## Una experiencia que se adapta a la persona

| Modo | Experiencia |
| --- | --- |
| **Personas ciegas** | Descripción hablada y consultas por voz desde una sola pantalla. Al terminar la descripción, tocar la pantalla activa el micrófono para facilitar la interacción. |
| **Personas sordas** | Acceso directo a las fotos, descripción escrita y consultas por texto, sin depender del audio. |
| **General** | Exploración visual y asistente de voz. Cada persona puede elegir cómo conocer la prenda. |

El modo de accesibilidad se recuerda en el dispositivo y puede cambiarse desde la propia interfaz.

## Del QR a una conversación sobre la prenda

1. **Escanea el QR:** se abre la prenda correspondiente.
2. **Conoce sus detalles:** escucha la descripción o explora la ficha visual.
3. **Haz una pregunta:** «¿Cuál es el diseño?», «¿De qué material es?» o «¿Cómo la cuido?».
4. **Recibe una respuesta concreta:** la información se adapta a la prenda seleccionada.

Las descripciones priorizan lo que ayuda a identificar y evaluar la pieza: apariencia, talla, material y características relevantes. Cuando un dato de cuidados necesita confirmación, la experiencia orienta a consultar la etiqueta y, si no ofrece la información, al personal de la tienda.

## Tres prendas, una misma experiencia

| Prenda piloto | Explorar |
| --- | --- |
| Varsity Perú roja | [Abrir experiencia](https://mrtinezu.github.io/tu-prenda-demo/?prenda=pieta-varsity-peru-rojo) |
| Polo PLAY blanco | [Abrir experiencia](https://mrtinezu.github.io/tu-prenda-demo/?prenda=pieta-cdg-basic-heart-blanco) |
| Casaca Stüssy azul | [Abrir experiencia](https://mrtinezu.github.io/tu-prenda-demo/?prenda=pieta-stussy-capucha-azul) |

Cada prenda tiene su propio enlace y QR. El piloto permite mostrar el recorrido completo: escaneo, selección de accesibilidad, descripción y consultas.

## Tecnología al servicio de la experiencia

- **Web móvil:** HTML, CSS y JavaScript, con una primera pantalla de voz que mantiene los controles visibles.
- **Entrada de voz:** reconocimiento del navegador mediante Web Speech API, con soporte para variantes de preguntas y transcripciones alternativas.
- **Respuestas habladas:** audios de demostración integrados para las descripciones y preguntas frecuentes.
- **Consultas por texto:** el mismo contenido de producto disponible desde la ficha visual.
- **Identificación por QR:** enlaces con un identificador de prenda para abrir el contenido correspondiente.
- **Validación del piloto:** 393 casos de preguntas de prueba, comprobaciones del enlace entre respuestas y audios, y protección frente a toques que interrumpan la descripción inicial en modo para personas ciegas.

## De piloto funcional a asistente conectado por API

**Esta versión ya permite probar la experiencia con tres prendas.** Las respuestas actuales utilizan un catálogo de preguntas frecuentes, reglas de reconocimiento de intenciones y voz pregrabada.

La siguiente etapa propuesta es conectar un modelo de IA mediante una API, a través de un backend que consulte la información autorizada de cada prenda. Esto permitiría ampliar la conversación manteniendo el catálogo como referencia y evitando inventar características del producto.

La evolución del producto contempla:

- **IA conectada al catálogo:** preguntas más abiertas y respuestas vinculadas a la pieza seleccionada.
- **Voz natural:** integración de reconocimiento y síntesis de voz según las necesidades del piloto.
- **Gestión de prendas:** incorporación de nuevas fichas y generación de sus QR.
- **Pruebas con usuarios:** evaluación con personas ciegas y sordas para mejorar interacción, claridad y autonomía.

Estas capacidades describen la hoja de ruta; la demo pública actual todavía no utiliza un modelo generativo remoto.

## Probar y ejecutar

Abre la [demo HTTPS](https://mrtinezu.github.io/tu-prenda-demo/) desde un móvil. Para preguntar por voz, concede el permiso del micrófono cuando el navegador lo solicite. La disponibilidad del reconocimiento depende del dispositivo y navegador.

El archivo `index.html` contiene la interfaz, los scripts, las fotografías y los audios del piloto. GitHub Pages publica el sitio desde la raíz de `main`.

La talla M es la selección de demostración. Las fichas no garantizan stock, precios vigentes ni condiciones de compra. El prototipo requiere evaluación de accesibilidad con usuarios y no declara una certificación de conformidad.

## Privacidad y seguridad

La demo no incluye claves de API ni un backend propio. Las conversaciones no se guardan de forma persistente por su código; la preferencia de accesibilidad se conserva localmente. El reconocimiento de voz puede utilizar servicios del proveedor del navegador.

El código y los recursos publicados son accesibles al visitante. Las credenciales de futuras integraciones deberán mantenerse en el servidor. Consulta [SECURITY.md](SECURITY.md) y las exclusiones de archivos en `.gitignore`.

## Autoría y recursos

© 2026 Mrtinezu. Todos los derechos reservados sobre las contribuciones originales que correspondan al autor. La publicación del repositorio permite mostrar y evaluar el prototipo; no concede una licencia abierta de reutilización. Consulta [LICENSE](LICENSE).

Las fotografías, marcas, tipografías y materiales de terceros conservan sus respectivos titulares y condiciones. Su uso en el piloto no implica afiliación ni respaldo comercial. Consulta [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).

