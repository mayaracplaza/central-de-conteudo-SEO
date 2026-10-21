# Central SEO — Agência FG

Ferramenta interna para gestão completa de operações SEO: criação de conteúdo, briefing, aprovação de clientes e auditoria técnica, feita para o fluxo de trabalho da Agência FG.

🔗 **Demo:** https://mayaracplaza.github.io/central-de-conteudo-SEO/

---

## O que é

Um app front-end (HTML/CSS/JS puro, sem build) que centraliza o processo de criação de conteúdo SEO por cliente: do briefing até a aprovação, passando por rascunhos e controle de filas, com preview do conteúdo no estilo visual do site do cliente.

---

## Principais funcionalidades

### Conteúdos e-commerce

**Importação de planilha**
Importa o cronograma de conteúdos (.xlsx) e preenche o briefing automaticamente ao selecionar um conteúdo da lista.

**Briefing do conteúdo**
H1, título SEO e meta description com contador de caracteres, palavra-chave principal, campo semântico, justificativa, perguntas e linkagens.

**Sugestão por IA**
Geração assistida de título e meta description via Claude.ai (requer conexão com a internet).

**Editor com preview em tempo real**
Editor rich text (negrito, itálico, headings, listas, links) com toggle para visualizar o código-fonte e preview renderizado no estilo do cliente.

**Checagens automáticas de SEO**
Contagem de palavras, presença da palavra-chave no H1/título e no primeiro parágrafo, hierarquia de headings, quantidade de links internos, limites de título/meta.

**Rascunhos**
Salva conteúdos em andamento por cliente. Qualquer rascunho pode ser retomado e editado antes de enviar para aprovação.

**Fluxo de aprovação**
Fila → Aguardando aprovação → Ajustes → Publicar, com contador de ajustes solicitados por cliente.

**Histórico de versões**
Organizado por ano/mês, com exportação em planilha (.csv) e geração de Folha de Rosto (.docx).

**Visão do cliente**
Tela separada onde o cliente revisa, aprova ou solicita ajustes nos conteúdos enviados.

### Cadastro de clientes

Domínio, plataforma (VTEX IO, Linx, Shopify etc.), formato de saída (Markdown ou HTML), limites de título/meta, sufixos fixos de SEO e estilo visual do preview (fonte, tamanhos, cores) para o preview ficar igual ao site real.

---

## Como usar

Basta abrir o `index.html` no navegador — não tem dependências externas nem processo de build.

```bash
git clone https://github.com/mayaracplaza/central-de-conteudo-SEO.git
cd central-de-conteudo-SEO
```

Depois abra o `index.html` diretamente ou sirva a pasta com qualquer servidor estático:

```bash
npx serve
```

---

## Como atualizar no GitHub Pages

1. Baixe o arquivo atualizado
2. Renomeie para `index.html`
3. No repositório GitHub: **Add file → Upload files**
4. Substitua o `index.html` existente e confirme o commit
5. Aguarde 1-2 minutos para o GitHub Pages atualizar

---

## Armazenamento

Os dados ficam salvos no `localStorage` do navegador, organizados por cliente. Por enquanto cada navegador tem sua própria cópia — integração com banco de dados compartilhado (Supabase) está planejada para a próxima fase.

---

## Stack

- HTML, CSS e JavaScript puro (sem frameworks ou build tools)
- Geração de `.docx` via ZIP + OOXML nativo (sem bibliotecas externas)
- Leitura de `.xlsx` via SheetJS (carregado sob demanda)
- Fontes: Newsreader, Public Sans e JetBrains Mono (Google Fonts)
- Publicado via GitHub Pages

---

## Status

Projeto em desenvolvimento ativo. As funcionalidades de IA dependem de estar rodando dentro do Claude.ai.

Desenvolvido por [Mayara Plaza](https://github.com/mayaracplaza) para a Agência FG.
