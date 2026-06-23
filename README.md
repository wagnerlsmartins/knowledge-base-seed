# Knowledge Base Seed

Template para iniciar uma **Knowledge Base (KB) versionada em Markdown** — conhecimento
estratégico, técnico, editorial ou operacional vivendo em arquivos simples, no Git, legível
por humanos **e** por agentes de IA. Sem depender de CMS, sem lock-in.

Esta semente nasceu de KBs reais em operação (uma empresa, um curso, um home-lab pessoal) e
condensa as convenções que sobreviveram ao uso. Clone, responda algumas perguntas, e você tem
uma KB funcionando com governança, navegação e prontidão para agentes desde o dia 1.

## O que é (e o que não é)

**É:** uma estrutura de pastas + convenções de frontmatter + rituais de contribuição para
acumular conhecimento de forma durável e portátil.

**Não é:** um wiki com banco de dados, um CMS, ou um lugar para dados brutos sensíveis
(segredos, dados pessoais, exports). Isso fica fora do Git.

## Por onde começar

**Com pressa / não é dev?** Vá direto para **[Sua primeira KB em 15 minutos](docs/00-comece-aqui/04_primeira-kb-em-15-min.md)** (tudo pelo navegador, sem terminal) e olhe o **[exemplo preenchido](exemplos/marca-pessoal/00_mapa.md)**.

**Quer entender tudo?** Leia a pasta **[docs/00-comece-aqui](docs/00-comece-aqui/)** nesta ordem:

1. **[Glossário rápido](docs/00-comece-aqui/00_glossario-rapido.md)** — os termos técnicos traduzidos.
2. **[As perguntas fundamentais](docs/00-comece-aqui/01_perguntas-fundamentais.md)** — 8 perguntas que definem a sua KB.
3. **[Ferramentas](docs/00-comece-aqui/02_ferramentas.md)** — o que usar (com e sem terminal).
4. **[Como instanciar](docs/00-comece-aqui/03_como-instanciar.md)** — passo a passo completo.

Se você é um **agente** (Claude, Codex, etc.), comece por **[AGENTS.md](AGENTS.md)**.

## Estrutura

```text
docs/
  00-comece-aqui/   perguntas, ferramentas e guia de instanciação (apague depois de ler)
  01-base/          fundação: mapa, tese, léxico, entidades
  02-conteudo/      o conhecimento do seu objeto (você cria as seções)
  09-operacao/      governança da própria base: schema, camadas, ingestão
exemplos/           uma KB de exemplo, preenchida, para imitar
views/              trilhas de leitura por público (≠ estrutura de pastas)
type/               tipos de nota como lente de navegação
projeto/            "SO de projeto": inbox → nota → decisão → backlog → log → handoff (opcional)
scripts/            utilitários (ex.: criar par de arquivos de ingestão de call)
AGENTS.md           instruções para agentes de IA
CONTRIBUTING.md     fluxo de contribuição (PR-only)
```

## Uso esperado

- documentação institucional, de produto ou de curso
- base pública, semi-pública ou privada
- fonte de contexto para agentes e MCP
- memória operacional versionada (calls, decisões, handoffs)
