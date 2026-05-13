# Ementa — Vibe Coding na Pesquisa Científica

**Última atualização:** 2026-05-05 (reestruturação para 6 módulos com novo M1 dedicado a IA/Prompts; B4-Limites consolidado em 3 capítulos)
**Status:** estrutura aprovada, redação em andamento

## Identidade do curso

- **Título:** Vibe Coding na Pesquisa Científica
- **Público-alvo:** professores universitários, sem pré-requisito de conhecimento técnico em programação.
- **Objetivo central:** capacitar docentes a usarem agentes de IA para realizar análise de dados em R e Python, e a publicarem seus materiais e pesquisas de forma reprodutível na web.
- **Formato de entrega:** site público em Quarto (provavelmente via GitHub Pages), com cada capítulo como arquivo `.qmd` independente.
- **Estrutura:** linear, sem trilhas opcionais. **6 Módulos** organizados em **14 sub-seções** (Blocos) que contêm **91 capítulos** (após fusão dos antigos 02+03 do B4-Limites e adição da variante 02b em M1-B3). Pensado para curso de um semestre.

## Estrutura

O curso é organizado em 6 Módulos. Cada Módulo é dividido em sub-seções temáticas, e cada sub-seção contém entre 4 e 12 capítulos. "Módulo" é o termo principal usado no site (página inicial, sidebar).

| Módulo | Título | Sub-seções | Capítulos |
|---|---|---|---|
| 0 | Setup | Instalações · Apêndice | 7 |
| 1 | Trabalhando com IA na pesquisa | Conceitos · Agentes · Padrões de prompts · Limites | 23 (19 prontos + 4 a escrever) |
| 2 | Fundamentos técnicos | Terminal · Ambientes de trabalho · Convenções técnicas | 25 |
| 3 | Análise de dados e escrita técnica | Markdown, Quarto e Escrita Técnica · Dados · Python e R | 18 |
| 4 | Publicação e reprodutibilidade | Git, GitHub e GitHub Pages · Reprodutibilidade | 12 |
| 5 | Capstone | Aplicação na docência | 6 |

### Módulo 0 — Setup

Módulo de instalação. A sub-seção principal *Instalações* tem uma página por ferramenta, pensada para ser consultada como menu, não como trilha sequencial. A sub-seção *Apêndice* concentra pré-requisitos transversais (ferramentas que são necessárias para outras instalações funcionarem). Os capítulos não explicam o que cada ferramenta é nem o que ela faz; isso fica nos módulos posteriores.

#### Instalações (6 capítulos)

Pasta: `M0-setup/B1-instalacoes/`

- 01 R e Python
- 02 Instalando Positron, RStudio e VS Code
- 03 Instalando o Quarto
- 04 Instalando o Zotero
- 05 Instalando Claude, Codex e Gemini CLI
- 06 Instalando o Git

#### Apêndice (1 capítulo)

Pasta: `M0-setup/B2-apendice/`

- 01 Node.js e npm

### Módulo 1 — Trabalhando com IA na pesquisa

Módulo dedicado à **forma de trabalho** central do curso: como dialogar com IA, quais agentes usar, quais padrões de prompt funcionam em cada tipo de tarefa, e onde estão os limites da abordagem. Vem **logo depois do Setup** porque é a lente por onde o aluno vai enxergar todo o resto do curso.

#### Conceitos Fundamentais (6 capítulos)

Pasta: `M1-ia-pesquisa/B1-conceitos/`

- 01 O que é IA generativa
- 02 Tokens
- 03 API × app
- 04 Prompts
- 05 Documentar uso de IA
- 06 LGPD e dados sensíveis em prompts

#### Agentes de IA (5 capítulos)

Pasta: `M1-ia-pesquisa/B2-agentes/`

- 01 De chatbot a agente: o que mudou e por que importa
- 02 Claude (Cowork, Claude Code, etc.)
- 03 Codex
- 04 Gemini (com seção sobre Antigravity)
- 05 O arquivo `AGENTS.md` (contexto persistente; padrão da Agentic AI Foundation)

#### Padrões de prompts (9 capítulos — 5 prontos + 4 a escrever)

Pasta: `M1-ia-pesquisa/B3-prompts/`

- 01 Anatomia de um bom prompt
- 02 Prompt para estrutura inicial de projeto
- 02b Prompt para estrutura de artigo (variante: BJPsych)
- 03 Prompt para AGENTS.md customizado
- 04 Prompt para limpeza e transformação de dados
- 05 Prompt para análise estatística
- 06 Prompt para visualização e tabelas
- 07 Prompt para escrita acadêmica
- 08 Prompt para Git, debugging e code review

