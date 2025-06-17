# 🔐 CodeQL Analysis Workflow

📄 Archivo: `.github/workflows/codeql.yml`

---

## ¿Qué es CodeQL?

**CodeQL** es una herramienta de análisis estático de seguridad desarrollada por GitHub que permite escanear el código fuente para detectar vulnerabilidades, errores lógicos y malas prácticas de seguridad.

---

## Características del workflow

- Análisis automático con CodeQL
- Soporte para múltiples lenguajes (JavaScript, Python, Java, C#, entre otros)
- Reutilizable y fácil de integrar en cualquier repositorio
- No requiere configuración de secrets adicionales

---

## Cómo usarlo

```yaml
# .github/workflows/codeql.yml
name: CodeQL via Shared Workflow

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  run-codeql:
    uses: your-account/shared-workflows/.github/workflows/codeql.yml@main
    with:
      languages: 'javascript' # add multulanguages javascript,python
