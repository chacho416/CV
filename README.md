# 📄 CV Web — Hugo Nicolas Pulido Moreno

Sitio web de currículum vitae desarrollado con **HTML y CSS puro**, sin frameworks ni dependencias externas. Basado en el diseño original del CV en PDF, adaptado a formato web responsivo con dos columnas.

---

## 🗂️ Estructura del proyecto

```
cv-web/
├── index.html       # Archivo principal (HTML + CSS en un solo archivo)
└── README.md        # Este archivo
```

> Todo el CSS está embebido dentro del `<style>` en el `<head>` del archivo HTML, por lo que no se necesita ningún archivo adicional para que funcione.

---

## 🚀 Cómo usar

1. Descarga o clona el repositorio.
2. Abre `index.html` directamente en cualquier navegador moderno (Chrome, Firefox, Edge, Safari).
3. No se requiere servidor, instalación ni conexión a internet (excepto para cargar las fuentes de Google Fonts).

```bash
# Ejemplo con VS Code Live Server
code .
# Click derecho en index.html → "Open with Live Server"
```

---

## 📸 Cambiar la foto de perfil

El avatar actual es un placeholder SVG. Para reemplazarlo con una foto real:

1. Localiza este bloque en `index.html`:

```html
<div class="header-photo">
  <svg class="avatar-svg" ...> ... </svg>
</div>
```

2. Reemplaza el `<svg>` con una etiqueta `<img>`:

```html
<div class="header-photo">
  <img src="foto.jpg" alt="Hugo Nicolas Pulido Moreno"/>
</div>
```

3. Coloca `foto.jpg` en la misma carpeta que `index.html`.

---

## 🎨 Personalización

### Colores
Todos los colores se controlan desde las variables CSS en `:root` al inicio del `<style>`:

```css
:root {
  --blue:       #2c4a9e;   /* Color principal */
  --blue-light: #4a6fc4;
  --blue-pale:  #dde5f7;
  --accent:     #e8b84b;   /* Color de acento (dorado) */
  --sidebar-bg: #f4f6fb;   /* Fondo de la barra lateral */
}
```

### Fuentes
Se importan desde Google Fonts:
- **Raleway** — títulos, etiquetas y encabezados
- **Lora** — texto del cuerpo (serif elegante)

Para cambiarlas, modifica el `<link>` en el `<head>` y actualiza las variables `--font-display` y `--font-body`.

---

## ✅ Requisitos CSS implementados

| Requisito                        | Cómo se aplicó                                                    |
|----------------------------------|-------------------------------------------------------------------|
| Cambiar color del texto          | `.muted`, `.lang-pct`, `.tl-sub`, `.contact-item .icon`          |
| Cambiar tamaño de fuente         | `h1: 3rem`, `h2: 1.05rem`, `h3: .72rem`, `p: .83rem`            |
| Importar fuente de Google        | `Raleway` + `Lora` vía `<link rel="stylesheet">`                 |
| Bordes alrededor de elementos    | `.goal-card`, `.ref-card`, `.lang-bar`, `.sidebar`, `.header`    |
| Color de fondo en `div`          | `.sidebar { background-color: var(--sidebar-bg) }`, `.goal-card` |
| Herencia de estilos              | `body` define `font-family`, `color` y `font-size` para hijos    |
| Código hexadecimal para colores  | `#2c4a9e`, `#1a1a2e`, `#dde5f7`, `#e8b84b`, `#c8cedf`, etc.     |
| Variable CSS personalizada       | `:root` con `--blue`, `--font-display`, `--radius`, `--muted`…   |
| Modificar tamaño de imágenes     | `.header-photo img { width: 220px; height: 220px }`              |

---

## 📋 Secciones del CV

| Sección               | Descripción                                              |
|-----------------------|----------------------------------------------------------|
| **Header**            | Foto, nombre completo y título profesional               |
| **Contact**           | Teléfono, email, ubicación, edad, nacionalidad y redes   |
| **Languages**         | Español e inglés con barras de porcentaje                |
| **Skills**            | Etiquetas de habilidades técnicas (Python, JS, VHDL…)   |
| **Software**          | Herramientas con barras de dominio en porcentaje         |
| **Interests**         | Áreas de interés profesional                             |
| **Profile**           | Párrafo de presentación personal                         |
| **Education**         | Tres niveles: primaria/secundaria, CONALEP y UdeG        |
| **Work Experience**   | Dos experiencias laborales con fechas                    |
| **Projects**          | Tres proyectos académicos/personales                     |
| **Professional Goals**| Metas a corto, mediano y largo plazo                     |
| **References**        | Dos referencias personales con contacto                  |

---

## 🌐 Compatibilidad

| Navegador | Soporte |
|-----------|---------|
| Chrome 90+   | ✅ Completo |
| Firefox 88+  | ✅ Completo |
| Edge 90+     | ✅ Completo |
| Safari 14+   | ✅ Completo |
| IE 11        | ❌ No soportado (usa CSS Grid y variables CSS) |

---

## 📱 Responsivo

El layout se adapta automáticamente en pantallas menores a **700px**:
- Las dos columnas se convierten en una sola columna
- La foto ocupa todo el ancho del header
- Las tarjetas de metas y referencias se apilan verticalmente

---

## 👤 Autor

**Hugo Nicolas Pulido Moreno**  
Estudiante de Ingeniería en Computación — Universidad de Guadalajara (CUCEI)  
📧 Hugonicolas783@gmail.com · 📞 332-989-6683

---

## 📝 Licencia

Proyecto personal de uso libre. Puedes tomar la estructura y adaptarla para tu propio CV.
