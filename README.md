# Storytelling & Storyboard · Liquid Death × Alien

Presentación web interactiva del **Parcial 01** de Publicidad 2. Es una pieza de una sola
página (`index.html`) que funciona como deck de 24 láminas navegables, con visores modales
para el storyboard y para las referencias de la historia.

**🔗 Ver la presentación:** https://whafonsecav.github.io/publi02_liquit-death/

| | |
|---|---|
| **Asignatura** | Publicidad 2 |
| **Modalidad** | Bogotá Presencial Nocturno · Viernes |
| **Autor** | William H. Fonseca. |
| **Marca** | Liquid Death |
| **Personaje asignado** | Alien (Kzár Xylar) |
| **Sentimiento asignado** | Euforia |
| **Duración de la pieza narrada** | 85 segundos · 17 escenas de 5 s |
| **Cuándo ocurre** | Octubre de 2026 |

---

## De qué se trata

Un falso noticiero global de 85 segundos. Un objeto interestelar frena a propósito antes de
llegar a la Tierra, el Pentágono pone su mensaje al aire y el mundo escucha a **Xylar**, del
*Tribunal P.E.T.* (Purga Evolutiva Total), anunciar que el plástico no es el asesino: los asesinos son los
habitantes. Mientras los gobiernos se rinden, un movimiento juvenil absurdo llamado
**Alumaxxing** revienta latas de aluminio contra su propia frente, y la ONU acaba enviando al
espacio a una marca de agua. Lo que desactiva la purga no es un argumento: es una lata.

El tono es irónico, sarcástico y oscuro, montado estrictamente como *breaking news* para que
el espectador sienta miedo real antes de que el humor rompa el formato.

---

## Cómo se usa

| Acción | Cómo |
|---|---|
| Avanzar / retroceder | `←` `→`, `↑` `↓`, `PageUp` / `PageDown`, `Espacio`, rueda del mouse o swipe |
| Ir al inicio / final | `Home` / `End` |
| Salto directo a lámina | Clic en los puntos del pie de página |
| Pantalla completa | `F` |
| **Versión resumida** de un acto | Clic sobre el título grande de *La Intro*, *El Nudo* o *El Desenlace* |
| Ampliar una escena del storyboard | Clic sobre la imagen o en *Ver ficha completa* |
| Navegar dentro del visor de escena | `←` `→` · cerrar con `Esc` |
| Abrir el detalle de una referencia | Clic sobre cualquier tarjeta de *Guiños & Referencias* |
| Recorrer las 14 locaciones | Flechas del carrusel o clic en los chips numerados |
| Cerrar la transmisión | Clic o `→` en la última lámina (dispara el glitch) |
| Parar / reanudar el cronómetro | Botón junto al badge `LIVE`, disponible al cerrar la transmisión |

La versión resumida no se anuncia: el título no lleva subrayado, ni color distinto, ni
icono, ni globo de ayuda. Lo único que cambia es el cursor al pasar por encima, para que
quien presenta pueda encontrarla sin que el público vea que hay algo ahí. Cada acto abre
un modal con el mismo relato en un solo párrafo —los mismos hechos, los mismos datos y el
mismo orden que la versión larga, que sigue intacta en la lámina—, pensado para cuando hay
que contar la historia en menos tiempo. Con el resumen abierto las flechas no cambian de
lámina; se cierra con `Esc`, con el botón o tocando fuera.

### En móvil y tablet

El deck es una lámina fija de **1920 × 1164 px** que se escala con `transform`,
así que la maqueta, los recuadros y los tamaños de letra son **idénticos en
cualquier pantalla**: nunca se reordena ni se recorta, solo cambia el zoom.

| Situación | Comportamiento |
|---|---|
| Lámina de conexión | Vive en el mismo marco de 1920 × 1164 que el deck: escala y rota igual |
| Cualquier ancho | La lámina se centra y se escala al viewport **visible** (`visualViewport`), así que la barra del navegador que aparece y desaparece en móvil no descuadra nada |
| Móvil o tablet en **vertical** | La lámina **rota 90°** para aprovechar el lado largo de la pantalla y aparece el aviso *Gira el dispositivo para verlo en horizontal* |
| Móvil o tablet en **horizontal** | Se muestra derecha y a la mayor escala posible |
| Cambio de orientación | Se reajusta solo (`orientationchange`, `resize`, `visualViewport`) |
| Avanzar | Swipe; con la lámina rotada el gesto se remapea al eje físico correcto |
| Doble toque | Entra y sale de pantalla completa |
| Controles | Flechas, chips y botones crecen en pantallas táctiles (`@media (pointer:coarse)`) y se desactivan los estados `:hover`, que en táctil se quedan pegados |

