---
type: guide
title: Como instanciar
description: Passo a passo para transformar esta semente na sua própria KB.
tags: [onboarding, setup, checklist]
timestamp: 2026-06-23
related:
  - 01_perguntas-fundamentais.md
  - 02_ferramentas.md
---

# Como instanciar

"Clonei a semente, e agora?" Siga estes passos. No fim você tem uma KB sua, sem rastro de
template.

> **Quer um atalho?** Se é seu primeiro material, faça antes a
> [primeira KB em 15 minutos](04_primeira-kb-em-15-min.md) — ela cobre os passos 1 a 4 sem
> terminal. Volte aqui quando quiser o processo completo.

## Passo a passo

1. **Crie o repo a partir do template.**
   No GitHub, use "Use this template", ou:
   ```bash
   gh repo create minha-kb --private --template wagnerlsmartins/knowledge-base-seed
   git clone https://github.com/<voce>/minha-kb && cd minha-kb
   ```

2. **Responda as oito perguntas.**
   Abra [as perguntas fundamentais](01_perguntas-fundamentais.md) e responda cada uma. Esse é
   o trabalho mais importante — o resto é mecânico.

3. **Escreva o mapa e a tese.**
   Preencha [`docs/01-base/00_mapa.md`](../01-base/00_mapa.md) (cole ali as respostas das 8
   perguntas) e [`01_tese.md`](../01-base/01_tese.md). Comece pequeno.

4. **Crie as seções do seu conteúdo.**
   Em [`docs/02-conteudo/`](../02-conteudo/) crie as pastas que fazem sentido para o **seu
   objeto** (ex.: `produtos/`, `aulas/`, `clientes/`, `infra/`). Veja o
   [mapa de conteúdo](../02-conteudo/00_mapa.md).

5. **Escolha o nível de frontmatter.**
   Decida em [`docs/09-operacao/00_schema.md`](../09-operacao/00_schema.md): comece **leve**.

6. **Ative ou apague o que é opcional.**
   - Vai ingerir calls/transcrições? Mantenha [`projeto/`](../../projeto/). Senão, apague.
   - Trabalha com agentes? Ajuste o [`AGENTS.md`](../../AGENTS.md). Senão, simplifique.
   - Mais de uma camada? Configure a [separação de camadas](../09-operacao/02_separacao-de-camadas.md).

7. **Monte suas views.**
   Em [`views/`](../../views/) crie uma trilha de leitura por público (ver
   [exemplo](../../views/00_comece-por-aqui.md)).

8. **Apague esta pasta.**
   Quando terminar o onboarding, **delete `docs/00-comece-aqui/`** — ela é andaime do
   template, não conteúdo da sua KB. Atualize o `README.md` para falar da *sua* base.

## Checklist final

- [ ] 8 perguntas respondidas e coladas no mapa
- [ ] `docs/01-base/` preenchido (mapa, tese, léxico, entidades)
- [ ] `docs/02-conteudo/` com as seções do meu objeto
- [ ] nível de frontmatter escolhido no schema
- [ ] `projeto/` ativado ou apagado
- [ ] `AGENTS.md` ajustado ou simplificado
- [ ] `views/` com pelo menos uma trilha
- [ ] `docs/00-comece-aqui/` apagada
- [ ] `README.md` reescrito para a minha KB
