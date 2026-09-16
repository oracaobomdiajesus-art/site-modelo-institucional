# Site Modelo Institucional

Template simples de site institucional (estilo "link na bio"), feito em [Hugo](https://gohugo.io/), pronto para publicar grátis no Cloudflare Pages e editar pelo [Pages CMS](https://pagescms.org/).

Sem catálogo, carrinho ou painel administrativo — só o essencial para um pequeno negócio ter uma página profissional: foto, biografia, redes sociais, links, vídeo e galeria de fotos.

## O que dá para editar pelo CMS

- Nome do negócio, foto de perfil e biografia
- Links de Instagram, WhatsApp e avaliação no Google
- Lista de links personalizados (ex: cardápio no PDF, outro site, localização no mapa)
- Vídeo do YouTube em destaque
- Galeria de fotos
- Tema de cor (marrom, verde, rosa ou azul)
- Imagem de fundo do site, com opção de ligar/desligar e ajustar a opacidade

## Como usar este template para um novo cliente

1. Crie um novo repositório no GitHub a partir deste (use o botão "Use this template" ou clone e troque o remote).
2. No Cloudflare Pages, crie um novo projeto apontando para o repositório novo. Build command: `hugo --minify`. Diretório de saída: `public`.
3. Configure o [Pages CMS](https://pagescms.org/) apontando para o novo repositório — o arquivo `.pages.yml` já define todos os campos editáveis.
4. Edite `content/_index.md` e a pasta `content/links/` com as informações reais do cliente.
5. Troque `static/img/perfil.svg` pela foto real do negócio (pode ser feito direto pelo CMS, no campo "Foto de perfil").

## Estrutura

```
content/
  _index.md        → dados do perfil (nome, bio, redes sociais, tema, fundo)
  links/           → cada arquivo é um link exibido na página
  galeria/         → cada arquivo é uma foto da galeria
layouts/
  index.html       → template da página única
  partials/
    theme-style.html → aplica tema de cor e imagem de fundo
    analytics.html   → espaço opcional para script de estatísticas
static/
  css/style.css    → estilos do site
  img/             → imagens (perfil, fundo, galeria)
```

## Desenvolvimento local

Requer [Hugo](https://gohugo.io/installation/) instalado.

```
hugo server -D
```
