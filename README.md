# Central de Conteúdo SEO

Ferramenta interna para briefing, criação e publicação de conteúdos otimizados para SEO, feita para o fluxo de trabalho da Agência FG com seus clientes.

🔗 **Demo:** https://mayaracplaza.github.io/central-de-conteudo-SEO/

## O que é

Um app front-end (HTML/CSS/JS puro, sem build) que centraliza o processo de criação de conteúdo SEO por cliente: do briefing até a publicação, passando por aprovação e ajustes, com preview do conteúdo já no estilo visual do site do cliente.

## Principais funcionalidades

- **Cadastro de cliente**: domínio, plataforma (VTEX IO, Linx, etc.), formato de saída (Markdown, HTML simples ou HTML com wrapper customizado), limites de título/meta, sufixos fixos de SEO e estilo visual do preview (fonte, tamanhos, cores), pra o preview ficar igual ao site real.
- **Briefing do conteúdo**: H1, título SEO e meta description com contador de caracteres, palavra-chave principal, campo semântico, justificativa, perguntas e linkagens. Suporta importação via planilha.
- **Sugestão por IA**: geração assistida de título e meta description (requer conexão com a internet, roda via Claude.ai).
- **Editor com preview em tempo real**: editor rich text (negrito, itálico, headings, listas, links) com toggle para visualizar o código-fonte e preview renderizado no estilo do cliente.
- **Checagens automáticas de SEO**: contagem de palavras, presença da palavra-chave no H1/título e no primeiro parágrafo, hierarquia de headings, quantidade de links internos, limites de título/meta.
- **Fluxo de aprovação**: Fila → Aguardando → Ajustes → Publicar, com contador de ajustes solicitados por cliente e insights gerados por IA sobre os padrões de revisão.
- **Histórico de versões**: organizado por ano/mês, com exportação em planilha.
- **Visão do cliente (demonstração)**: prévia de como ficaria a tela do cliente revisando e aprovando conteúdos.

## Como usar

Basta abrir o `index.html` no navegador — não tem dependências externas nem processo de build. Para rodar localmente:

```bash
git clone https://github.com/mayaracplaza/central-de-conteudo-SEO.git
cd central-de-conteudo-SEO
```

Depois é só abrir o `index.html` diretamente ou servir a pasta com qualquer servidor estático (ex: `npx serve`).

## Stack

- HTML, CSS e JavaScript puro (sem frameworks ou build tools)
- Fontes: Newsreader, Public Sans e JetBrains Mono (Google Fonts)
- Publicado via GitHub Pages

## Status

Projeto em desenvolvimento ativo — as funcionalidades de IA dependem de estar rodando dentro do Claude.ai.

---

Desenvolvido por [Mayara Plaza](https://github.com/mayaracplaza) para a Agência FG.
