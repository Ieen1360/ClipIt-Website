# Site oficial do ClipIt

Landing page estática do ClipIt, em português brasileiro. HTML, CSS e JavaScript puros, sem dependências,
sem backend e sem chamadas a outros domínios. Funciona em qualquer caminho, inclusive em subpastas como
`usuario.github.io/repositorio/`, porque todos os caminhos são relativos.

## Estrutura

```
ClipIt-Official-Website/
├── index.html              página principal
├── css/styles.css          estilos (tema escuro, responsivo)
├── js/main.js              menu no celular e animação de entrada
├── assets/                 logotipo, favicon e ilustração em SVG
├── .nojekyll               impede o processamento Jekyll no GitHub Pages
└── pages-workflow.yml      workflow opcional de publicação via GitHub Actions
```

## Executar localmente

Dentro da pasta do site:

```bash
python3 -m http.server 8000
```

Abra `http://localhost:8000`. Também é possível abrir o `index.html` diretamente no navegador.

## Publicar no GitHub Pages

O site pode ser publicado de duas formas.

**Opção 1: pasta `website/` do repositório (recomendada)**

1. Copie o conteúdo desta pasta para uma pasta `website/` na raiz do repositório.
2. Mova `pages-workflow.yml` para `.github/workflows/pages.yml`.
3. Em **Settings → Pages**, escolha **Source: GitHub Actions**.
4. Envie as alterações para o branch `main`. O workflow publica o site.

Se o branch padrão não for `main`, ou se a pasta tiver outro nome, ajuste os campos `branches` e `path`
no workflow.

**Opção 2: branch e pasta `/docs`**

1. Copie o conteúdo desta pasta para `docs/` na raiz do repositório.
2. Em **Settings → Pages**, escolha **Deploy from a branch**, o branch desejado e a pasta `/docs`.

Na opção 2, o arquivo `docs/historico-de-desenvolvimento.md` deste repositório também seria publicado. Se
isso não for desejado, use a opção 1.

## Antes de divulgar

- O site não tem URL canônica nem imagem de compartilhamento (`og:image`), porque o endereço público ainda não
  existe. Quando existir, acrescente `<link rel="canonical">` e `og:url`.
- O site não contém link de repositório. O link de download aponta para o APK de teste no MediaFire; troque
  o endereço se o arquivo for substituído.
