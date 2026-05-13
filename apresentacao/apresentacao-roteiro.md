# Roteiro da Apresentação — Vibe Coding na Pesquisa Científica

**Contexto:** aula para alunos de graduação e residência médica
**Duração:** 40 minutos (com margem para perguntas)
**Estilo:** poucas palavras nos slides, narrativa toda na fala
**Status:** rascunho — aguardando aprovação para gerar no Gamma

## Estrutura geral

| # | Bloco | Slides | Tempo |
|---|---|---|---|
| 1 | Abertura | 1 | 1 min |
| 2 | Gancho e dor (workflow tradicional) | 2–7 | 12 min |
| 3 | A virada (Quarto: um documento) | 8–10 | 6 min |
| 4 | Demo do Positron e Quarto renderizando | 11–13 | 7,5 min |
| 5 | Demo do Cowork escrevendo o `.qmd` | 14–16 | 7,5 min |
| 6 | Fechamento e curso | 17–18 | 5 min |
| | **Total** | **18** | **~39 min** |

Convenção: cada bloco de slide especifica **texto na tela** (o que o aluno vê — sempre poucas palavras), **visual** (imagem/diagrama/screenshot — `[PLACEHOLDER]` indica que você inserirá depois) e **fala** (o que dizer ao apresentar).

---

## Slide 1 — Capa

**Texto na tela:**
> Vibe Coding na Pesquisa Científica
> Análise de dados reprodutível com IA
> Henrique Alvarenga da Silva

**Visual:** fundo escuro (paleta EDL — preto azulado, acento *teal*), sem ilustração elaborada; só o título centralizado com o nome embaixo.

**Fala (~1 min):**
Apresentação pessoal curta. "Hoje a gente vai falar de uma forma diferente de fazer análise de dados — uma forma que praticamente não existia há dois anos e que mudou como eu trabalho. Não vou ensinar a programar nesta aula. Vou mostrar uma ideia."

---

## Slide 2 — O que é Vibe Coding

**Texto na tela:**
> Vibe Coding
> Você descreve. A IA escreve o código.

**Visual:** ícone simples — uma seta de "humano" para "código", com rótulo "linguagem natural".

**Fala (~2 min):**
O termo "vibe coding" foi popularizado em 2025. A ideia é que o pesquisador descreve em português o que quer fazer (importar uma planilha, calcular médias, comparar grupos, fazer um gráfico) e um agente de IA escreve o código. Você não precisa decorar sintaxe. Você precisa saber *o que quer*. Isso muda o pré-requisito da análise: deixa de ser "saber programar" e passa a ser "saber descrever sua pesquisa".

---

## Slide 3 — Cena familiar

**Texto na tela:**
> Sua pesquisa.
> 200 pacientes.
> 30 variáveis.

**Visual:** uma planilha estilizada (tabela com colunas), imagem genérica.

**Fala (~1,5 min):**
Vamos imaginar uma pesquisa qualquer — não importa a área. Você tem um banco de dados clínico, vai fazer uma análise, escrever um artigo. Vou descrever um fluxo que provavelmente todo mundo aqui já viveu.

---

## Slide 4 — Fluxo tradicional

**Texto na tela:**
> SPSS → Word

**Visual:** diagrama horizontal com três caixas: **SPSS** (logo ou ícone) → seta com texto "copia tabela / cola figura" → **Word** (logo ou ícone). Setas grossas.

**Fala (~2 min):**
A maneira clássica: você roda a análise no SPSS (ou Stata, ou JASP, ou Excel). Pega a tabela de saída, copia. Cola no Word. Salva o gráfico como imagem. Insere no Word. Reformata para caber. Repete. Ao fim do dia, você tem um documento. Funciona — mas tem um problema invisível.

---

## Slide 5 — O orientador pede

**Texto na tela:**
> "Refaz tirando os menores de 18."

**Visual:** balão de fala. Fundo neutro.

**Fala (~2 min):**
Aí o orientador, ou o revisor, ou você mesmo um mês depois pede uma mudança simples: tira os menores de 18, ou troca um teste estatístico, ou inclui um novo desfecho. Em código, isso é uma linha mudada. No fluxo tradicional…

---

## Slide 6 — Refazer tudo. Manualmente.

**Texto na tela:**
> Refazer tudo.
> Manualmente.