> Convenção de sufixo-letra: `02b`, `02c`... reservado para variantes especializadas do capítulo principal de mesmo número (aqui, prompts de estrutura calibrados para periódicos específicos). Se o conjunto de variantes crescer além de 3-4, refatorar para sub-pasta.

#### Limites e armadilhas (3 capítulos — ESCRITOS 2026-05-05)

Pasta: `M1-ia-pesquisa/B4-limites/`

- 01 Quando a IA falha (alucinação, viés, limites de contexto)
- 02 Validação e responsabilidade humana (consolida operacional + metodológico)
- 03 Considerações éticas e regulatórias (LGPD revisitado, ICMJE, declaração de uso, equidade)

> Nota (2026-05-05): plano original tinha 4 capítulos. Os antigos "Validação obrigatória" e "Decisão metodológica continua humana" foram fundidos em 02 — defendiam o mesmo princípio (humano continua responsável) sob ângulos diferentes; separar produzia repetição.

### Módulo 2 — Fundamentos técnicos

Módulo de **infraestrutura técnica** comum a todo o trabalho que vem depois. Terminal, IDEs, e convenções técnicas (nomeação, encoding, YAML, etc.). Conteúdo migrado do antigo M1, com o foco semântico-de-IA agora isolado no novo M1.

#### Terminal (9 capítulos)

Pasta: `M2-fundamentos-tecnicos/B1-terminal/`

- 01 História e conceitos básicos
- 02 Shells: bash, zsh, cmd, PowerShell
- 03 Abrindo o Terminal
- 04 Anatomia de um comando
- 05 Navegação no sistema de arquivos
- 06 Caminhos absolutos e relativos
- 07 Manipulação de arquivos e pastas
- 08 Visualização, busca e informações do sistema
- 09 Atalhos, prática e o que vem depois

#### Ambientes de trabalho (4 capítulos)

Pasta: `M2-fundamentos-tecnicos/B2-ambientes/`

- 01 Introdução: o que é uma IDE
- 02 Positron
- 03 RStudio
- 04 VS Code

#### Convenções técnicas (12 capítulos)

Pasta: `M2-fundamentos-tecnicos/B3-convencoes/`

- 01 Introdução ao Bloco
- 02 Convenções de nomeação e extensões de arquivo
- 03 Comentários
- 04 Símbolos e operadores
- 05 Indentação: o "símbolo invisível"
- 06 Arquivos invisíveis e como vê-los
- 07 YAML em todo lugar
- 08 Versão semântica, dependências e lockfiles
- 09 Estrutura clássica de projeto técnico
- 10 Encoding e caracteres especiais (UTF-8)
- 11 Lendo mensagens de erro (stack trace)
- 12 Interfaces: CLI, GUI, TUI

### Módulo 3 — Análise de dados e escrita técnica

#### Markdown, Quarto e Escrita Técnica (4 capítulos)

Pasta: `M3-analise/B1-markdown/`

- 01 Markdown
- 02 Quarto (chunks, multi-formato, YAML)
- 03 Citação: BibTeX e CSL
- 04 LaTeX

#### Dados (8 capítulos)

Pasta: `M3-analise/B2-dados/`

- 01 Por que existem tantos formatos
- 02 CSV e TSV
- 03 Excel (XLSX/XLS)
- 04 JSON
- 05 Parquet (formatos colunares)
- 06 SQLite e bancos relacionais
- 07 *Tidy data*
- 08 Convenção de organização: raw, processed, output

#### Python e R (6 capítulos)

Pasta: `M3-analise/B3-linguagens/`

- 01 Por que Python *e* R, não Python *ou* R
- 02 R: a linguagem para análise estatística
- 03 Python: linguagem de propósito geral aplicada a dados
- 04 Instalação de ambientes (renv, uv, virtualenv)
- 13 Documentação reprodutível (Quarto + engines knitr/jupyter)
- 14 Padrões de prompt para gerar código de análise

