# LP Pedro v2 — Site Profissional para Médicos

Landing page de vendas da Laender Software, construída com Astro 5 + Tailwind v4.

## Setup

```bash
npm install
npm run dev
```

O site estará disponível em `http://localhost:4321`.

## Build & Preview

```bash
npm run build
npm run preview
```

Os arquivos estáticos serão gerados em `dist/`.

## Deploy (Vercel)

1. Conecte o repositório ao Vercel
2. Framework preset: **Astro**
3. Build command: `npm run build`
4. Output directory: `dist`

Ou via CLI:

```bash
npx vercel --prod
```

## Estrutura

```
src/
├── layouts/Layout.astro        — Layout base com meta tags, OG, Google Fonts
├── styles/global.css           — Tailwind v4 import + tema customizado
├── components/
│   ├── Header.astro            — Header fixo com CTA WhatsApp
│   ├── Hero.astro              — Headline principal + CTA
│   ├── ArgumentoCentral.astro  — Argumento de autoridade
│   ├── Dores.astro             — Pain points (5 cards)
│   ├── ComoFunciona.astro      — 4 steps do processo
│   ├── JornadaPaciente.astro   — Jornada do paciente
│   ├── Bundles.astro           — O que está incluso (4 bundles)
│   ├── Bonus.astro             — Bônus inclusos
│   ├── Preco.astro             — Pricing card
│   ├── Garantia.astro          — Garantia de 14 dias
│   ├── Depoimentos.astro       — Placeholder para depoimentos
│   ├── FAQ.astro               — 8 perguntas frequentes
│   ├── CTAFinal.astro          — CTA final com WhatsApp
│   ├── Footer.astro            — Footer
│   └── WhatsAppButton.astro    — Botão flutuante WhatsApp
└── pages/index.astro           — Página principal (monta todos os componentes)
```

## Personalização

- **WhatsApp link**: definido como constante em `src/pages/index.astro`, passado via props
- **Cores**: tema definido em `src/styles/global.css` via `@theme`
- **Fontes**: Playfair Display (headings) + Inter (body) via Google Fonts
- **Textos**: todos vindos da copy aprovada, editáveis diretamente nos componentes

## Stack

- Astro 5 (static output)
- Tailwind CSS v4 (via @tailwindcss/vite)
- Zero frameworks JS — apenas Intersection Observer para animações
- Google Fonts (Playfair Display + Inter)
