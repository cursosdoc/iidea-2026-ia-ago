# Capacitación en IA · Fundación Nikols

Sitio web (GitHub Pages) para alojar los recursos de la capacitación en Inteligencia Artificial
aplicada al emprendimiento — Fundación Nikols / IIDEA, agosto 2026.

Es una landing page estática, sin dependencias. Todo está en `index.html`.

## Publicar en GitHub Pages

1. Crea un repositorio en GitHub (por ejemplo `iidea-2026-ia-ago`) y sube estos archivos:

   ```bash
   git init
   git add .
   git commit -m "Sitio de la capacitación en IA"
   git branch -M main
   git remote add origin https://github.com/<tu-usuario>/<tu-repo>.git
   git push -u origin main
   ```

2. En GitHub, ve a **Settings → Pages**.
3. En **Source**, elige la rama `main` y la carpeta `/ (root)`. Guarda.
4. En uno o dos minutos el sitio estará disponible en:
   `https://<tu-usuario>.github.io/<tu-repo>/`

El archivo `.nojekyll` ya está incluido para que GitHub Pages sirva el sitio sin procesarlo con Jekyll.

## Agregar los recursos después de cada clase

Todo se controla desde un solo lugar: el arreglo `classes` dentro de `index.html`
(al final del archivo, en la etiqueta `<script>`). Cada clase se ve así:

```js
{ n: 1, day: 12, weekday: "Miércoles", zoom: null, password: null, slides: null },
```

Para publicar un recurso, reemplaza el `null` correspondiente:

- **`zoom`** → enlace de la reunión de Zoom, ej.: `zoom: "https://zoom.us/j/123456789"`
- **`password`** → contraseña para ver la grabación, ej.: `password: "aB3$x9"`
- **`slides`** → enlace a las diapositivas, ej.: `slides: "https://docs.google.com/presentation/..."`

Mientras el valor sea `null`, la página muestra automáticamente la etiqueta
**"Por agregar tras la clase"**. Guarda el archivo, haz `commit` y `push`, y el sitio se
actualiza solo.

## Calendario de clases

| Clase | Fecha | Día |
|------|-------|-----|
| 1 | 12 de agosto de 2026 | Miércoles |
| 2 | 14 de agosto de 2026 | Viernes |
| 3 | 15 de agosto de 2026 | Sábado |
| 4 | 19 de agosto de 2026 | Miércoles |
| 5 | 21 de agosto de 2026 | Viernes |
| 6 | 22 de agosto de 2026 | Sábado |
