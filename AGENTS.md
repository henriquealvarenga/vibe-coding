# AGENTS.md

Arquivo de contexto persistente para agentes de IA (Claude Code, Codex,
Gemini CLI, etc.) trabalhando neste projeto. Os agentes leem este arquivo
automaticamente em toda conversa, **antes** do prompt do usuário. As regras
abaixo se aplicam sem precisar serem mencionadas em cada interação.

## Sobre este projeto

- **Tipo:** site Quarto de pesquisa científica.
- **Idioma:** português brasileiro (PT-BR).
- **Stack:** Quarto + R + Python + Git.
- **Bibliografia:** `references/references.bib` (BibTeX), com estilo CSL ABNT
  em `references/csl_styles/ABNT.csl`.

## Convenções de nomeação (consistência > preferência)

- **Arquivos `.qmd`** (viram URLs no site): *kebab-case* minúsculo, sem acentos,
  sem espaços. Exemplo: `analise-sobrevida.qmd`, NÃO `Analise_Sobrevida.qmd`.
- **Arquivos `.R`, `.py`, `.ipynb`** (código): *snake_case* minúsculo, sem
  acentos. Exemplo: `analise_sobrevida.R`. Hífen quebra import no Python.
- **Variáveis, funções e colunas de dataframe:** *snake_case* minúsculo
  (convenção do tidyverse e do PEP 8). Exemplo: `idade_anos`,
  `calcular_media`, `df$pressao_arterial`.
- **Constantes** (parâmetros que não mudam em runtime): `UPPER_SNAKE_CASE`.
  Exemplo: `ALPHA_NIVEL = 0.05`, `IDADE_MIN_INCLUSAO = 18`.
- **Nomes descrevem intenção, não implementação ou versão.** Bom:
  `analise_sobrevida_por_grupo.R`. Ruim: `script_v3_final.R`.
- **Nunca usar sufixos de versão** como `_v2`, `_final`, `_FINAL_DEFINITIVO`.
  Versionamento é responsabilidade do Git, não do nome do arquivo.
- **Filesystem case-insensitive (macOS/Windows):** localmente, `Claude.qmd` e
  `claude.qmd` parecem o mesmo arquivo, mas em servidor Linux (onde o site é
  publicado) são URLs diferentes. **Sempre use minúsculas desde o início**
  para evitar 404 silenciosos em produção.
- **Nunca misture convenções no mesmo projeto.** A escolha entre estilos
  importa menos do que aplicar a mesma regra em todos os arquivos do mesmo
  tipo.

## Configurações externalizadas

- Parâmetros do projeto (caminhos, limiares estatísticos, *seeds*, critérios
  de inclusão) ficam em `config.yml` ou em `_variables.yml` na raiz, **nunca
  espalhados como literais pelos scripts**.
- Lockfiles obrigatórios para reprodutibilidade: `renv.lock` (R) e/ou
  `pyproject.toml` + `uv.lock` (Python).

## Comentários no código

- Explicam o **por que** de uma decisão (escolha de teste estatístico,
  justificativa de transformação), não **o que** o código faz (que o próprio
  código já mostra).
- Não comente o óbvio (`# soma a + b`).

## Comportamento do agente

- **Plan-first.** Antes de criar mais de 3 arquivos novos, fazer refatoração
  ampla, ou qualquer mudança estrutural, **apresentar o plano completo e
  aguardar confirmação** explícita do usuário.
- **Pedir permissão** antes de **renomear, mover ou deletar** arquivos.
- **Não fabricar referências bibliográficas.** Projeto acadêmico exige
  verificação. Se uma referência não pode ser confirmada por fonte primária,
  marcar explicitamente como "não verificada" — nunca inventar.
- **Verificar antes de afirmar fatos** sobre versões, releases, capacidades
  de produtos, datas. Quando em dúvida, buscar fontes oficiais e citar.
- **Documentar uso de IA** conforme recomendações do ICMJE quando o agente
  contribui para artefatos de pesquisa (manuscritos, análises, scripts).
- **Comandos destrutivos** (`rm`, `git push --force`, `DROP TABLE`,
  `--allow-root`) sempre exigem confirmação explícita.

## Tom de redação dos textos

- Didático, conversacional, mas rigoroso.
- Usar callouts do Quarto: `note`, `tip`, `warning` conforme apropriado.
- Usar tabelas comparativas quando ajudarem clareza.
- Blocos de código com `filename` quando útil para o leitor.
- "O que vem a seguir" no fim de cada capítulo, ligando ao próximo.
- Cortar redundância. Não inflar texto.

## Exemplos e datasets

- Exemplos genéricos (`mtcars`, `iris`, datasets sintéticos) para sintaxe.
- Posicionamento de domínio (médico, biológico, etc.) no texto que descreve
  o exemplo, não no código em si.
- Não introduzir vocabulário fora do escopo: termos de game-engine, OOP
  estrito, ou jargão de outros domínios que não casa com pesquisa científica.

---

## Especificidades deste projeto

<!--
Esta seção contém regras específicas deste projeto que NÃO são genéricas.
Quem usa este AGENTS.md como template em outro projeto pode apagar ou
substituir o conteúdo desta seção pelas regras do próprio projeto.
-->

- **Estrutura de pastas:** `M{n}-{slug}/B{n}-{slug}/{nn}-{slug}.qmd`. Exemplo:
  `M1-fundamentos/B2-agentes/02-claude.qmd`.
- **Numeração de Bloco reseta dentro de cada Módulo.** Capítulos com prefixo
  *zero-padded* (`01-`, `02-`, ..., `12-`) para que a ordem alfabética bata
  com a ordem real.
- **Cross-references entre capítulos no texto:** sempre por número
  (`M1-B2-03`), nunca por caminho de arquivo.
- **Não renomear** pastas ou arquivos seguindo o padrão `M{n}-`, `B{n}-`,
  `{nn}-` sem aprovação explícita do usuário — a convenção é estável e mexer
  nela quebra sidebars e links cruzados.
- **Sidebars:** uma sidebar por Bloco no `_quarto.yml`, com link
  "Próximo bloco" no rodapé apontando para o primeiro capítulo do próximo
  Bloco em ordem linear do curso.
- **Navegação global:** navbar com logo (casinha SVG em `images/house-fill.svg`),
  itens "Prefácio", "Módulos", "Créditos", e busca à direita.
- **Identidade visual:** tema `slate`, paleta EDL com acento *teal* `#00d9c0`,
  fontes Inter e JetBrains Mono. Detalhes em `styles.css`.
- **Renderização:** apenas `.qmd` é renderizado. Arquivos `.md` (incluindo
  este `AGENTS.md`) e as pastas `planejamento/` e `OLD_FILES/` são excluídas
  via `render:` em `_quarto.yml`.
- **Ementa do curso completa:** `planejamento/ementa.md`. Antes de mudanças
  estruturais (novo capítulo, novo bloco, renomeação), consultar a ementa.
