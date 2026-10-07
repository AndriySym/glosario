# 🛡️ Glosario Colaborativo de Ciberseguridad

Repositorio colaborativo para crear, organizar y mantener una enciclopedia técnica de ciberseguridad mediante contribuciones del alumnado con **Pull Requests**.

---

## 📂 Estructura del Repositorio

Para facilitar la contribución, los alumnos únicamente interactúan con la carpeta de términos y la plantilla:

```text
glosario/
├── terminos/                       # 📁 Carpeta con todos los términos del glosario (*.md)
│   ├── cifrado.md
│   ├── cve.md
│   ├── firewall.md
│   ├── zero-trust.md
│   └── ...
├── plantilla.md                    # 📄 Plantilla oficial para redactar un nuevo término
└── README.md                       # 📖 Esta guía rápida de contribución
```

*(La infraestructura web de MkDocs se encuentra empaquetada de forma transparente dentro de `.mkdocs/`).*

---

## 🚀 Cómo Contribuir con un Nuevo Término (Paso a Paso)

### 1. Haz un Fork del Repositorio
Pulsa el botón **Fork** (arriba a la derecha en GitHub) para copiar el repositorio a tu cuenta personal.

### 2. Clona tu Fork y Crea una Rama
Abre tu terminal y ejecuta:

```bash
git clone https://github.com/TU-USUARIO/glosario.git
cd glosario
git checkout -b feat/nombre-del-termino
```

> 💡 *Usa nombres en minúsculas separados por guiones para la rama, por ejemplo: `feat/cross-site-scripting` o `feat/ransomware`.*

### 3. Redacta tu Término Usando la Plantilla
1. Copia la plantilla a la carpeta `terminos/` con el nombre de tu concepto en formato **kebab-case**:
   ```bash
   cp plantilla.md terminos/nombre-del-termino.md
   ```
2. Abre `terminos/nombre-del-termino.md` en tu editor de código (VS Code, etc.).
3. Rellena el bloque inicial de **metadatos YAML (Frontmatter)**:
   ```yaml
   ---
   title: "Nombre del Término"
   category: "Vulnerabilidades Web"
   author: "@tu-usuario-github"
   tags:
     - ciberseguridad
     - web
   summary: "Resumen conciso del término en 1 o 2 líneas explicativas."
   ---
   ```
4. Desarrolla las secciones del término: **Definición**, **¿Cómo funciona?**, **Ejemplo práctico (seguro vs inseguro)**, **Medidas de mitigación** y **Referencias**.

---

### 4. Enviar tu Contribución (Pull Request)

1. Guarda los cambios y haz commit:
   ```bash
   git add terminos/nombre-del-termino.md
   git commit -m "feat(terminos): añadir término <nombre-del-termino>"
   ```
2. Sube la rama a tu fork en GitHub:
   ```bash
   git push origin feat/nombre-del-termino
   ```
3. Dirígete a GitHub y haz clic en **"Compare & pull request"**.
4. Completa la plantilla de PR verificando que cumples los puntos del checklist.
5. El flujo automatizado de GitHub Actions validará automáticamente el formato de tu término.
6. Tras la revisión y aprobación, el término se integrará y aparecerá publicado en la web oficial del glosario.

---

## 🐳 (Opcional) Probar la Web en Local con Docker

Si deseas previsualizar cómo se renderiza la web completa en tu navegador:

```bash
docker compose -f .mkdocs/compose.yaml up
```

Abre en tu navegador: **[http://localhost:8000](http://localhost:8000)**
Cualquier cambio que hagas en `terminos/` se actualizará automáticamente en vivo.