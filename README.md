# Conteúdo LAF

Hub de reports e páginas estáticas do time de conteúdo da LAF.

## Estrutura

```
/
  index.html                          # Hub (browseable no GitHub / htmlpreview)
  reports/
    2026-09-04-criadores/index.html   # Report de monitoramento de criadores
  public/                             # Mirror para Cloudflare Workers (assets)
    index.html
    reports/...
  wrangler.jsonc
  .nojekyll
```

- **Root** (`index.html` + `reports/…`): caminhos simples para GitHub Pages / [htmlpreview](https://htmlpreview.github.io/).
- **`public/`**: mesmo conteúdo, pasta de assets do Wrangler.

## Deploy

Deploy via **Cloudflare Workers** com static assets:

- Worker name: `laf-conteudo`
- Assets directory: `./public`
- Domínio customizado planejado: **conteudo.agencialaf.com**

```bash
npx wrangler deploy
```

## Preview temporário (htmlpreview)

- Hub: https://htmlpreview.github.io/?https://raw.githubusercontent.com/rafaelrards/laf-criadores-report/main/index.html
- Report criadores (2026-09-04): https://htmlpreview.github.io/?https://raw.githubusercontent.com/rafaelrards/laf-criadores-report/main/reports/2026-09-04-criadores/index.html

## Reports

| Data | Título | Path |
|------|--------|------|
| 2026-09-04 | Monitoramento Criadores | [`reports/2026-09-04-criadores/`](reports/2026-09-04-criadores/) |

Uso interno · Paulo · LAF
