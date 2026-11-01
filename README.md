# MisKosikas

App web local para controlar productos de uso diario: consultar sus detalles, llevar el historial de compras y marcar lo que hay que reponer.

## Funciones

- Ficha de producto: nombre, detalle, categorías (etiquetas libres, varias por producto), uso e imagen.
- Historial de compras (fecha, lugar y precio) con botón **Registrar compra**.
- Casilla **Comprar de nuevo**, que se desmarca sola al registrar una compra.
- Buscador por nombre y filtros acumulativos por categoría y por reposición.
- Exportación de lo filtrado a PDF y CSV.
- Copia de seguridad completa (exportar e importar, con imágenes).
- Funciona sin conexión e instalable como app en móvil y ordenador.

## Privacidad

Los datos se guardan solo en el navegador de cada dispositivo (IndexedDB). No se envían a ningún servidor ni a GitHub. Este repositorio contiene únicamente el código.

Cada dispositivo (y cada dirección web) tiene su propia base de datos. Para pasar datos de uno a otro, usa **Datos → Exportar copia** e **Importar copia**.

## Publicar en GitHub Pages

1. Crea un repositorio nuevo en GitHub (con el plan gratuito, público).
2. Sube estos archivos a la raíz: `index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`, `README.md` y `.gitignore`.
3. En el repositorio, ve a **Settings → Pages**. En *Build and deployment* elige **Deploy from a branch**, rama `main` y carpeta `/ (root)`, y guarda.
4. Tras uno o dos minutos la app estará en `https://TU-USUARIO.github.io/NOMBRE-DEL-REPOSITORIO/`.

## Instalar

- **Android (Chrome):** menú ⋮ → *Instalar aplicación* o *Añadir a pantalla de inicio*.
- **iPhone (Safari):** Compartir → *Añadir a pantalla de inicio*.
- **Ordenador (Chrome/Edge):** icono de instalar en la barra de direcciones.

## Actualizar

Edita `index.html`, cambia el número de versión en `sw.js` (`miskosikas-v1` → `miskosikas-v2`) y súbelo de nuevo. Las copias instaladas se renuevan al abrirlas con conexión.

## Estructura

| Archivo | Función |
| --- | --- |
| `index.html` | La app completa (HTML, CSS y JavaScript) |
| `manifest.webmanifest` | Datos de instalación como app |
| `sw.js` | Service worker para uso sin conexión |
| `icon-192.png`, `icon-512.png` | Iconos de la app |
