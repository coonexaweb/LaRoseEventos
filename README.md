# La Rose Decorações

Site institucional da **La Rose Decorações**, empresa de decoração de casamentos, festas de 15 anos e eventos sociais em São Luís de Montes Belos (GO). O objetivo da página é apresentar o portfólio e levar o visitante a pedir um orçamento pelo WhatsApp.

**Site publicado:** <https://laroseeventos.netlify.app/>

## Funcionalidades

- Página única com as seções de apresentação, sobre, serviços, portfólio, perguntas frequentes e localização
- Galeria com filtros por categoria, botão "Ver mais eventos" e ampliação das fotos em lightbox
- Menu lateral no celular e cabeçalho que se esconde ao rolar a página para baixo
- Botões de WhatsApp com mensagem pronta, incluindo uma barra fixa no celular
- Animações de entrada dos elementos ao rolar a página
- Imagens em WebP com miniaturas para a galeria e carregamento sob demanda

## Tecnologias

O site é feito em HTML, CSS e JavaScript puros, sem framework, dependências ou etapa de build. Dois recursos externos são carregados por CDN:

- [Google Fonts](https://fonts.google.com/): Antonio, Cormorant Garamond e Plus Jakarta Sans
- [Font Awesome 6.4](https://fontawesome.com/): ícones

## Estrutura

```text
.
├── index.html                    # Conteúdo, estilos e scripts do site
├── img/                          # Fotos dos eventos, logo e imagem principal
│   └── thumbs/                   # Miniaturas WebP da galeria
├── sitemap.xml                   # Mapa do site para buscadores
├── robots.txt                    # Regras de rastreamento, incluindo bots de IA
├── llms.txt                      # Resumo da empresa para assistentes de IA
└── google32436fa39b90396c.html   # Verificação do Google Search Console
```

## Como rodar localmente

Abra o `index.html` no navegador ou sirva a pasta com um servidor local:

```bash
python -m http.server 8000
```

Depois acesse <http://localhost:8000>.

## Como editar

Tudo fica em `index.html`:

| O que alterar | Onde |
| --- | --- |
| Cores e fontes | Variáveis CSS em `:root`, no início do bloco `<style>` |
| Textos e serviços | Seções `#sobre`, `#servicos` e `#perguntas` |
| Fotos da galeria | Itens `.portfolio-item` da seção `#portfolio` |
| Comportamento da página | Bloco `<script>` no final do arquivo |

**Ao adicionar uma foto:** salve a versão completa em `img/` e a miniatura em `img/thumbs/`, ambas em WebP. Use um nome descritivo e preencha o `alt`. Para aparecer em um filtro, o item precisa ter a classe correspondente ao `data-filter` do botão.

**Ao mudar dados da empresa** (telefone, endereço, serviços ou domínio), atualize também o JSON-LD no `<head>` do `index.html`, o `llms.txt` e, se o domínio mudar, a tag canônica, o `robots.txt` e o `sitemap.xml`.

## SEO

O site já inclui metadados de busca, dados estruturados JSON-LD, sitemap, `robots.txt` com bots de IA liberados, `llms.txt` e verificação do Search Console.

O Google Analytics ainda **não está ativo**. Para ativá-lo, localize o trecho comentado no `<head>` do `index.html`, substitua `G-XXXXXXXXXX` pelo ID da propriedade GA4 e remova os marcadores de comentário.

## Publicação

O site está hospedado no [Netlify](https://www.netlify.com/). Por não ter etapa de build, basta publicar a raiz do repositório, sem comando de build.

## Contato da empresa

- **WhatsApp:** [(64) 9 9287-2934](https://wa.me/5564992872934)
- **Instagram:** [@larosedecoracoes](https://www.instagram.com/larosedecoracoes/)
- **Endereço:** Av. Hermógenes Coelho, 1731, Vila Boa, São Luís de Montes Belos - GO, 76100-000