> En **iPhone**, Safari no expone la API de pantalla completa para elementos
> (solo para vídeo), así que el doble toque no puede ocultar la barra del
> navegador. La alternativa es *Compartir → Agregar a pantalla de inicio*: el
> sitio declara `apple-mobile-web-app-capable`, por lo que abierto desde el
> icono se ejecuta sin barra ni pestañas. En Android Chrome y en iPad el doble
> toque sí entra en pantalla completa.

### Enlaces profundos

| URL | Efecto |
|---|---|
| `index.html?s=13` | Abre directamente la lámina 13 |
| `index.html?s=17&scene=4` | Abre la ficha completa de la escena 4 |
| `index.html?s=24&fin=1` | Abre el cierre ya en estado «Fin de la transmisión» |
| `index.html?nb=1` | Salta la pantalla de arranque |
| `index.html?na=1` | Desactiva las animaciones de entrada (útil para capturas) |

---

## Estructura del deck (24 láminas)

| # | Lámina | Fondo |
|---|---|---|
| 01 | Portada · título, datos del ejercicio, personaje y sentimiento asignados | `00. PORTADA` |
| 02 | La marca y el producto · infografía de quién es Liquid Death, su portafolio y cómo comunican | `05. STORYBOARD` |
| 03 | La Trama · **La Intro** (planteamiento) | `01. TRAMA` |
| 04 | La Trama · **El Nudo** (confrontación) | `01. TRAMA` |
| 05 | La Trama · **El Desenlace** (resolución) | `01. TRAMA` |
| 06 | La Trama · **El Tono** · registro dominante + matices + mecanismo en 3 pasos | `01. TRAMA` |
| 07 | **Guiños & Referencias** · 13 tarjetas clicables con datos clave y el hecho real | `01. TRAMA` |
| 08 | Personaje · Demográfico (dossier de 8 campos) | `02. PERSONAJE` |
| 09 | Personaje · Actitudes y Opiniones (6 tarjetas) | `02. PERSONAJE` |
| 10 | Personaje · Intereses (4 tarjetas) | `02. PERSONAJE` |
| 11 | Personaje · Intenciones (4 tarjetas, con el giro destacado) | `02. PERSONAJE` |
| 12 | Escenario · fecha + carrusel de las 14 locaciones | `03. ESCENARIO` |
| 13 | Motivación · Emoción y Sentimiento (los 3 momentos de la euforia) | `04. MOTIVACION` |
| 14 | Motivación · **El Conflicto** · lluvia de 20 ideas que converge en un solo hecho | `04. MOTIVACION` |
| 15 | Storyboard · subportada | `05. STORYBOARD` |
| 16 | Storyboard · escenas 01–03 | `05. STORYBOARD` |
| 17–23 | Storyboard · escenas 04–17, de dos en dos | `05. STORYBOARD` |
| 24 | Cierre · CTA del movimiento → *glitch* → Fin de la transmisión | `05` → `00` |

---

## Decisiones de diseño

### Escenario escalado y zonas seguras

Todo se maqueta sobre un escenario fijo de **1920 × 1164 px** que se escala por `transform`
para caber en cualquier pantalla sin reflow: la lámina ocupa los 1080 px superiores y debajo
quedan 12 px de aire y un pie de página de 72 px. Así el cromo de navegación **nunca se
superpone a la imagen de fondo**.

Cada fondo tiene la lata del producto en un lugar distinto, así que el contenido respeta una
zona segura por fondo:

| Fondo | Zona segura para la información |
|---|---|
| `00. PORTADA` y cierre | 75 % superior (`y ≤ 810`) |
| `01`–`04` (lata a la derecha) | 68 % izquierdo (`x ≤ 1305`) |
| `05. STORYBOARD` | 88 % izquierdo y 85 % superior (`x ≤ 1690`, `y ≤ 918`) |

El resultado se verificó midiendo por JS el rectángulo de cada elemento de cada lámina:
**0 desbordes y 0 textos recortados** en las 24 láminas.

### Color leído de cada fondo

Cada lámina inyecta su propio par de acentos (`--acc`, `--acc2`) y lo heredan encabezados,
filetes, tarjetas, iconos, puntos de navegación y barra de avance:

| Sección | Acentos |
|---|---|
| Portada / Storyboard / Cierre | `#7cf03c` verde ácido + `#2e7bff` azul |
| La Trama | `#4b86ff` azul eléctrico + `#c247e6` magenta |
| Personaje | `#ff2e88` rosa + `#ff8ac4` |
| Escenario | `#ff3b4e` rojo sangre + `#e8bd57` oro |
| Motivación | `#ff6f1f` naranja + `#4fa8ff` azul |

