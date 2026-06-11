# 💌 Dedicatorias QR — Carta digital con foto, texto y canción

## ¿Qué hace esto?

- **`index.html`** → tu **editor**. Aquí escribes la dedicatoria, subes la foto y la canción, y generas el QR.
- **`postal.html`** → la **vista del destinatario**. Es lo que se abre cuando alguien escanea el QR.

Todo el contenido (foto, texto, canción) viaja **comprimido dentro del enlace del QR**. No necesitas base de datos ni servidor: con tener estos 2 archivos publicados en internet, ya funciona.

---

## 🚀 Publicarlo (5 minutos, gratis)

### Opción A — GitHub Pages (recomendado, lo más simple)

1. Sube `index.html` y `postal.html` a tu repositorio en GitHub (en la raíz, o en una carpeta).
2. Ve a tu repo → **Settings** → **Pages**.
3. En "Source" selecciona la rama `main` (o `master`) y la carpeta `/ (root)`.
4. Guarda. Espera 1-2 minutos.
5. GitHub te dará una URL tipo:
   ```
   https://tuusuario.github.io/turepo/index.html
   ```
6. Abre esa URL en tu celular o computadora → ese es tu **editor**.

### Opción B — Vercel (tu dominio actual)

1. En tu proyecto de Vercel, asegúrate de que `index.html` y `postal.html` estén en la carpeta `public/` (o en la raíz si es un proyecto estático simple).
2. Haz `git push` — Vercel despliega automáticamente.
3. Tu editor quedará en:
   ```
   https://tudominio.vercel.app/index.html
   ```
   y la postal en:
   ```
   https://tudominio.vercel.app/postal.html
   ```

> Ambas opciones sirven. Vercel es más rápido para actualizaciones, GitHub Pages es más simple para empezar. **No necesitas elegir solo una** — puedes tener ambas activas.

---

## ✅ Cómo usarlo (para ti, como negocio)

1. Abre tu **editor publicado** (la URL de `index.html`).
2. Pestaña **✏️ Editar**:
   - Sube la foto del cliente (se comprime automáticamente).
   - Escribe el nombre, la dedicatoria y la firma.
   - Sube el MP3 de la canción (opcional).
3. Presiona **💾 Guardar y listo**.
4. Ve a la pestaña **📲 QR**.
5. Presiona **⬇️ Descargar QR** — obtienes una imagen PNG lista para imprimir o enviar.
6. Envíasela a tu cliente. Al escanearla, verá la postal **exactamente como la diseñaste**, con foto, texto y canción reproducible.

---

## ⚠️ Límites importantes

- Todo viaja dentro del QR/enlace, así que:
  - **Fotos**: se comprimen automáticamente a máx. 800px y calidad media. Normalmente quedan en 50–250 KB.
  - **Audio (MP3)**: idealmente menos de 3-5 MB. Archivos más grandes generan QR muy densos que algunos celulares antiguos no leen bien.
  - El editor te avisa si el contenido es demasiado grande (pestaña QR, mensaje en amarillo/rojo).

- **Recomendación para audio**: usa un fragmento corto (30-60 segundos) de la canción en MP3 a baja calidad (ej. 96-128kbps), comprimido con alguna herramienta online gratuita como `cloudconvert.com` antes de subirlo.

---

## 🎨 Personalización

Ambos archivos usan las mismas variables de color al inicio del `<style>`:

```css
:root {
  --rose: #c0392b;   /* color principal */
  --gold: #b8860b;   /* acentos dorados */
  --cream: #fdf6f0;  /* fondo */
  --dark: #2c1a1a;   /* texto */
}
```

Cambia estos valores para adaptar la paleta a tu marca/emprendimiento.

---

## 🔁 Cada postal es independiente

Cada vez que generas un QR para un cliente nuevo:

1. En el editor, borra los campos del cliente anterior (o simplemente reemplázalos).
2. Sube la nueva foto/canción.
3. Guarda y descarga el nuevo QR.

El QR de cada cliente es único — el contenido vive **dentro del propio QR**, no se sobrescribe nada en el servidor.
