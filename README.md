# 🕒 Timer Pastel

Un reloj digital minimalista con estética pastel, hecho con **HTML, CSS y JavaScript puro** (sin frameworks ni dependencias). Todo funciona en un único archivo: `reloj1.html`.

## ✨ Características

- 🕓 Muestra la hora actual en formato **HH:MM:SS** (24 horas)
- ✨ Dos puntos centrales parpadeantes (efecto de reloj clásico)
- 📅 Fecha completa en español (día de la semana, número y mes)
- 🌍 Badge con la **zona horaria** detectada automáticamente del sistema
- 🎨 Fondo degradado pastel con tarjeta central y sombra suave
- 📱 Diseño totalmente responsivo (tipografía y espaciado con `clamp()` y unidades `vw`)
- 🔄 Actualización en tiempo real cada segundo

## 🚀 Uso

No requiere instalación ni dependencias. Solo:

1. Descarga el archivo `reloj1.html`
2. Ábrelo directamente en tu navegador (doble clic o `Ctrl/Cmd + O`)

```bash
# Alternativamente, desde una terminal:
open reloj1.html      # macOS
start reloj1.html     # Windows
xdg-open reloj1.html  # Linux
```

## 🎨 Personalización

Los colores principales están definidos como variables CSS al inicio del archivo y se pueden editar fácilmente:

```css
:root {
  --bg1: #ffe5ec;          /* color 1 del fondo degradado */
  --bg2: #e0f7fa;          /* color 2 del fondo degradado */
  --card: #ffffff;         /* fondo de la tarjeta */
  --text: #4a4a68;         /* color principal del texto */
  --muted: #9b9bb4;        /* color de la fecha */
  --pink-dark: #ff9eb5;    /* color de los dos puntos */
  --lavender-dark: #b9a3e6;/* color de los segundos */
  --mint: #c1f0dc;         /* fondo del badge de zona horaria */
}
```

También puedes ajustar el formato de la fecha modificando las opciones de `toLocaleDateString`:

```js
const opciones = { weekday: 'long', day: 'numeric', month: 'long' };
dateLabel.textContent = now.toLocaleDateString('es-ES', opciones);
```

## 🛠️ Tecnologías

- HTML5
- CSS3 (variables CSS, `clamp()`, gradientes, animaciones con `@keyframes`)
- JavaScript vanilla (`Date`, `Intl.DateTimeFormat`, `setInterval`)

## 📁 Estructura del proyecto

```
reloj-digital-pastel/
└── reloj1.html   # aplicación completa (HTML + CSS + JS en un solo archivo)
```

## 🌐 Compatibilidad

Funciona en cualquier navegador moderno (Chrome, Firefox, Safari, Edge). No requiere conexión a internet ni servidor: es un archivo estático que se abre localmente. La hora y zona horaria mostradas corresponden a la configuración del sistema del usuario.

## 📄 Licencia

Este proyecto está bajo la licencia MIT.

---

⏰ **Un reloj sencillo, bonito y siempre a tiempo.**