### Tipografía

| Uso | Fuente |
|---|---|
| Logotipo y titulares góticos | **Pirata One** (blackletter) |
| Titulares condensados de noticiero | **Anton** |
| Etiquetas, chips y subtítulos | **Barlow Condensed** |
| Cuerpo de texto | **Inter** |
| Timecodes, códigos y datos | **Space Mono** |

### Sensación 3D sin cortar la imagen

El fondo va sobredimensionado un 2.8 % y deriva con `perspective` + `rotateX/rotateY` guiado
por una curva de Lissajous continua más la posición del puntero. Las variables `--px` / `--py`
se escriben en un único nodo (`#deckwrap`), así que **todas las láminas comparten el mismo
valor en el mismo instante**: al avanzar no se percibe ningún salto ni cambio de encuadre.
El velo, la luz especular y el bloque de texto se mueven en contra para dar profundidad.
Respeta `prefers-reduced-motion`.

### Storyboard

Las 17 escenas se muestran en blanco y negro (`filter: grayscale(1)`) con marco verde, imagen
centrada en 3:4 y un divisor vertical entre escenas. Debajo de cada cuadro van los cuatro
campos del guion recortados a un número fijo de líneas para que la grilla quede pareja; al
hacer clic, la imagen crece y se desplaza a la izquierda con una animación FLIP calculada
desde la posición real de la tarjeta, el fondo se desenfoca y a la derecha entra la ficha
completa: descripción general, escenario, voz en off / diálogos (con el hablante destacado)
y subtítulos maquetados como rótulos de televisión.

### Cronómetro en vivo

Al cargar, el badge `LIVE` se desplaza a la izquierda y de detrás emerge un cronómetro que
corre en tiempo real desde que se abrió la página. En la última lámina, una vez cerrada la
transmisión, sale por la derecha el botón **Parar transmisión**: congela el reloj y cambia el
badge a `FIN`, con opción de reanudar.

---

## La portada en PDF

`Portada_Liquid_Death_x_Alien.pdf` es la lámina de portada como archivo suelto: una sola
página en 16:9 exacto (338,7 × 190,5 mm), con el mismo diseño del deck y un botón que abre
la presentación completa. Pesa 531 KB.

Está **aplanado a propósito**. La primera versión salió en vectores y se llevó al PDF los
modos de fusión del diseño —el grano en `overlay`, el desenfoque cromático del logo en
`screen`—, sus máscaras y sus sombras difusas: 34 grupos de transparencia, 16 máscaras y
modos `Screen` y `Overlay` en un archivo de una página. Varios visores renderizan mal esos
grupos sobre fondo oscuro, y la página titilaba y se quedaba en negro. Ahora la portada se
rasteriza con Chrome —que sí dibuja bien las fusiones—, se captura a 3× (3840 × 2160), se
reduce a 2560 × 1440 con Lanczos y se guarda en JPEG progresivo q90. El PDF resultante no
tiene **ni un solo** grupo de transparencia, así que no hay nada que un visor pueda
interpretar mal. A 2560 px sobre una hoja de 338 mm son unos 192 ppp: nítido en pantalla,
en proyector y en impresión.

El botón sigue siendo un enlace real: sobre la imagen va un área transparente que produce
la anotación de enlace del PDF. Y debajo del botón está la URL escrita, por si el archivo
se imprime en papel y hay que teclearla.

---

## Carga y rendimiento

**La lámina de conexión precarga de verdad.** No es un adorno: descarga los seis
fondos y los diecisiete bocetos, los decodifica, y solo cuando termina invita a
avanzar. Muestra el conteo real (`14 / 24 imágenes`), el porcentaje y una barra
que se mueve con la descarga, y cada línea del terminal se confirma con un tramo
real del progreso. A partir de ahí, ir y volver entre láminas es instantáneo
porque todo está ya en caché. Si algo no responde, entra igual a los 30 segundos:
nadie queda encerrado en la pantalla de carga.

**El peso bajó de 98 MB a 8,3 MB.** Los fondos se sirven a 2400 px (se ven a
1920) y los bocetos a 1100 px en escala de grises, que es como se muestran
siempre. La descarga completa cabe en una conexión móvil normal.

