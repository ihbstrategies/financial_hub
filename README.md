# Financial Hub

App instalável (PWA) do controle financeiro **M&M** — publicado via GitHub Pages e
"adicionar à tela inicial" no celular.

## O que é (e o que não é)
- Este repositório contém **apenas a casca do app** (`docs/`): HTML/CSS/JS da interface,
  ícones e o service worker. **Nenhum dado financeiro** e **nenhum token** ficam aqui —
  por isso o repositório pode ser público.
- Os dados vêm **em tempo real** de uma API no Google Apps Script, protegida por **token**.
  O token é pedido **uma vez** no app e guardado só no aparelho (`localStorage`).
- Funciona **offline**: cacheia os dados e enfileira as edições, que sobem ao reconectar.

## Publicar / atualizar
O `docs/` é gerado pelo `build-web.mjs` do projeto (fora deste repo). Para atualizar:
1. No projeto, rode o build (gera `docs/`).
2. Copie o `docs/` para cá, `git add docs && git commit && git push`.

Pages: **Settings → Pages → Source: `main` / `/docs`**. A URL fica
`https://ihbstrategies.github.io/financial_hub/`.

## Instalar no celular
Abrir a URL do Pages → **Compartilhar → Adicionar à Tela de Início** (iPhone) ou
menu ⋮ → **Instalar app** (Android). Na primeira abertura, cole o **token**.
