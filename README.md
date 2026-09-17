# Site Centro Automotivo Shekinah

Site estático em HTML, CSS e JavaScript. Para pré-visualizar, sirva a raiz com um servidor HTTP (por exemplo, `python -m http.server 8080`).

## Banner da página inicial

- A área é vertical e responsiva (proporção 4:5), preparada para artes de **1080 × 1350 pixels**, sem recorte.
- As campanhas agora são enviadas pelo **Shekinah-ADM**, na seção **Banner do site**, sem editar o HTML a cada troca.
- O site lê `GET /api/banner` na mesma API do catálogo e pré-carrega a imagem antes de substituir a arte padrão. Sem banner, com API indisponível ou imagem inválida, mantém `assets/banner-home.svg`.
- O texto alternativo vem da descrição preenchida no painel. O destino do clique continua sendo o WhatsApp da loja.
- O banner novo aparece ao abrir/atualizar a página. A versão da URL muda a cada publicação, e a API revalida a imagem por ETag.
- Publique `assets/` junto com `index.html`; a arte local é a alternativa em caso de falha.

### Dependência de publicação

A API precisa receber as rotas de banner e a migração, e o ADM precisa receber seu editor e a autenticação no servidor. Consulte os READMEs de `shekinah-api` e `Shekinah-ADM` para configurar as variáveis e coordenar a publicação. Até a API ser atualizada, esta página continua exibindo a arte padrão.

## Atendimento por WhatsApp

O banner e os CTAs levam diretamente ao WhatsApp. Os botões de orçamento dos produtos incluem o nome do produto na mensagem, sem formulário intermediário.

O número existente foi preservado: `559293022416`. Não foi validada a existência da conta no WhatsApp. Para alterar o número, atualize `WHATSAPP_NUMBER` e os links estáticos `https://wa.me/559293022416` no HTML (usados também sem JavaScript).

Os formulários de orçamento e contato e seus manipuladores JavaScript foram removidos. O catálogo, a API de produtos e os carrosséis foram mantidos.
