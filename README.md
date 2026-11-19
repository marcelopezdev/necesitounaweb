# NecesitoUnaWeb Studio

Sitio web de NecesitoUnaWeb Studio, un estudio de desarrollo a medida en Paraguay. Presenta los servicios, el proceso de trabajo y un formulario para pedir presupuesto por WhatsApp.

Es una página estática de un solo archivo, sin frameworks ni paso de compilación.

## Qué incluye

- Hero con palabra rotativa y una ventana de navegador animada.
- Marquesina de servicios.
- Lista de servicios numerados, con efectos al pasar el mouse.
- Sección de trabajos.
- Proceso en cuatro pasos, con una línea que avanza al hacer scroll.
- Diagnóstico exprés: el visitante marca su situación y recibe una recomendación, con un botón que abre WhatsApp con el mensaje armado.
- Modalidades de contratación: proyecto cerrado y desarrollo mensual.
- Formulario de contacto que genera un mensaje listo para enviar por WhatsApp.

Otros detalles:

- Diseño responsive, probado en celular y escritorio.
- Respeta la preferencia del sistema "reducir movimiento" y desactiva las animaciones cuando está activa.
- Controles accesibles con teclado y foco visible.

## Estructura

```
.
├── index.html   # HTML, CSS y JavaScript en un solo archivo
└── README.md
```

## Configuración

Antes de publicar, editá estas tres variables al inicio del bloque `<script>` de `index.html`:

| Variable | Qué es | Ejemplo |
| --- | --- | --- |
| `WHATSAPP` | Número en formato internacional, sin `+` ni espacios | `595981123456` |
| `WHATSAPP_VISIBLE` | Número como se muestra en la página | `+595 981 123 456` |
| `EMAIL` | Correo de contacto | `hola@necesitounaweb.com.py` |

También reemplazá por tus proyectos reales las tres tarjetas de ejemplo de la sección **Trabajos**.

## Probar en local

Opción simple: abrí `index.html` en el navegador.

Opción con servidor local, desde la carpeta del proyecto:

```bash
python3 -m http.server 8000
```

Después entrá a `http://localhost:8000`.

## Despliegue en Cloudflare

El sitio es estático, así que no necesita comando de compilación.

1. En el panel de Cloudflare, andá a **Workers y Pages** y creá un proyecto.
2. Elegí subir los archivos directamente y arrastrá la carpeta del proyecto.
3. Desplegá. Cloudflare te da una dirección `.pages.dev`.
4. Para usar un dominio propio, agregalo en **Dominios personalizados** dentro del proyecto.

También podés conectar este repositorio de GitHub. En ese caso dejá el comando de compilación vacío y usá la raíz del repositorio como directorio de salida.

## Tecnologías

- HTML5, CSS3 y JavaScript sin dependencias.
- Tipografías de Google Fonts: Bricolage Grotesque, DM Sans e Instrument Serif.

## Cómo funciona el formulario

El formulario no envía datos a ningún servidor. Valida nombre y teléfono, arma el mensaje y genera un enlace `https://wa.me/` con el texto ya cargado. El visitante lo envía desde su WhatsApp.

Si más adelante querés recibir los pedidos por correo o en una planilla, hay que sumar un backend, por ejemplo una función de Cloudflare.

## Licencia

Pendiente de definir.

## Contacto

NecesitoUnaWeb Studio. Gran Asunción, Paraguay.
