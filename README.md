# Invitación Digital — Brindis Especial (Primavera Events Group)

Invitación digital de una sola página, lista para desplegar en GitHub Pages o abrir localmente.

## Estructura

```
invitacion brindis/
├── index.html            ← Página principal (todo en uno)
├── assets/
│   ├── sobre.mp4              ← Video de apertura del sobre (silencioso)
│   ├── logo_primavera.png     ← Logotipo Primavera Events Group
│   └── identidadsonora1.mp3   ← Pista oficial de identidad sonora (fase de expectativa)
└── README.md
```

## Colores institucionales usados

Tomados del Manual de Branding en `primavera brain/base_de_datos_primavera.md`:

| Color | Hex |
| --- | --- |
| Rosa Principal | `#F65C7A` |
| Rosa Claro | `#FF8FA3` |
| Oro Noble | `#C9A96E` |
| Gris Suave | `#6D6D6D` |
| Negro Profundo | `#1F1F1F` |

La música es `identidadsonora1.mp3`, una de las 3 pistas oficiales de identidad sonora de PEG (la que se usa específicamente en fase de expectativa/landing, según el manual).

## Flujo de la experiencia

1. **Pantalla 1** → Se muestra el primer frame del video del sobre (cerrado) con el logotipo y un aviso pulsante "Toca para abrir tu invitación".
2. Al tocar, se reproduce el **video del sobre abriéndose** (sin sonido) y arranca la **pista oficial de identidad sonora** en loop.
3. Al terminar el video, transiciona con fade a la **Lámina de invitación**: logotipo, "Brindis Especial" (sin revelar el motivo — se da a conocer en el evento), anfitriones, fecha, hora, lugar, botón de ubicación (Google Maps) y contador regresivo.
4. Botón de silenciar música (esquina superior derecha) en todo momento.

## Datos del evento

- **Motivo:** No se revela en la invitación (se anuncia en el propio brindis).
- **Anfitriones:** Richard Hernández y Jessy Sandoval.
- **Fecha:** Lunes 3 de agosto de 2026.
- **Hora:** 5:00 p.m. – 6:00 p.m.
- **Lugar:** Centro de Convenciones Presidente — Av. Defensa Nacional #8, Col. Chamilpa, 62210 Cuernavaca, Morelos (dirección verificada en `primavera brain/venues/centro_convenciones_presidente.json` y en `base_de_datos_primavera.md`; no existe un nombre alterno "Salón Presidente" en la base de datos de PEG).

## Cómo verlo localmente

Los navegadores bloquean video/audio por política de `file://`. Sirve la carpeta con un servidor local:

```bash
cd "invitacion brindis"
python -m http.server 8080
```

Y abre `http://localhost:8080`.

## Repositorio

Publicado en [github.com/5410m0n0c001/invitacion-primavera-events-group](https://github.com/5410m0n0c001/invitacion-primavera-events-group).

Para activarlo como página pública: Settings → Pages → Branch `main` / `root` en ese repositorio.

## Notas técnicas

- Sin dependencias externas salvo Google Fonts (Playfair Display + Quicksand).
- Compatible con iOS Safari (`playsinline`, `webkit-playsinline`).
- El contador regresivo apunta a `2026-08-03T17:00:00-06:00` (hora de Cuernavaca, Morelos).
- El botón de ubicación abre una búsqueda de Google Maps con la dirección postal exacta del recinto (Av. Defensa Nacional #8, Col. Chamilpa, 62210 Cuernavaca, Morelos).
