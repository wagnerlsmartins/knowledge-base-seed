# Como contribuir

> **Está sozinho na sua KB?** Pode editar direto (pelo navegador, botão do lápis → Commit). O
> fluxo de Pull Request abaixo é para quando **mais de uma pessoa ou agente** colabora na
> mesma base — aí ele evita atropelo e dá revisão. Não precisa dele no seu primeiro material.

Em colaboração, toda mudança é feita por **Pull Request**. Nada de commit direto no `main`.

**Regra de ouro:** uma sessão = uma branch = uma PR, sempre saindo do `main` atualizado. Isso
evita branches empilhadas e conflitos. Se precisa só do fluxo de Git, veja o
[manual de Git](./docs/09-operacao/01_manual-git.md).

## Fluxo

1. `git switch main && git pull --ff-only`
2. criar **uma** branch (prefixo de autor/agente: `claude/*`, `codex/*`, `<nome>/*`)
3. editar ou criar Markdown
4. manter o frontmatter (ver schema abaixo)
5. atualizar os links `related` afetados
6. abrir PR com resumo claro — **sem merge próprio**
7. pedir revisão e incorporar feedback
8. merge apenas após aprovação de quem mantém

## Frontmatter

A convenção padrão é **OKF leve** — só `type` é obrigatório:

```yaml
---
type: ""
title: ""
description: ""
tags: []
timestamp: ""   # AAAA-MM-DD
related: []
---
```

Para KB institucional há o **schema rico** opcional (com `authority`, `audience`, `status`,
`owner`…). Os dois níveis estão em [docs/09-operacao/00_schema.md](./docs/09-operacao/00_schema.md).

## Agentes de IA

Se você é um agente, declare o modelo no commit (`Co-Authored-By:`) e no corpo da PR. Veja
[colaboração com modelos](./docs/09-operacao/03_colaboracao-com-modelos.md) e
[AGENTS.md](./AGENTS.md).
