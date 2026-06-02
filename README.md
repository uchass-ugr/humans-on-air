# Cómo publicar este sitio en GitHub Pages

## Estructura de archivos

```
mi-proyecto-web/
├── _config.yml          ← configuración global
├── _data/
│   └── navigation.yml   ← menú de navegación
├── assets/
│   └── images/          ← pon aquí tus imágenes
├── index.md             ← portada
├── sobre.md             ← sección "Sobre el proyecto"
├── noticias.md          ← sección "Noticias"
├── charlas.md           ← sección "Charlas"
├── talleres.md          ← sección "Talleres"
├── equipo.md            ← sección "Equipo"
└── Gemfile
```

---

## Pasos para publicar

### 1. Crear el repositorio en GitHub

1. Ve a https://github.com/new
2. Nombre del repositorio:
   - Si quieres que la URL sea `https://TU-USUARIO.github.io` → llámalo `TU-USUARIO.github.io`
   - Si quieres `https://TU-USUARIO.github.io/mi-proyecto` → llámalo `mi-proyecto`
3. Márcalo como **Public**
4. No añadas README ni .gitignore ahora (ya los tienes aquí)

### 2. Subir los archivos

Desde la terminal, en la carpeta de este proyecto:

```bash
git init
git add .
git commit -m "Primer commit: estructura base del sitio"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/NOMBRE-REPO.git
git push -u origin main
```

### 3. Activar GitHub Pages

1. Ve a tu repositorio → **Settings** → **Pages** (menú lateral izquierdo)
2. En "Source" selecciona **Deploy from a branch**
3. Rama: `main`, carpeta: `/ (root)`
4. Haz clic en **Save**

Al cabo de 1–2 minutos el sitio estará en:
`https://TU-USUARIO.github.io` (o `/NOMBRE-REPO` según el paso 1)

---

## Personalización básica

### Cambiar el nombre y descripción del sitio
Edita `_config.yml`:
```yaml
title: "Nombre real del proyecto"
description: "Tu descripción aquí"
url: "https://TU-USUARIO.github.io"
```

### Añadir una noticia
Abre `noticias.md` y añade una nueva entrada siguiendo el patrón:
```markdown
### Título de la noticia
*Fecha*

Texto de la noticia.
```

### Añadir imágenes
Pon las imágenes en `assets/images/` y referencialas así en Markdown:
```markdown
![Texto alternativo](/assets/images/mi-imagen.jpg)
```

### Cambiar el color de cabecera en la portada
En `index.md`, cambia el valor de `overlay_color`:
```yaml
overlay_color: "#1a1a2e"   # cualquier color hex
```

---

## Actualizar el sitio

Cada vez que hagas cambios, simplemente:
```bash
git add .
git commit -m "Descripción del cambio"
git push
```
GitHub reconstruye el sitio automáticamente en 1–2 minutos.
