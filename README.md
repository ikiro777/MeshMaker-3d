MeshMaker 3D - Loja Virtual

Loja virtual de modelos 3D, filamentos, impressoras e acessórios, feita em Vue.js (com `<script setup>`), sem bibliotecas externas e sem Vue Router.

**Equipe:** [Ryan 04213577], [Brendon 4213310], [Felipe 04213566]

Funcionalidades

- Lista de produtos exibida em cards, alinhados em linhas e colunas com flexbox e responsivos.
- Clique em um produto para adicioná-lo ao carrinho.
- Rodapé com a quantidade de itens e o valor total do carrinho.
- Popup do carrinho com a lista de produtos, remoção de itens e botão de compra.
- Barra de pesquisa que filtra os produtos ao apertar Enter.

Componentes

- `App.vue`: guarda a lista de produtos, o carrinho e a busca.
- `AppHeader.vue`: cabeçalho com a logo e o slogan.
- `AppSearch.vue`: campo de busca.
- `CardProduto.vue`: card reutilizável que recebe título, valor, descrição, categoria e imagem por props.
- `FooterCarrinho.vue`: rodapé com total e botão "Ver carrinho".
- `PopupCarrinho.vue`: janela com os itens do carrinho.

Como executar

1. Baixe ou clone o repositório.
2. Instale as dependências: `npm install`
3. Rode o projeto: `npm run dev`

Prompts utilizados
| 1. Layout dos cards | "Adicione bastante CardProduto no App.vue para ter cara de loja e alinhe todos lado a lado, em linhas e colunas, com flexbox. Não altere o CSS dos componentes." |
| 2. Responsividade | "Pesquise propriedades de responsividade do CSS e aplique no layout da lista de produtos." |
| 3. Imagens | "Como colocar as imagens na pasta public e passar o nome delas pelo App.vue para o CardProduto usando props?" |
| 4. Cabeçalho | "Coloque a imagem da logo (MeshMakerLogo.svg) no AppHeader.vue e escreva uma frase de slogan." |
| 5. Carrinho | "Quando o usuário clicar em um produto, ele deve ir para o carrinho. O botão Ver carrinho deve abrir o popup listando os produtos escolhidos, com o total." |
| 6. Pesquisa | "Faça a barra de pesquisa funcionar: ao digitar um nome e apertar Enter, mostrar só os produtos que combinam." |
| 7. Correção de erro | "Os ícones ficaram gigantes e o carrinho sumiu depois de colar o código. Por que isso aconteceu?" |
| 8. Apresentação | "Faça um roteiro de 1 minuto sobre a reutilização de componentes, incluindo o CardProduto." |

Uso de IA

A IA foi usada como ferramenta de apoio. Todo o código gerado foi revisado, testado e compreendido pelo grupo.
