# Site — Joaquim Santini

Landing page estática (HTML + CSS). Sem build, sem dependências para instalar.

## Arquivos que compõem o site

Estes precisam ir para o repositório:

- `index.html` — a página
- `styles.css` — todo o estilo (Tailwind já compilado; **não depende mais de internet/CDN**)
- `.nojekyll` — diz ao GitHub Pages para servir os arquivos sem processar com Jekyll
- `joaquim-santini-perfil.jpg` — foto do perfil
- `insead-novo-trim.png`, `unicamp-trim.png` — logos da seção "Formação"
- `Times_Brasil_CNBC_logo.svg.png`, `75f26bc9-...png` — logos dos botões de colunas (Times / Exame)
- `Logos - Clientes/norm/` — os 17 logos de clientes usados no carrossel

> As imagens das colunas (thumbnails) e as fontes (Google Fonts) são carregadas da internet,
> então o site precisa de conexão para exibi-las — o resto funciona offline.

> Os demais arquivos soltos na pasta (versões antigas de logos, `.webp`, `nestle-clean.png` etc.)
> **não são usados** e podem ser apagados sem afetar o site.

## Publicar no GitHub Pages

1. Crie um repositório no GitHub (ex.: `site-joaquim`).
2. Suba **todo o conteúdo desta pasta** para o repositório (incluindo a pasta `Logos - Clientes`).
   - Pelo site do GitHub: botão **Add file → Upload files**, arraste tudo e confirme (Commit).
3. No repositório, vá em **Settings → Pages**.
4. Em **Build and deployment → Source**, escolha **Deploy from a branch**.
5. Em **Branch**, selecione `main` e a pasta `/ (root)`. Salve.
6. Aguarde ~1 minuto. O endereço aparece no topo da página Pages
   (algo como `https://SEU-USUARIO.github.io/site-joaquim/`).

## Domínio personalizado (.com.br)

1. Registre/possua o domínio (ex.: no Registro.br).
2. No GitHub: **Settings → Pages → Custom domain**, digite o domínio (ex.: `www.joaquimsantini.com.br`) e salve.
   Isso cria um arquivo `CNAME` no repositório automaticamente.
3. No painel de DNS do domínio:
   - **www** → registro `CNAME` apontando para `SEU-USUARIO.github.io`
   - **raiz** (`joaquimsantini.com.br`) → registros `A` para os IPs do GitHub Pages:
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
4. De volta em Settings → Pages, marque **Enforce HTTPS** (pode levar alguns minutos/horas
   até o certificado ser emitido).

## Editar o conteúdo depois

Tudo está em `index.html` (textos, links, logos). Cores, fontes e espaçamentos estão em `styles.css`.
