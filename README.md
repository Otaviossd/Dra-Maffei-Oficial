# Site — Dra. Gabriela Mafei

Site institucional de página única. HTML puro, sem build, sem dependências de instalação.
Fotos e estilos estão embutidos no próprio `index.html`.

## Arquivos

| Arquivo | Para que serve | Pode remover? |
|---|---|---|
| `index.html` | O site inteiro | Não |
| `og-image.jpg` | Miniatura que aparece ao compartilhar o link no WhatsApp/Instagram | Não |
| `vercel.json` | Regras de cache (só usado pela Vercel) | Sim, se não usar Vercel |
| `.nojekyll` | Impede o GitHub Pages de processar os arquivos | Sim, se não usar Pages |

> Os três primeiros precisam ficar **na mesma pasta**, no nível raiz.

## Publicar pela Vercel (recomendado)

1. Suba os arquivos num repositório do GitHub
2. Em vercel.com → **Add New → Project** → importe o repositório
3. Framework Preset: **Other**. Não preencha build nem output.
4. Deploy

Sai em `<nome>.vercel.app`. Domínio próprio em Settings → Domains.

## Publicar pelo GitHub Pages

Settings → Pages → Source: `main`, pasta `/ (root)`.

⚠️ O Pages publica em `usuario.github.io/repositorio/`, um subcaminho.
Nesse caso é obrigatório trocar a linha da og:image no `index.html`:

```html
<meta property="og:image" content="https://usuario.github.io/repositorio/og-image.jpg">
```

O mesmo vale para a linha `twitter:image`.

## Depois de publicar

Assim que tiver o domínio final, troque `/og-image.jpg` pela URL absoluta
nas duas linhas (`og:image` e `twitter:image`). É o que garante a miniatura
correta no WhatsApp.

Para testar a miniatura antes de divulgar:
- WhatsApp: mande o link para você mesmo
- Facebook/Instagram: developers.facebook.com/tools/debug (force "Scrape Again")

## Editar o conteúdo

Tudo está em `index.html`, em espanhol.

- **Telefones**: procure por `wa.me/` — são 12 ocorrências
- **Sedes**: procure por `class="loc"`
- **Tratamentos**: procure por `class="tcard"`
- **Perguntas frequentes**: procure por `class="qa"`

---

Desenvolvido por **Tape** — branding, produção audiovisual e tráfego pago.
Instagram: [@tapegrowth](https://www.instagram.com/tapegrowth/)
