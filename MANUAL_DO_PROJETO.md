# Manual de uso — Sua Adega

## Arquivos do projeto

- `index.html`: loja que o cliente acessa.
- `admin.html`: painel de administração da adega.
- `PROMPT_PARA_CONTINUAR.md`: contexto pronto para outra IA continuar o projeto.

Abra `index.html` para ver a loja. Para o painel, abra `admin.html`.

## Acesso ao ADM

No protótipo atual, entre com:

- Login: `admin`
- Senha: `adega123`

Essas credenciais são apenas demonstrativas. Não use este acesso em uma loja publicada sem implementar autenticação de servidor.

## Produtos e preços

1. No ADM, abra **Produtos e preços**.
2. Cadastre o nome, categoria, preço inicial e, se quiser, descrição e foto.
3. Na lista, filtre por categoria para encontrar um item.
4. Ajuste preço ou categoria direto no cartão do produto.
5. Use **Tamanhos e preços** para marcar os volumes disponíveis, informar cada preço ou adicionar um tamanho personalizado.
6. Use as ações do cartão para trocar foto, pausar/reativar a venda ou excluir.

Fotos marcadas como ilustrativas servem apenas para visualizar o layout. Substitua-as por fotos reais da loja.

## Cupons por quantidade

1. No ADM, abra **Cupons**.
2. Em **Criar cupom**, configure uma ou mais faixas com quantidade mínima de itens e porcentagem.
3. Use **Adicionar outra faixa** para definir descontos progressivos. Exemplo: 1 item = 5%, 3 itens = 10%, 6 itens = 15%.
4. Clique em **Gerar código do cupom**. O sistema cria um código aleatório.
5. Na lista, você pode pausar/reativar ou excluir cupons.
6. O cliente digita o código na sacola. O sistema aplica a maior faixa alcançada pela quantidade de itens e mostra subtotal, desconto e total.
7. O código e o desconto são incluídos no pedido e na mensagem enviada ao WhatsApp da loja.

O protótipo permite uma faixa de desconto por cupom por pedido. Não há limite de uso ou validade configurável ainda.

## Loja e funcionamento

Em **Configurações da loja**, edite os dados da adega, horários, WhatsApp, informação de entrega, textos do banner, da bebida personalizada e do rodapé. O status **Aberto para pedidos / Fechado no momento** aparece no site do cliente. Também é possível enviar uma foto em destaque para o banner e uma imagem de fundo geral.

## Pedido do cliente

O cliente escolhe produtos e tamanhos, pode aplicar um cupom e seleciona **Entrega por motoboy** ou **Retirar no local** no checkout. Para entrega, endereço e bairro são obrigatórios. O pedido é salvo no protótipo e a confirmação é encaminhada ao WhatsApp da loja com os itens, valores, forma de recebimento e cupom.

No ADM, a aba **Pedidos** mostra os pedidos e a forma de recebimento. A equipe atualiza as etapas, cancela pedidos ou conclui a entrega. O acompanhamento é uma simulação de status, não rastreio GPS em tempo real.

## Visão geral

O painel mostra ranking de produtos por quantidade vendida e janelas de faturamento com base nos pedidos finalizados.

## Limitações importantes do protótipo

- O projeto é composto por páginas HTML estáticas e usa `localStorage` do navegador.
- Produtos, pedidos, configurações e cupons não têm banco de dados ou sincronização entre dispositivos.
- O checkout não processa Pix ou cartão. Ele prepara uma mensagem para confirmação pelo WhatsApp.
- Login e senha do ADM ficam no código do navegador e não são segurança real.
- As imagens de exemplo são carregadas da internet; substitua-as por fotos próprias antes de usar comercialmente.
- Para operar de verdade, será necessário publicar o site e implementar backend, autenticação, persistência central, regras de preço/cupons no servidor e integração de pagamento adequada.

