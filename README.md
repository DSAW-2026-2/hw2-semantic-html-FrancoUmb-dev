## Sitio publicado

https://dsaw-2026-2.github.io/hw2-semantic-html-FrancoUmb-dev/

## Registro de uso de IA

**Prompt utilizado:** le pedí a Claude que convirtiera el contenido de
HW01 en HTML semántico puro (header, nav, main, section, article,
footer), sin CSS ni JavaScript, con jerarquía de encabezados correcta.

**Qué cambió:** el primer esqueleto usaba ids en español
(`id="problema"`, `id="solucion"`). Los corregí a inglés
(`id="problem"`, `id="solution"`, `id="target-users"`) para cumplir la
convención del curso: código en inglés, texto en español.

**Error real y cómo lo resolví:** clonamos por error el repositorio
plantilla de solo lectura, no el repositorio personal que crea GitHub
Classroom. El push falló con error 403. Lo resolví apuntando el
repositorio local al correcto con `git remote set-url origin <url>` y
luego `git push origin main --force`.

**Diferencia entre el syllabus general y el rubric.json real:** el
rubric.json de este repo específico pedía un formulario con `label
for=` conectado al `id` de cada input, y una imagen con `alt`
descriptivo — ninguno estaba en la descripción general de la tarea. Los
agregué después de comparar directamente contra ese archivo.

**Parte que no entendí de inmediato:** por qué GitHub Pages seguía
mostrando una versión vieja después de varios push exitosos. La causa
real (confirmada revisando Actions) era que un cambio de `index.html`
nunca se había llegado a confirmar con `git commit` — `git status`
mostraba "modified: index.html" pendiente todo ese tiempo.

# HW02 — Semantic HTML

**Week 2 · DSAW · Universidad de La Sabana**

## Objective

Build the HTML skeleton of your project's landing page using **semantic HTML only** — no CSS, no JavaScript.

## Deliverables

### `index.html`

Build your project's landing page with:

- Complete semantic HTML5 structure: `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>` — used meaningfully, not as div replacements
- A single `<h1>` per page. Use `<h2>` and `<h3>` for subsections.
- At least one `<form>` with:
  - `<input>` fields with appropriate types (`text`, `email`, `password`, etc.)
  - Every field has a `<label>` associated via matching `for` and `id` attributes
- All images have a descriptive `alt` attribute — not empty, not "image"
- **No styles. No scripts.** This deliverable evaluates structure only.

## Layer 2

Run your page through [WAVE Web Accessibility Evaluator](https://wave.webaim.org/). Fix at least 2 of the flagged errors or alerts. Include a screenshot of the result in an `assets/` folder.

## AI Log

If you used AI to generate the HTML, include at the end of the file or in an `AI-LOG.md`:
- Which parts were AI-generated
- What you had to fix and why

## Deployment

Push to GitHub Pages. Plain HTML — no build step required.

## Autograding

The pipeline will check:
- ✅ `index.html` exists and has content
- ✅ HTMLHint: zero HTML errors
- ✅ GitHub Pages responds with HTTP 200
- ✅ Correct use of semantic tags, forms, and accessibility attributes (reviewed by Claude)

> **Submission rule:** If it is not deployed and public, it cannot be graded.
