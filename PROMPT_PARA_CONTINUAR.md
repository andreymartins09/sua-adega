# Prompt para continuar o projeto Sua Adega

Você está continuando o protótipo web **Sua Adega**, um site de pedidos para uma adega popular, com batidas, cervejas, gelo e combos. O usuário quer que você continue o trabalho existente, preservando os recursos e o estilo já implementados.

## Onde estão os arquivos

- `outputs/index.html`: loja do cliente.
- `outputs/admin.html`: painel ADM.
- `outputs/MANUAL_DO_PROJETO.md`: manual de uso e limitações.

Leia primeiro o manual e inspecione os dois HTMLs antes de alterar qualquer coisa. O projeto é estático e usa CSS e JavaScript embutidos nos HTMLs; várias funções estão minificadas em linhas longas. Faça mudanças pontuais para não apagar recursos existentes.

## Estilo e idioma

- Responda em português brasileiro.
- Mantenha a identidade preta, amarela e creme, com linguagem simples e popular.
- Faça a interface funcionar em celular e desktop.
- Prefira controles fáceis para pequenos empreendedores e clientes.

## Recursos que já existem

- Loja cliente com categorias, produtos em destaque, busca, sacola e detalhes dos produtos.
- Fotos de produtos em cartões verticais; algumas fotos da demonstração são remotas e estão marcadas como ilustrativas.
- Perfis do cliente e consulta/acompanhamento de pedidos.
- Checkout com entrega por motoboy ou retirada no local, e envio do pedido ao WhatsApp.
- Acompanhamento de etapas do pedido; o ADM pode avançar, cancelar e concluir. Há cancelamento automático após três horas para pedidos não concluídos.
- Painel ADM com visão geral, ranking de vendas por quantidade, janelas de faturamento, filtros de período, lista de pedidos e catálogo de produtos.
- Cadastro/edição de produtos, filtros por categoria, envio de fotos e edição visual de tamanhos e preços em ml.
- Configurações para textos da loja, imagens de banner e fundo, horário, WhatsApp e status aberto/fechado.
- Cupons: o ADM gera códigos aleatórios e configura faixas de quantidade mínima e desconto percentual. O cliente informa o cupom no carrinho; o sistema aplica a maior faixa alcançada e inclui o desconto no resumo do WhatsApp e do pedido ADM.

## Acesso demonstrativo do painel

- Login: `admin`
- Senha: `adega123`

Não apresente esse acesso como seguro para produção. O protótipo não possui backend.

## Limitações técnicas que precisam ser lembradas

- Dados ficam no `localStorage` do navegador. Não há sincronização confiável entre dispositivos, usuários ou navegadores.
- A autenticação do ADM é apenas demonstrativa e roda no cliente.
- Pagamentos são combinados pelo WhatsApp; não há processamento real de cartão ou Pix.
- Status de entrega é uma animação/etapas de pedido, sem GPS em tempo real.
- Imagens remotas dependem de internet.

Se o usuário pedir produção real, explique e planeje a migração para backend e banco de dados. Não apague dados ou recursos sem necessidade. Preserve arquivos existentes, atualize o manual se mudar fluxos importantes e abra as páginas modificadas para revisão visual quando possível.

## Pedido atual concluído

Foi solicitado criar cupons aleatórios pelo ADM, com descontos configuráveis que variam por quantidade de itens. O código atual permite várias faixas por cupom, por exemplo 1 item = 5%, 3 itens = 10%, 6 itens = 15%. O código é gerado como `ADEGA-XXXXXXX`. O desconto maior é escolhido quando a quantidade alcança uma faixa. O usuário pediu também guardar o projeto com manual e prompt para continuidade.

Para uma próxima tarefa, continue a partir do pedido mais recente do usuário; não refaça a loja do zero.

