# Diana Hair Salon — sitio web

Sitio de una sola página (`index.html`), autocontenido: el HTML, CSS, JavaScript y las fotos (en base64) están todos en un único archivo. No necesita build, ni Node, ni dependencias — se sube tal cual.

## Publicarlo gratis con GitHub Pages

1. **Crea un repositorio nuevo** en GitHub (puede ser público o privado si tienes GitHub Pro; Pages gratis requiere que sea público).
2. **Sube `index.html`** a la raíz del repositorio. Puedes hacerlo por la web ("Add file → Upload files") o por consola:
   ```bash
   git init
   git add index.html
   git commit -m "Primera versión del sitio"
   git branch -M main
   git remote add origin https://github.com/TU-USUARIO/TU-REPO.git
   git push -u origin main
   ```
3. Entra a **Settings → Pages** dentro del repositorio.
4. En "Build and deployment", elige **Source: Deploy from a branch**.
5. En "Branch", selecciona **main** y la carpeta **/ (root)** → Guarda.
6. Espera uno o dos minutos. GitHub te va a mostrar la URL pública, algo como:
   ```
   https://TU-USUARIO.github.io/TU-REPO/
   ```

Listo — esa es la página que puedes compartir en Instagram, WhatsApp, etc.

## Dominio propio (opcional)

Si más adelante Diana quiere algo como `www.dianahairsalon.cl` en vez del link de GitHub:

1. Compra el dominio (Nic Chile, GoDaddy, etc.).
2. En el repositorio, crea un archivo llamado `CNAME` (sin extensión) con una sola línea dentro: el dominio, por ejemplo `dianahairsalon.cl`.
3. En el proveedor del dominio, agrega un registro **CNAME** apuntando a `TU-USUARIO.github.io`.
4. En **Settings → Pages**, pon ese mismo dominio en el campo "Custom domain".

## Actualizar el sitio más adelante

Cada vez que haya un cambio (precios, fotos, cursos nuevos), solo hay que reemplazar `index.html` en el repositorio (subir el archivo nuevo o hacer `git add` + `commit` + `push`) y GitHub Pages lo actualiza solo, normalmente en menos de un minuto.

## Nota técnica

- Las fotos están incrustadas como `base64` dentro del propio HTML, por eso el archivo pesa más de lo normal (~350 KB) pero no depende de ninguna carpeta de imágenes aparte — un solo archivo, cero configuración.
- Las fuentes (Google Fonts) y los íconos se cargan desde CDNs públicos; no se necesita ninguna llave ni configuración adicional.
