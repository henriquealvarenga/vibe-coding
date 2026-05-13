# Vibe Coding na Pesquisa Científica

Curso sobre o uso de agentes de IA na pesquisa médica e científica — concebido como um site público em [Quarto](https://quarto.org).

🌐 **Site:** <https://henriquealvarenga.com/vibe-coding>

## Sobre o curso

Disciplina concebida para docentes universitários e pesquisadores que querem incorporar agentes de IA (Claude, Codex, Gemini) ao trabalho diário de pesquisa: análise de dados em R/Python, escrita técnica em Quarto, publicação reprodutível na web. Não exige pré-requisito técnico em programação — começa do "Terminal? o que é isso?" e vai até "publiquei um artigo reprodutível com DOI no Zenodo".

A tese central é o **vibe coding**: você descreve em português brasileiro o que precisa, a IA escreve o código, você valida e adapta. O curso ensina como fazer isso bem (e quais armadilhas evitar) no contexto específico da pesquisa científica, onde a régua de exigência é maior que a de um chat conversacional.

## Estrutura

O curso é organizado em **6 Módulos** com **14 Blocos** e **91 capítulos**:

- **Módulo 0** — Setup (instalações)
- **Módulo 1** — Trabalhando com IA na pesquisa (conceitos, agentes, padrões de prompts, limites)
- **Módulo 2** — Fundamentos técnicos (terminal, ambientes, convenções)
- **Módulo 3** — Análise de dados e escrita técnica (Markdown/Quarto, dados, Python e R)
- **Módulo 4** — Publicação e reprodutibilidade (Git, GitHub, GitHub Pages, FAIR, Zenodo)
- **Módulo 5** — Capstone (projeto integrador aplicado à docência)

A ementa completa, com decisões editoriais documentadas, está em [`planejamento/ementa.md`](planejamento/ementa.md).

## Status

Em construção. Material sendo escrito e revisado ao longo de 2026. Alguns capítulos ainda em rascunho; o site sinaliza quando esse é o caso. Feedback é bem-vindo via *issues* no GitHub.

## Como reutilizar

Material licenciado sob [Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE) — você pode usar, modificar e redistribuir (inclusive comercialmente) desde que atribua o autor.

Atribuição sugerida:

> Henrique Alvarenga da Silva. *Vibe Coding na Pesquisa Científica*. 2026. Disponível em <https://henriquealvarenga.com/vibe-coding>. Licença: CC BY 4.0.

## Como renderizar localmente

O site é construído com Quarto. Para gerar localmente:

```bash
quarto preview      # com hot-reload no navegador
quarto render       # gera os HTMLs em docs/
```

## Como contribuir

Encontrou um erro factual, link quebrado, referência mal citada, ou tem sugestão? Abra uma *issue* descrevendo o problema, ou um *pull request* com a correção. Convenções de redação e de uso de IA estão em [`AGENTS.md`](AGENTS.md).

## Autor

**Henrique Alvarenga da Silva** — psiquiatra, professor de Medicina.

Site: <https://henriquealvarenga.com> · GitHub: [@henriquealvarenga](https://github.com/henriquealvarenga)
