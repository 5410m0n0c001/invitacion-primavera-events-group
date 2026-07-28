# Invitación Digital — Brindis Especial (Primavera Events Group)

Invitación digital de una sola página, lista para desplegar en GitHub Pages o abrir localmente.

## Estructura

```
invitacion brindis/
├── index.html            ← Página principal (todo en uno)
├── assets/
│   ├── sobre.mp4          ← Video de apertura del sobre (silencioso)
│   ├── logo_primavera.png ← Logotipo Primavera Events Group
│   └── musica.m4a         ← Música de fondo de marca
└── README.md
```

## Flujo de la experiencia

1. **Pantalla 1** → Se muestra el primer frame del video del sobre (cerrado) con el logotipo y un aviso pulsante "Toca para abrir tu invitación".
2. Al tocar, se reproduce el **video del sobre abriéndose** (sin sonido) y arranca la **música de fondo** en loop.
3. Al terminar el video, transiciona con fade a la **Lámina de invitación**: logotipo, "Brindis Especial" (sin revelar el motivo — se da a conocer en el evento), anfitriones, fecha, hora, lugar, botón de ubicación (Google Maps) y contador regresivo.
4. Botón de silenciar música (esquina superior derecha) en todo momento.

## Datos del evento

- **Motivo:** No se revela en la invitación (se anuncia en el propio brindis).
- **Anfitriones:** Richard Hernández y Jessy Sandoval.
- **Fecha:** Lunes 3 de agosto de 2026.
- **Hora:** 5:00 p.m. – 6:00 p.m.
- **Lugar:** Centro de Convenciones Presidente, Cuernavaca, Morelos.

## Cómo verlo localmente

Los navegadores bloquean video/audio por política de `file://`. Sirve la carpeta con un servidor local:

```bash
cd "invitacion brindis"
python -m http.server 8080
```

Y abre `http://localhost:8080`.

## Despliegue en GitHub Pages

```bash
cd "invitacion brindis"
git init
git add .
git commit -m "Invitación digital — Brindis Primavera Events Group"
git remote add origin https://github.com/TU_USUARIO/invitacion-brindis.git
git branch -M main
git push -u origin main
```

Luego activa GitHub Pages en Settings → Pages → Branch `main` / `root`.

## Notas técnicas

- Sin dependencias externas salvo Google Fonts (Playfair Display + Quicksand).
- Compatible con iOS Safari (`playsinline`, `webkit-playsinline`).
- El contador regresivo apunta a `2026-08-03T17:00:00-06:00` (hora de Cuernavaca, Morelos).
- El botón de ubicación abre una búsqueda de Google Maps del recinto (no se tenía un enlace de coordenadas exacto guardado).
