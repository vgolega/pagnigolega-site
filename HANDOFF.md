# HANDOFF - Site Pagni & Golegã

**Data:** 2026-02-28
**Projeto:** Migração do site do Wix para Astro

---

## Goal

Criar um novo site para o escritório de advocacia **Pagni & Golegã** migrando do Wix para uma solução estática com Astro + Tailwind CSS, hospedado na Vercel (gratuito).

O site deve:
- Ter identidade visual profissional (paleta Azul Naval + Prata aprovada)
- Conter páginas: Home, Sobre, Áreas de Atuação, Blog, Contato
- Migrar 17 artigos do blog atual do Wix
- Integrar WhatsApp com mensagem pré-preenchida
- Ser otimizado para SEO e performance

---

## Current Progress

### Concluído

1. **Setup do projeto**
   - Projeto Astro inicializado em `/root/projetos/pagnigolega-site/`
   - Tailwind CSS configurado
   - Estrutura de pastas criada

2. **Identidade Visual**
   - 6 paletas foram propostas ao cliente
   - **Aprovada: Opção 2 - Azul Naval + Prata**
   - Cores principais:
     - Primária: `#1a2a5e` (Azul Naval)
     - Secundária: `#9ca3af` (Prata)
     - Footer: `#0f172a`
   - Tipografia: Playfair Display (headlines) + Inter (body)
   - Documentação em `docs/identidade-visual.md`

3. **Logos**
   - Copiados para `/public/images/`
   - Arquivos: `pg.jpg`, `P&G.jpg`, `logo.jpg`, `p&Glogo_xícara.png`

4. **Páginas criadas (todas funcionando)**
   - `src/pages/index.astro` - Home
   - `src/pages/sobre.astro` - Sobre o escritório
   - `src/pages/areas-de-atuacao.astro` - 6 áreas listadas
   - `src/pages/contato.astro` - Formulário + WhatsApp
   - `src/pages/blog/index.astro` - Listagem de artigos
   - `src/pages/blog/[...slug].astro` - Artigo individual

5. **Componentes**
   - `src/components/Header.astro` - Com logo e navegação responsiva
   - `src/components/Footer.astro` - Com áreas, links e WhatsApp
   - `src/layouts/Base.astro` - Layout base com SEO
   - `src/layouts/BlogPost.astro` - Layout para artigos

6. **Blog**
   - Content collection configurada em `src/content.config.ts`
   - Um artigo de exemplo criado: `src/content/blog/exemplo-artigo.md`

7. **Informações do cliente**
   - WhatsApp: `+5511937305492`
   - Áreas: Família e Sucessões, Planejamento Sucessório, Direito à Saúde, Consumidor, Trabalhista, Criminal
   - Domínio: pagnigolega.com.br

---

## What Worked

- **Astro + Tailwind**: Setup rápido e build funcionando
- **Google Fonts via CSS**: Playfair Display + Inter carregando bem
- **Content Collections**: Sistema de blog com Markdown funcionando
- **Componentes reutilizáveis**: Header e Footer compartilhados
- **Preview local**: `npm run preview` funciona em http://localhost:4321
- **Demonstração de paletas**: Criado `demo-paletas.html` para cliente visualizar opções

---

## What Didn't Work

- **WebFetch no blog do Wix**: O Wix usa JavaScript para renderizar conteúdo, então WebFetch não consegue extrair os artigos. Retorna apenas código técnico, não o conteúdo real.
- **Preview HTML direto**: Abrir o HTML gerado direto do sistema de arquivos não funciona porque as referências CSS são relativas. Precisa de servidor local.

---

## Next Steps

### Imediato: Migrar os 17 artigos do Wix

O cliente precisa fornecer o conteúdo dos artigos. Opções:
1. Copiar manualmente cada artigo para arquivo .txt/.docx
2. Exportar do painel do Wix (Blog > Posts)
3. Fornecer links individuais para tentar acessar um por um

**Template para artigos** (`src/content/blog/nome-do-artigo.md`):
```markdown
---
title: "Título do Artigo"
description: "Descrição para SEO (máx 160 caracteres)"
pubDate: 2026-01-15
author: "Pagni & Golegã"
tags: ["família", "sucessões"]
---

Conteúdo do artigo em Markdown...
```

### Depois da migração

1. **Configurar Formspree** para o formulário de contato
   - Criar conta em formspree.io
   - Substituir `YOUR_FORM_ID` em `src/pages/contato.astro`

2. **Deploy na Vercel**
   - Criar conta na Vercel
   - Conectar repositório Git
   - Apontar domínio pagnigolega.com.br

3. **SEO final**
   - Criar `public/robots.txt`
   - Gerar sitemap (Astro tem integração)
   - Configurar redirects 301 se URLs mudarem

4. **Testes de performance**
   - Rodar Lighthouse
   - Meta: 90+ em Performance, SEO, Accessibility

---

## Arquivos Importantes

| Arquivo | Descrição |
|---------|-----------|
| `CLAUDE.md` | Instruções do agente WebDev |
| `docs/identidade-visual.md` | Paleta aprovada e especificações |
| `src/content.config.ts` | Configuração do blog |
| `src/styles/global.css` | Variáveis CSS e fontes |

---

## Comandos

```bash
cd /root/projetos/pagnigolega-site

npm run dev      # Desenvolvimento (localhost:4321)
npm run build    # Build de produção
npm run preview  # Preview do build
```

---

## Plano Completo

O plano detalhado está em:
`/root/projetos/.ideias/plans/agente-webdev-pagnigolega.md`

---

## Contexto Adicional

- Cliente não é programador, precisa de explicações simples
- Responder em português
- Site atual: https://www.pagnigolega.com.br/ (Wix)
- O cliente está aberto a sugestões mas quer validar mudanças visuais
