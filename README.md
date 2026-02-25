# BuyMeCoffee

- [demo](https://www.youtube.com/shorts/TWmtCKO6BIg)
- Designed and implemented an end-to-end [checkout](https://app.bloomingrice.com/menu_order/c5b52e3b-3dee-488d-bebd-f9e216547d68) workflow, including order creation, payment initiation, idempotent processing, transactional consistency, webhook signature verification, and asynchronous payment confirmation
- Designed and implemented production and staging traffic routing architecture using Cloudflare DNS and Traefik
- Improved overall security posture by separating public and private network boundaries, implementing VPC peering, configuring firewall / Traefik rules, and applying Cloudflare anti-bot protection
- Implemented a centralized [logging](img/logscreen.png) pipeline, notification(firebase), [SliderCaptcha](https://app.bloomingrice.com/login), i18n and timezone
