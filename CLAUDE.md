# CLAUDE.md - Site Pagni & Golegã

## Contexto

Site institucional do escritório **Pagni & Golegã Consultoria Jurídica**.

- **URL atual (Wix):** https://www.pagnigolega.com.br/
- **Domínio:** pagnigolega.com.br
- **Público-alvo:** Pessoa física e jurídica, Estado de São Paulo
- **Propósito:** Portfólio institucional + Blog jurídico

## Stack Tecnológico

| Componente | Tecnologia |
|------------|------------|
| Framework | Astro |
| Estilização | Tailwind CSS |
| Hospedagem | Vercel |
| Formulário | Formspree |
| Analytics | A definir |

## Comandos

```bash
# Desenvolvimento
npm run dev          # Servidor local (localhost:4321)
npm run build        # Build de produção
npm run preview      # Preview do build

# Deploy
# Push para branch `main` dispara deploy automático na Vercel
```

## Estrutura do Projeto

```
src/
├── components/      # Componentes reutilizáveis (Header, Footer, etc.)
├── layouts/         # Layouts de página (Base, BlogPost)
├── pages/           # Páginas do site
│   ├── index.astro          # Home
│   ├── sobre.astro          # Sobre o escritório
│   ├── areas-de-atuacao.astro
│   ├── contato.astro
│   └── blog/
│       ├── index.astro      # Lista de artigos
│       └── [...slug].astro  # Artigo individual
├── content/         # Conteúdo em Markdown
│   └── blog/        # Artigos do blog
└── styles/          # Estilos globais
```

## Identidade Visual

### Cores (A VALIDAR)
- Primária: A definir
- Secundária: A definir
- Neutras: A definir

### Tipografia (A VALIDAR)
- Headlines: A definir
- Body: A definir

### Referência do Site Atual
- Azul primário: #0f2ccf, #2f5dff
- Neutros: #151414, #767574, #a8a6a5
- Tipografia: Madefor Display

## Estrutura de Conteúdo

### Adicionar Novo Artigo

1. Criar arquivo em `src/content/blog/nome-do-artigo.md`
2. Usar o template:

```markdown
---
title: "Título do Artigo"
description: "Descrição para SEO (máx 160 caracteres)"
pubDate: 2026-02-28
author: "Nathalie Pagni"
tags: ["direito civil", "família"]
image: "/images/blog/nome-da-imagem.jpg"  # opcional
---

Conteúdo do artigo aqui em Markdown...

## Subtítulo

Mais conteúdo...
```

### Editar Páginas

- Páginas estão em `src/pages/`
- Use componentes de `src/components/` para manter consistência
- Mantenha a responsividade mobile

## Regras do Agente

### SEMPRE fazer:
- Validar mudanças visuais significativas antes de implementar
- Manter código limpo e bem organizado
- Testar responsividade em mobile
- Otimizar imagens antes de adicionar
- Seguir boas práticas de SEO
- Seguir WCAG para acessibilidade

### NUNCA fazer:
- Alterar conteúdo jurídico sem aprovação explícita
- Remover funcionalidades sem consultar
- Fazer deploy sem testes
- Ignorar erros de build

### Validações Obrigatórias
- Mudanças na identidade visual precisam de aprovação
- Novos artigos devem seguir o template
- Alterações em textos jurídicos requerem revisão

## Funcionalidades

### WhatsApp
- Botão com mensagem pré-preenchida
- Formato: `https://wa.me/55XXXXXXXXXXX?text=MENSAGEM`
- Mensagem padrão: "Olá! Vim pelo site e gostaria de mais informações."

### Formulário de Contato
- Integrado com Formspree
- Campos: Nome, Email, Telefone, Assunto, Mensagem
- Validação client-side

### SEO
- Meta tags em todas as páginas
- Open Graph para redes sociais
- Schema.org para rich snippets
- Sitemap automático
- robots.txt configurado

## Critérios de Qualidade

| Métrica | Alvo |
|---------|------|
| Lighthouse Performance | 90+ |
| Lighthouse SEO | 95+ |
| Lighthouse Accessibility | 90+ |
| Tempo de carregamento | < 2s |

## Fases do Projeto

- [x] Fase 0: Setup inicial
- [ ] Fase 1: Identidade visual (propor opções, validar)
- [ ] Fase 2: Desenvolvimento das páginas
- [ ] Fase 3: Blog e migração de conteúdo (17 artigos)
- [ ] Fase 4: Otimização e deploy
- [ ] Fase 5: Pós-lançamento
- [ ] Fase Futura: Integração PartilhaFácil

## Links Úteis

- **Plano completo:** `/root/projetos/.ideias/plans/agente-webdev-pagnigolega.md`
- **Documentação Astro:** https://docs.astro.build
- **Documentação Tailwind:** https://tailwindcss.com/docs
- **Vercel:** https://vercel.com/docs

## Contato do Cliente

Para validações e aprovações, consultar o usuário diretamente na conversa.
