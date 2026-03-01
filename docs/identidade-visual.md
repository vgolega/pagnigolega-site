# Identidade Visual - Pagni & Golegã

**Data:** 2026-02-28
**Status:** APROVADA

---

## Paleta Escolhida: Azul Naval + Prata (Opção 2)

### Cores

| Uso | Nome | Hex | Aplicação |
|-----|------|-----|-----------|
| **Primária** | Azul Naval | `#1a2a5e` | Headers, títulos, botões principais |
| **Primária Clara** | Azul Naval Claro | `#2d3a6e` | Hover, gradientes |
| **Primária Escura** | Azul Escuro | `#0f172a` | Footer, fundos escuros |
| **Secundária** | Prata | `#9ca3af` | Destaques, linhas decorativas |
| **Cinza** | Slate 600 | `#64748b` | Textos secundários |
| **Fundo** | Slate 50 | `#f8fafc` | Fundos de seção |
| **Branco** | White | `#ffffff` | Fundos principais, textos em fundos escuros |

### Variáveis CSS

```css
:root {
  --color-primary: #1a2a5e;
  --color-primary-light: #2d3a6e;
  --color-primary-dark: #0f172a;
  --color-silver: #9ca3af;
  --color-silver-dark: #6b7280;
  --color-gray-50: #f8fafc;
  --color-gray-600: #64748b;
  --color-gray-900: #0f172a;
}
```

---

## Tipografia

| Uso | Fonte | Pesos | Fallback |
|-----|-------|-------|----------|
| **Headlines** | Playfair Display | 400, 500, 600, 700 | Georgia, serif |
| **Body** | Inter | 400, 500, 600, 700 | -apple-system, sans-serif |

### Aplicação

- **H1:** Playfair Display Bold, 2.5-3.75rem
- **H2:** Playfair Display Bold, 1.875-2.25rem
- **H3:** Playfair Display Semibold, 1.25rem
- **Body:** Inter Regular, 1rem
- **Small:** Inter Regular, 0.875rem

---

## Logo

**Arquivos disponíveis em `/public/images/`:**

| Arquivo | Uso |
|---------|-----|
| `pg.jpg` | Logo circular (monograma) - usado no header |
| `P&G.jpg` | Logo completo com nome - usado na seção "Sobre" |
| `logo.jpg` | Logo horizontal |
| `p&Glogo_xícara.png` | Wordmark |

---

## Componentes

### Botões

**Primário:**
```css
background: #1a2a5e;
color: white;
hover: #2d3a6e;
```

**Secundário:**
```css
background: transparent;
border: 2px solid rgba(255,255,255,0.4);
color: white;
```

**WhatsApp:**
```css
background: #16a34a;
color: white;
hover: #15803d;
```

### Cards

```css
background: white;
border: 1px solid #e2e8f0;
border-radius: 0.75rem;
hover-border: #1a2a5e;
```

### Linhas Decorativas

```css
width: 4rem;
height: 0.25rem;
background: #9ca3af;
```

---

## Áreas de Atuação

1. Família e Sucessões
2. Planejamento Sucessório
3. Direito à Saúde
4. Consumidor
5. Trabalhista
6. Criminal

---

## Contato

- **WhatsApp:** +55 11 93730-5492
- **Mensagem padrão:** "Olá! Vim pelo site e gostaria de mais informações."
- **Link:** `https://wa.me/5511937305492?text=...`

---

## Notas de Implementação

- Cores aplicadas com valores hexadecimais inline via Tailwind
- Fontes importadas via Google Fonts no `global.css`
- Logo circular usado no Header e Footer
- Linha decorativa (prata) usada abaixo de títulos de seção
- Footer com fundo escuro (#0f172a)

---

*Documento atualizado em 2026-02-28*
*Paleta aprovada pelo cliente*
