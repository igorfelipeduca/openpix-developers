---
id: faq-cloudflare
title: CloudFlare
tags:
- faq
- cloudflare
---
import Embed from 'react-embed';

## Não estou conseguindo cadastrar meu Webhook

- Crie uma regra de excessão de firewall
- Se a regra não funcionar, desative a proteção antibots

## Regra de excessão de firewall

<Embed url='https://youtu.be/q-XhQbGziGk' />

Exemplo de regra de excessão de firewall:

### Acesse `Security > WAF`

![CloudFlare Regra de firewall](/img/cloudflare/cloudflare_regra_firewall.png)

## Desabilitar Cloudflare Bot

### Acesse `Security > Bots`

A solução de antibot da Cloudflare pode bloquear os requests de Webhooks.

Para desabilitar a proteção antibot siga os passos abaixo:

1. clique no seu dominio
2. Na Sidebar lateral procure por Security e clique, em seguida escolha o item Bots no menu:
![cloudflare sidebar security example](./__assets__/cloudflare-sidebar.png)

3. Em Bots clique em `Configure Super Bot Fight Mode`
![cloudflare bots home](./__assets__/cloudflare-bots.png)

4. Procure por Definitely Automated e Verified Bots, atualize os valores de ambos para Allow
![cloudflare bots options](./__assets__/cloudflare-bots-options.png)

5. Realize um teste e veja se esta funcionando normalmente
[https://www.cloudflare.com/products/bot-management/](https://www.cloudflare.com/products/bot-management/)
