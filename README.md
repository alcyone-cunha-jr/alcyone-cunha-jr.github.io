# Portfólio Profissional – Alcyone Cunha Junior

Site estático (apenas HTML + CSS + JS inline) publicável diretamente no GitHub Pages.

## Conteúdo

- `index.html` — Apresentação com 3 trilhas (Juízes, Advogados, Empresas/Condomínios)
- `curriculo.html` — Currículo completo
- `README.md` — este arquivo

Os dois HTMLs são autônomos: não dependem de imagens externas (a foto está embutida em base64 no currículo) nem de qualquer build. Só precisam de conexão para carregar as fontes do Google Fonts.

## Como publicar no GitHub Pages

1. Crie um repositório novo no GitHub (ex.: `portfolio` ou `alcyone-cunha`).
2. Faça upload dos três arquivos (`index.html`, `curriculo.html`, `README.md`) na raiz do repositório — ou clone localmente, copie e dê push:
   ```bash
   git clone https://github.com/<seu-usuario>/<seu-repo>.git
   cp index.html curriculo.html README.md <seu-repo>/
   cd <seu-repo>
   git add .
   git commit -m "Publica portfólio e currículo"
   git push
   ```
3. No repositório, vá em **Settings → Pages**.
4. Em **Source**, selecione **Deploy from a branch**, branch `main` (ou `master`), pasta `/ (root)`. Salve.
5. Em alguns minutos o site fica disponível em:
   `https://<seu-usuario>.github.io/<seu-repo>/`

## Domínio personalizado (opcional)

Se quiser usar um domínio próprio (ex.: `cunha.eng.br`):
1. Adicione um arquivo `CNAME` na raiz contendo apenas o domínio.
2. Configure os DNS do domínio apontando para o GitHub Pages (registros A para os IPs documentados em `https://docs.github.com/pages` ou um CNAME para `<seu-usuario>.github.io`).

## Estrutura de navegação

- A barra superior (**ACJ**) liga as duas páginas: "← Apresentação" e "Currículo →".
- Os três botões da capa (Juízes / Advogados / Empresas) abrem trilhas de conteúdo na própria página `index.html`.
- Os links das trilhas (deep-link) funcionam por `#hash`:
  - `index.html#juiz`
  - `index.html#advogado`
  - `index.html#empresa`

## Atualização de contato

Telefone, e-mail e WhatsApp aparecem no rodapé da capa e nos CTAs das três trilhas. Para atualizar, faça find/replace de:
- `+55 21 98801-0557`
- `alcyone.cunha.junior@hotmail.com`
- `5521988010557` (formato dos links `wa.me`)
