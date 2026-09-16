# Site Auto Center Shekinah

Site estático em HTML, CSS e JavaScript. Para pré-visualizar, sirva a raiz com um servidor HTTP (por exemplo, `python -m http.server 8080`).

## Banner da página inicial

- O espaço aceita uma arte quadrada de **1080 × 1080 pixels** e mantém proporção **1:1** em desktop e celular. A exibição se ajusta à tela; não fica fixa em 1080 pixels de largura.
- `assets/banner-home.svg` é uma arte base provisória, sem oferta ou preço, até o marketing fornecer a campanha final.
- Para trocar a arte, adicione o PNG, JPG, WebP ou SVG em `assets/` e atualize o `src` da imagem dentro de `.promotion-banner` no `index.html`.
- Mantenha `width="1080" height="1080"` e atualize o `alt` e o `aria-label` do link para refletir a campanha. O CSS usa `object-fit: contain` para não recortar a arte.
- Publique a pasta `assets/` junto com `index.html`.

## Atendimento por WhatsApp

O banner e os CTAs levam diretamente ao WhatsApp. Os botões de orçamento dos produtos incluem o nome do produto na mensagem, sem formulário intermediário.

O número existente foi preservado: `559293022416`. Não foi validada a existência da conta no WhatsApp. Para alterar o número, atualize `WHATSAPP_NUMBER` e os links estáticos `https://wa.me/559293022416` no HTML (usados também sem JavaScript).

Os formulários de orçamento e contato e seus manipuladores JavaScript foram removidos. O catálogo, a API de produtos e os carrosséis foram mantidos.
