---
type: guide
title: Ferramentas
description: O que instalar para operar uma KB versionada em Markdown, e por quê.
tags: [onboarding, ferramentas, setup]
timestamp: 2026-06-23
related:
  - 01_perguntas-fundamentais.md
  - 03_como-instanciar.md
---

# Ferramentas

Uma KB versionada em Markdown pede pouco. Esta é a lista do essencial ao opcional.

| Ferramenta | Para quê | Obrigatória? |
| --- | --- | --- |
| **Git** | versionar, ramificar, manter histórico | Sim |
| **Conta no GitHub** (ou GitLab) | hospedar, revisar por Pull Request, autoria | Sim |
| **Editor de texto/Markdown** | escrever (VS Code, Obsidian, qualquer um) | Sim |
| **YAML frontmatter** | metadados legíveis por humano e agente (é só convenção, nada a instalar) | Sim |
| **Editor com agente de IA** (Claude Code, Cursor) | escrever, navegar, ingerir e manter a base com ajuda | Recomendada |
| **`gh` CLI** | abrir PRs e gerenciar o repo pelo terminal | Recomendada |
| **MCP** (Model Context Protocol) | expor a KB para agentes consumirem como contexto | Opcional |
| **Gestor de tarefas** (Basecamp, Linear, etc.) | onde mora a **ação de equipe** — que NÃO é memória versionada | Conforme o objeto |
| **Skills `/checkin` e `/checkout`** | ritual de sessão: sincroniza `main`, cria 1 branch, abre 1 PR ao fechar | Opcional, recomendada |

## Princípios por trás da escolha

- **Markdown + Git, não plataforma.** O conhecimento precisa sobreviver à ferramenta. Texto
  simples em Git é portátil, diffável e legível por qualquer agente, hoje e em 10 anos.
- **Frontmatter pequeno.** Metadado em YAML no topo do arquivo (ver
  [schema](../09-operacao/00_schema.md)). O suficiente para busca, filtro e indexação — sem
  burocracia.
- **Separe memória de ação.** O que precisa de responsável e prazo vive no gestor de tarefas.
  O que é conhecimento durável vive aqui. Não confunda os dois.

## Dois caminhos: escolha o seu

Você **não precisa de terminal** para ter uma KB. Escolha pelo seu conforto.

### Caminho A — sem terminal (recomendado para começar)

Só uma conta no GitHub e um navegador.

1. abra esta semente no GitHub e clique em **"Use this template" → "Create a new repository"**;
2. edite os arquivos pelo próprio site (botão do **lápis** → **Commit changes**);
3. (opcional) instale o **GitHub Desktop** se quiser editar no seu computador sem comandos.

É por aqui que a [primeira KB em 15 minutos](04_primeira-kb-em-15-min.md) acontece.

### Caminho B — terminal (para quem já é fluente)

```bash
brew install git gh        # macOS, via Homebrew
gh auth login
gh repo create minha-kb --private --template wagnerlsmartins/knowledge-base-seed
```

---

Não entendeu algum termo desta página? Veja o
[glossário rápido](00_glossario-rapido.md). Depois siga para
**[sua primeira KB em 15 minutos](04_primeira-kb-em-15-min.md)** ou, se quiser planejar antes,
**[as perguntas fundamentais](01_perguntas-fundamentais.md)**.