**La textura de emisión se dimensiona en píxeles de pantalla, no de lámina.**
La trama de línea (`#scan`) y el grano (`#grain`) estaban fijados en píxeles de
la lámina de 1920: al escalarla a 0,32 en un celular, esas líneas de 1 px cada
3 px medían 0,32 px sobre una rejilla de 1 px, y el grano se desplazaba tres
veces por segundo encima. Eso era el parpadeo de interferencia. Ahora el tamaño
se recalcula desde la escala aplicada, así que sobre la pantalla mide lo mismo en
cualquier dispositivo. Además, en pantallas táctiles se apagan la animación del
grano y la deriva 3D del fondo, que reescribían dos variables CSS por frame sobre
una capa a pantalla completa.

---

## Fuentes del contenido

El HTML se genera a partir de los dos entregables del parcial, sin resumir:

- **`Propuesta_Liquid_Death.md`** — trama, personaje principal, escenario y motivación.
- **`Storyboard_Mejorado.xlsx`** — las 17 escenas con escenario, voz en off / diálogos,
  subtítulos y descripción general.

La narración de la Intro, el Nudo y el Desenlace se reescribió en tercera persona omnisciente
para la presentación, conservando todos los hechos del entregable original.

Sobre ese texto se aplican unas normalizaciones, en un solo lugar del generador, para
que el deck hable con una sola voz aunque las fuentes usen términos distintos:

| Norma | Por qué |
|---|---|
| El personaje es el **alien** | El entregable y el storyboard lo llamaban a veces *extraterrestre* y a veces *alienígena*. El personaje asignado del ejercicio es el alien |
| **Tribunal P.E.T.** (Purga Evolutiva Total) | Aparecía como *Tribunal de Purga P.E.T.*; la sigla se explica en la primera mención de cada lámina |
| **Protocolo de Limpieza Planetaria** | Se llamaba *de Asesinato Planetario*, y acabar con la civilización es el primer paso del protocolo, no su objetivo |
| **Octubre de 2026** | Es el cuándo de la historia. Las fechas históricas de los guiños no se tocan |
| **Alegría**, no felicidad | La emoción asignada es la alegría, que escala a euforia |
| Cada voz declara **país e idioma** | Y los subtítulos, que siempre van en español, solo aparecen cuando la voz no está en español |


Las 12 referencias de *Guiños & Referencias* citan hechos verificables: 1I/ʻOumuamua (2017) y
3I/ATLAS (2025), la falla real de telemetría de la Voyager 1 (2023–2024), el telescopio James
Webb, la Sonda Parker, el PET, el sufijo *–maxxing* de internet, el monolito de *2001: Odisea
del espacio* y el de Utah (2020), la Agenda 2030 y sus 17 ODS, las plataformas de video
generativo (Sora, Veo, Runway, Kling, Luma, Pika), la conspiración reptiliana de David Icke,
la emisión de *La guerra de los mundos* (1938), la misión real «Death to Plastic» de la marca
y la regla del video borroso del alien (Patterson–Gimlin 1967, los videos OVNI del Pentágono).

---

## Estructura del repositorio

```
.
├── index.html                     # la presentación completa (HTML + CSS + JS en un archivo)
├── Portada_Liquid_Death_x_Alien.pdf   # la portada como PDF de una página, con enlace al deck
├── .nojekyll                      # sirve las rutas con espacios sin procesar por Jekyll
└── assets/
    ├── img laminas/web/           # 6 fondos de sección (2400 px, JPEG q86)
    ├── img storyboard/web/        # 17 bocetos del storyboard (1100 px, JPEG q80, gris)
    └── logo/                      # logotipos institucionales
```

Los originales de las imágenes (98 MB en PNG y JPEG de cámara) se quedan en la
carpeta de trabajo como archivo; aquí solo viaja la versión web, **8,3 MB en
total**. El deck apunta a `web/` y, si un boceto nuevo todavía no tiene su copia
ligera, cae al original con cualquier extensión.

`index.html` no tiene dependencias de build: solo carga las tipografías desde Google Fonts.
Se puede abrir directamente con doble clic o servir como sitio estático.

Las imágenes de este repositorio están optimizadas para web (98 MB → 14 MB) manteniendo los
nombres de archivo; los originales a máxima resolución viven en la carpeta de trabajo del
proyecto.

---

## Desarrollo local

```bash
python -m http.server 8000
```

Y abrir `http://localhost:8000/`. También funciona abriendo `index.html` directamente desde
el sistema de archivos.

Si se agregan o reemplazan bocetos, basta con guardarlos en `assets/img storyboard/` con el
número de escena (`01` … `17`); el visor prueba las extensiones `.jpeg`, `.jpg`, `.png` y
`.webp`, y muestra un marco de «boceto pendiente» si todavía no existe el archivo.