> **Decisão estrutural (2026-05-04):** os capítulos 05–12 originais (sintaxe mínima, estruturas de dados, importação, limpeza, descritiva, visualização, inferencial, modelagem) foram **deletados**. Razão: o curso vende a tese "vibe coding" — você descreve em PT-BR, a IA escreve o código. Reensinar essas operações em capítulos próprios contraria o argumento central. Para tratamento aprofundado de R, o leitor é direcionado ao livro do autor em [henriquealvarenga.com/manual_r](https://henriquealvarenga.com/manual_r/) (apontado a partir do cap. 02). Para Python, recursos curados aparecem no cap. 03. O cap. 14 substitui essa cobertura ao ensinar **como usar IA para gerar código de análise** — o que a abordagem "vibe coding" promete em vez de aprender sintaxe a fundo.

### Módulo 4 — Publicação e reprodutibilidade

#### Git, GitHub e GitHub Pages (6 capítulos)

Pasta: `M4-publicacao/B1-git/`

- 01 Versionamento: por que importa
- 02 Conceitos de Git (commit, branch, merge)
- 03 GitHub: hospedagem, colaboração, *issues*
- 04 Git assistido por IA
- 05 GitHub Pages: publicação estática
- 06 Quarto + GitHub Pages

#### Reprodutibilidade (6 capítulos)

Pasta: `M4-publicacao/B2-reprodutibilidade/`

- 01 Princípios FAIR
- 02 Ambientes reprodutíveis: renv, venv, uv
- 03 Quarto como artefato reprodutível
- 04 Zenodo (com OSF e Figshare em parágrafos curtos)
- 05 DOIs para dados e código
- 06 Estudo de caso integrador: do dado bruto ao site publicado

### Módulo 5 — Capstone

#### Aplicação na docência (6 capítulos)

Pasta: `M5-capstone/B1-aplicacao/`

- 01 Apresentação do projeto integrador
- 02 Escolha do tema e do *dataset*
- 03 Planejamento (escopo e divisão em etapas)
- 04 Execução com IA e pontos de validação
- 05 Publicação e divulgação
- 06 Retrospectiva crítica

## Registro de decisões

Decisões tomadas durante a fase de planejamento (abril/2026), com a justificativa para cada uma — para evitar revisitar o mesmo debate em conversas futuras.

### Reestruturação para 6 módulos com M1 dedicado a IA (05/05/2026)

Decisão maior. O M1 antigo (*Fundamentos*) misturava dois universos conceitualmente diferentes: (a) **diálogo com IA** (Conceitos sobre IA + Agentes) e (b) **infraestrutura técnica** (Terminal + Ambientes + Convenções). A separação em dois módulos distintos resolve essa tensão e torna a tese central do curso (vibe coding) **visível desde cedo**.

A reestruturação:

- **M1 antigo (Fundamentos)** dividido em dois novos módulos.
- **M1 novo (Trabalhando com IA na pesquisa)** absorve B1-Conceitos e B2-Agentes do M1 antigo, e adiciona B3-Padrões de prompts (8 caps novos) e B4-Limites e armadilhas (3 caps novos — após fusão dos planejados 02+03 em um único capítulo, 2026-05-05).
- **M2 novo (Fundamentos técnicos)** absorve B3-Terminal, B4-Ambientes e B5-Convenções do M1 antigo, agora renumerados como B1, B2, B3.
- **M2 antigo (Análise)** vira **M3**.
- **M3 antigo (Publicação)** vira **M4**.
- **M4 antigo (Capstone)** vira **M5**.

*Implicações operacionais:* renomeação de pastas (M1-fundamentos → M1-ia-pesquisa; criação de M2-fundamentos-tecnicos com migração interna; M2-analise → M3-analise; M3-publicacao → M4-publicacao; M4-capstone → M5-capstone). Atualização do `_quarto.yml` (sidebars), de cross-references nos 79 capítulos existentes, e da memória do projeto. Total de capítulos sobe de 79 para 91 (12 novos a escrever em M1-B3 e M1-B4).

*Razão didática:* a tese do curso é "você descreve, a IA escreve". Se essa tese é central, ela merece módulo próprio com **destaque editorial máximo** — primeiro módulo de conteúdo após o Setup. Aluno termina M0 (instalou tudo), abre M1 (entende como trabalhar com IA), e usa essa lente para ler todo o resto do curso.

### Foco em agentes, não em chatbots

A virada qualitativa de 2025–2026 foi o salto de chatbot para agente de IA — sistemas que executam código, criam arquivos e atuam diretamente no computador do usuário. A sub-seção *Agentes de IA* reflete essa premissa: o "diferencial" da IA hoje, para o docente, é o agente, não o chatbot conversacional.

### Python e R num único bloco

A escolha foi não obrigar o aluno a optar entre as duas linguagens. A sub-seção *Python e R* trata cada tópico (importação, transformação, visualização, etc.) de forma comparativa entre as duas — coerente com a realidade de quem usa IA, que com frequência alterna entre ambas.

### Sem trilhas opcionais

Curso com tronco linear único, sem ramificações por área de conhecimento. *Decisão revertida em parte:* o título passou a ser "Pesquisa Médica" para focar em pesquisadores médicos como público principal — implica que exemplos e datasets devem tender pra esse domínio à medida que os capítulos forem escritos.

> *Atualização (2026-05-05):* o título do curso foi modificado para "Vibe Coding na Pesquisa Científica". O público-alvo continua sendo pesquisadores médicos — apenas o título foi ampliado. A prosa de capítulos que descreve "pesquisa médica" como domínio dos exemplos foi mantida intencionalmente.

### LaTeX como capítulo separado, dentro de Markdown e Escrita Técnica

Inserido na sub-seção *Markdown, Quarto e Escrita Técnica* como capítulo isolado para quem precisa (teses, artigos com fórmulas pesadas, submissões a revistas que exigem `.tex`), sem inflar o curso para quem não precisa.

### Capítulos granulares (um tópico por arquivo)

Cada tópico conceitualmente distinto vai em seu próprio `.qmd`. Razão: o leitor de um site público chega via busca, em um capítulo específico — capítulos amplos prejudicam navegação e *deep linking*.

### Site público em Quarto

O projeto será publicado como site real, provavelmente via GitHub Pages. Implicações: cada `.qmd` precisa ser auto-suficiente para o leitor que cai ali sem ter lido o anterior; referências precisam ser impecáveis (não há autor à mão para esclarecer dúvida); navegação e índice ganham peso.

### Estrutura de pastas espelha a hierarquia

Capítulos vivem em `M{n}-modulo/B{n}-bloco/{nn}-titulo.qmd`. A numeração de Bloco reseta dentro de cada Módulo (M1 tem B1-conceitos, B2-agentes, B3-prompts, B4-limites; M2 começa de novo com B1-terminal). Razão: adicionar/remover/reordenar Blocos dentro de um Módulo só renumera dentro daquele Módulo, em vez de cascatear pelo curso inteiro. Filenames de capítulos usam padding `01-`, `02-`, ..., `12-` para ordem alfabética coincidir com ordem real.

### Bloco *Apêndice* (M0-B2) e capítulo Node.js/npm (01/05/2026)

Adicionado um segundo Bloco ao Módulo 0 chamado *Apêndice*, com um único capítulo: *Node.js e npm*. Razão: três das ferramentas instaladas em M0-B1 (Claude Code, Codex, Gemini CLI) dependem de Node.js como pré-requisito. Em vez de repetir a instrução de instalação dentro de cada capítulo de agente, foi criado um capítulo único de pré-requisito transversal, referenciado pelos capítulos que precisam. Mantém-se o princípio de "uma instalação, um lugar" e evita duplicação.

## Próximos passos

1. **Próximo trabalho de redação (continuação a partir de 2026-05-05):** finalizar os **4 capítulos restantes** do **B3 Padrões de prompts** (capítulos 05-08; capítulos 01-04 e a variante 02b — BJPsych — já escritos). O **B4 Limites e armadilhas** está **completo** com 3 capítulos (escritos 2026-05-05; plano original de 4 capítulos foi consolidado para 3). Padrão de redação consolidado: sem hard-wrap, tom didático-conversacional, callouts apenas onde agregam, citações peer-reviewed em `[@chave]`, "O que vem a seguir" no fim, abertura concreta com cena, pegada histórica onde couber.

2. Após escrita dos 12 capítulos novos, **revisão humana ampla** do curso completo. O prefácio adverte que material ainda não foi todo revisado.

3. Apagar `OLD_FILES/` quando estiver confortável de que não há mais nada útil a aproveitar dele.

4. Limpeza pendente do `references.bib`: duas chaves duplicadas (`wickham2023r4ds` e `wilson2017good` aparecem cada uma em duas entradas com pequenas variações). BibTeX silenciosamente usa a última e emite warning. Não é urgente, mas vale resolver antes da base crescer mais.

5. Construir `references/references.bib` em paralelo com a redação, **sempre verificando referências reais** — projeto acadêmico exige verificação rigorosa, sem invenções (regra absoluta, vale também para exemplos dentro de blocos de código).

6. Decidir se exemplos e datasets dos Módulos 3–5 vão tender pra área médica (coerente com o título) ou se ficam genéricos. *Decisão atual (28/04/2026):* exemplos genéricos (mtcars, iris) com posicionamento médico apenas no texto descritivo. Não revisitar.