**Visual:** ilustração de várias setas circulares — análise → tabela → Word, repetido com símbolos de "refresh". Pode ser um GIF ou imagem estilizada.

**Fala (~2 min):**
Você roda a análise de novo. Apaga as tabelas antigas do Word. Cola as novas. Apaga as figuras. Cola as novas. Reformata tudo. E reza para não ter esquecido nenhuma. É hora perdida — e é onde os erros entram.

---

## Slide 7 — Onde os erros se escondem

**Texto na tela:**
> Tabela 3 ainda tem o número antigo.

**Visual:** uma tabela com uma célula destacada em vermelho.

**Fala (~1,5 min):**
A Tabela 3 ficou com o n da análise anterior. O p-valor do gráfico não bate com o do texto. A figura é da versão antiga porque você esqueceu de re-exportar. Esse tipo de inconsistência é mais comum do que se admite, e é uma das fontes silenciosas de erros em artigos médicos. Não é falta de cuidado. É um *workflow* frágil.

---

## Slide 8 — E se…

**Texto na tela:**
> E se a análise *fosse* o documento?

**Visual:** um único caractere de pergunta, ou uma transição visual minimalista.

**Fala (~1,5 min):**
Aqui vem a virada. E se o texto que você escreve, o código da análise e os resultados (tabelas, gráficos) vivessem no mesmo arquivo? E se mudar o código atualizasse automaticamente todas as tabelas e figuras do artigo, sem você tocar em nada?

---

## Slide 9 — Quarto

**Texto na tela:**
> Quarto
> Texto + código + saída

**Visual:** logo do Quarto (azul) ao lado de três blocos sobrepostos rotulados "texto", "código", "saída".

**Fala (~2 min):**
Esse é o Quarto. Um formato de documento desenvolvido pela Posit — a mesma empresa do RStudio. O arquivo `.qmd` mistura três coisas: o texto que você escreve em Markdown, blocos de código em R ou Python, e a saída do código (tabelas, gráficos, números). Quando você renderiza, o Quarto executa o código e *insere* o resultado no lugar certo do documento. Tudo ao vivo.

---

## Slide 10 — Anatomia de um `.qmd`

**Texto na tela:** (sem texto explicativo — só o código)

```
---
title: "Estudo de coorte"
---

## Resultados

A média de idade foi de:

```{r}
mean(dados$idade)
```
```

**Visual:** o bloco acima estilizado como código com sintaxe colorida. Setas pequenas apontando: "YAML / metadados", "texto", "código que executa".

**Fala (~2 min):**
A anatomia é simples. Em cima, um bloco de metadados — título, autor. No meio, texto comum (Markdown — você aprende em quinze minutos). E os blocos de código entre crases triplas. Quando o documento é renderizado, o `mean(dados$idade)` é substituído pelo número real. Se os dados mudam, o número muda. Sozinho.

---

## Slide 11 — Demo: Positron

**Texto na tela:**
> Positron

**Visual:** [PLACEHOLDER — screenshot do Positron com um `.qmd` aberto à esquerda e o preview renderizado à direita, mostrando código + saída ao vivo].

**Fala (~2,5 min):**
Aqui está o Positron — o IDE da Posit, sucessor do RStudio. Ele abre o `.qmd` à esquerda e o preview renderizado à direita. Eu mudo um valor no código, salvo, o preview atualiza. Sem copiar, sem colar. *(Mostrar 2-3 mudanças ao vivo se possível, ou narrar o screenshot.)*

---

## Slide 12 — Mude o código → tudo se atualiza

**Texto na tela:**
> Uma mudança. Tudo refeito.

**Visual:** [PLACEHOLDER — duas screenshots lado a lado: antes e depois de mudar um filtro no código, mostrando que tabelas e gráficos do documento mudaram juntos].

**Fala (~2 min):**
Volta ao orientador querendo tirar os menores de 18. No Quarto, isso é uma linha de código: `filter(idade >= 18)`. Salvo. Renderizo de novo. Tabela 1, Tabela 3, Figura 2, todas se atualizaram juntas, com o n correto, com o p-valor correto, com os números do texto correto. Não tem como esquecer.

---

## Slide 13 — Um arquivo. Vários formatos.

**Texto na tela:**
> `.qmd` → HTML, PDF, Word, slides

