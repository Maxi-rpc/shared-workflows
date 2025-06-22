# 🤖 Codium PR Agent

📄 Archivo: `.github/workflows/codium-pr-agent.yml`

---

## ¿Qué es?

El workflow `Codium PR Agent` ejecuta [Codium-ai/pr-agent](https://github.com/Codium-ai/pr-agent), un agente de revisión automática de Pull Requests impulsado por OpenAI.

### Funcionalidades:
- Revisión automática del PR (`auto_review`)
- Descripción automática del PR (`auto_describe`)
- Mejora sugerida del código (`auto_improve`)
- Soporte para comentarios e interacciones en el PR

---

## Cómo usarlo

```yaml
# .github/workflows/codium-pr.yml
name: Codium PR Agent

on:
  pull_request:
    types: [opened, reopened, ready_for_review, review_requested]
  issue_comment:

permissions:
  contents: write
  pull-requests: write
  issues: write
  
jobs:
  codium-agent:
    uses: your-account/shared-workflows/.github/workflows/codium-pr-agent.yml@main
    secrets: inherit

