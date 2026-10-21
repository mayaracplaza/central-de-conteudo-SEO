# Central SEO — Agência FG

Ferramenta interna para gestão completa de operações SEO: criação de conteúdo, briefing, aprovação de clientes e controle de fluxo, feita para o time da Agência FG.

🔗 **Demo:** https://mayaracplaza.github.io/central-de-conteudo-SEO/

---

## O que é

Um app front-end (HTML/CSS/JS puro, sem build) que substitui o processo manual de criação de conteúdo SEO — do briefing até a aprovação do cliente — eliminando a dependência do Google Docs e os problemas de formatação que surgiam ao copiar conteúdo para o site.

**Problema que resolve:** o conteudista criava o conteúdo no Google Docs com tags SEO (H1, H2, negritos, links), enviava por e-mail para o cliente aprovar, e quando o dev publicava, a formatação frequentemente quebrava. A Central SEO gera o código HTML limpo direto, pronto para publicação.

---

## Funcionalidades atuais

### Conteúdos e-commerce

**Abas internas**
- ✍️ **Criar conteúdo** — espaço de trabalho do conteudista
- 📝 **Rascunhos** — conteúdos em andamento, salvos e editáveis
- 📋 **Fila** — kanban de status: Aguardando aprovação → Ajustes → Publicar

**Importação de planilha**
Importa o cronograma de conteúdos (.xlsx) e preenche o briefing automaticamente ao selecionar um conteúdo da lista — palavra-chave, justificativa, campo semântico, perguntas e linkagens já vêm preenchidos.

**Briefing do conteúdo**
H1, título SEO e meta description com contador de caracteres, palavra-chave principal, campo semântico, justificativa, perguntas e linkagens.

**Sugestão por IA**
Geração assistida de título e meta description via Claude.ai (requer estar rodando dentro do Claude.ai).

**Editor com preview em tempo real**
Editor rich text (negrito, itálico, headings, listas, links) com toggle para visualizar o código-fonte e preview renderizado no estilo visual do cliente.

**Checagens automáticas de SEO**
Contagem de palavras, presença da palavra-chave no H1/título e no primeiro parágrafo, hierarquia de headings, quantidade de links internos, limites de título/meta.

**Rascunhos**
Salva conteúdos em andamento por cliente. Qualquer rascunho pode ser retomado e editado antes de enviar para aprovação.

**Fluxo de aprovação**
Fila → Aguardando aprovação → Ajustes → Publicar, com contador de ajustes solicitados por cliente.

**Histórico de versões**
Organizado por ano/mês, com exportação em planilha (.csv) e geração de Folha de Rosto (.docx).

### Visão do cliente

Tela separada acessada pela tela inicial — o cliente faz login, revisa os conteúdos enviados, aprova ou solicita ajustes com comentário. Sem acesso a nenhuma parte interna da agência.

### Cadastro de clientes

Domínio, plataforma (VTEX IO, Linx, Shopify etc.), formato de saída (Markdown ou HTML), limites de título/meta, sufixos fixos de SEO e estilo visual do preview para o preview ficar igual ao site real.

---

## Armazenamento atual

Os dados ficam salvos no `localStorage` do navegador, organizados por cliente. Cada navegador tem sua própria cópia — dados não são compartilhados entre pessoas do time ainda.

---

## Próximos passos

### Fase 1 — Supabase (banco compartilhado)
Substituir o `localStorage` por um banco de dados centralizado na nuvem. Com isso:
- Rascunhos, fila e histórico ficam acessíveis para todo o time
- Dados não somem ao limpar o cache
- Cada ação fica registrada com autoria

### Fase 2 — Login por Gmail
Autenticação via Google para cada pessoa do time e para os clientes:
- **Admin (Mayara)** — vê todos os clientes, atribui conteudistas
- **Conteudistas (João Victor, Marina, Sarah)** — veem só seus clientes atribuídos
- **Clientes** — acessam só o dashboard de aprovação dos próprios conteúdos

### Fase 3 — Publicação direta na VTEX
Botão "Publicar" após aprovação do cliente, enviando o conteúdo direto para a loja via API VTEX. As credenciais (App Key + Token) ficam guardadas com segurança no Supabase, nunca expostas no código.

---

## Como atualizar no GitHub Pages

1. Baixe o arquivo atualizado
2. Renomeie para `index.html`
3. No repositório GitHub: **Add file → Upload files**
4. Substitua o `index.html` existente e confirme o commit
5. Aguarde 1-2 minutos para o GitHub Pages atualizar

---

## Como rodar localmente

```bash
git clone https://github.com/mayaracplaza/central-de-conteudo-SEO.git
cd central-de-conteudo-SEO
```

Abra o `index.html` diretamente no navegador ou use um servidor estático:

```bash
npx serve
```

---

## Stack

- HTML, CSS e JavaScript puro (sem frameworks ou build tools)
- Geração de `.docx` via ZIP + OOXML nativo (sem bibliotecas externas)
- Leitura de `.xlsx` via SheetJS (carregado sob demanda)
- Fontes: Newsreader, Public Sans e JetBrains Mono (Google Fonts)
- Publicado via GitHub Pages

---

Desenvolvido por [Mayara Plaza](https://github.com/mayaracplaza) para a Agência FG.