**Visual:** [PLACEHOLDER — diagrama mostrando um arquivo `.qmd` no centro e quatro saídas: HTML (página web), PDF, DOCX, slides Reveal.js].

**Fala (~2,5 min):**
O mesmo `.qmd` exporta para múltiplos formatos. Site na web? `format: html`. PDF para submeter na revista? `format: pdf`. Word porque o coorientador só revisa em Word? `format: docx`. Slides para apresentar em congresso? `format: revealjs`. O conteúdo é o mesmo. Você não escreve quatro versões — você escreve uma.

---

## Slide 14 — E quem escreve o `.qmd`?

**Texto na tela:**
> E o código?
> Quem escreve?

**Visual:** silhueta de uma pessoa olhando para um arquivo. Tom de mistério/transição.

**Fala (~1 min):**
Aí volta a dúvida que provavelmente todos aqui têm: "tudo isso parece ótimo, mas eu não sei R nem Python." Resposta: você não precisa.

---

## Slide 15 — Claude Cowork

**Texto na tela:**
> Claude Cowork
> Você descreve. Ele escreve.

**Visual:** logo do Claude (Anthropic) ao lado de um cursor digitando. Tom limpo.

**Fala (~2 min):**
O Claude Cowork é um agente de IA — não um chatbot. A diferença: ele não só responde, ele *executa* no seu computador. Ele cria arquivos, escreve código, roda análises. Você fala em português o que quer ("compare a idade entre os dois grupos com teste t e me dê uma tabela"), ele escreve o `.qmd` correspondente e renderiza para você ver.

---

## Slide 16 — Demo: Cowork criando o `.qmd`

**Texto na tela:** (apenas legenda)
> Conversa → arquivo `.qmd` pronto

**Visual:** [PLACEHOLDER — screenshot ou GIF mostrando o painel do Cowork à esquerda com um pedido em português, e o arquivo `.qmd` sendo escrito à direita; preferencialmente mostrar também o preview renderizado].

**Fala (~2,5 min):**
*(Demo ao vivo se possível, ou narrar o screenshot.)* O Cowork não é um chatbot que sugere código pra você copiar. Ele cria o arquivo. Salva. Roda. Mostra o resultado. Se você pede uma mudança, ele edita o arquivo. Se algo falha, ele lê o erro e corrige. O papel do pesquisador deixa de ser "escrever código" e passa a ser "saber pedir e validar".

---

## Slide 17 — O loop fechado

**Texto na tela:**
> Dado bruto → análise → artigo
> em um arquivo

**Visual:** diagrama circular fechado: dado → análise → texto → render → submissão. Setas conectando.

**Fala (~2 min):**
Esse é o loop fechado da pesquisa reprodutível. Do dado bruto à figura na revista, sem perder rastreabilidade. Daqui a dois anos, quando o revisor pedir uma análise adicional, você abre o `.qmd`, muda uma linha, renderiza. Cinco minutos. E fica documentado o que mudou.

---

## Slide 18 — Aprofundar: o curso

**Texto na tela:**
> Vibe Coding na Pesquisa Científica
> Curso completo
> henriquealvarenga.com/vibe-coding

**Visual:** captura da home do site (`index.qmd` renderizado), com URL embaixo. Discreto.

**Fala (~3 min):**
Tudo isso vai mais fundo num curso que estou montando: Vibe Coding na Pesquisa Científica. São seis módulos — Setup, Trabalhando com IA, Fundamentos técnicos, Análise de dados, Publicação e reprodutibilidade, e um projeto final. Conteúdo aberto, no site. Encerrar com convite a perguntas.

---

## Notas para o gerador (Gamma)

- **Idioma:** PT-BR.
- **Tom:** acadêmico mas conversacional. Não usar emojis.
- **Tipografia:** se possível, sans-serif limpa para títulos (Inter ou similar) e monoespaçada para código (JetBrains Mono).
- **Paleta:** tons escuros com um acento *teal* (`#00d9c0`) para títulos e elementos de destaque, alinhado com a identidade visual do projeto Quarto. Branco/cinza-claro para o corpo do texto.
- **Densidade:** poucas palavras na tela. Em qualquer slide, se houver mais de 12 palavras visíveis, repensar.
- **Imagens [PLACEHOLDER]:** deixar áreas grandes reservadas para que o autor insira screenshots reais depois. Evitar imagens genéricas de banco *(stock)* nesses lugares.
