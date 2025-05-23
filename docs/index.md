# Order Service

O `order-service` é o microsserviço responsável por registrar e consultar pedidos realizados pelos usuários. Ele integra-se com o `product-service` para verificar produtos e calcular totais, e com o `account-service` para associar pedidos a usuários autenticados.

---

## Funcionalidades

- **Registrar Pedido**: Permite que um usuário faça um pedido de produtos disponíveis.
- **Consultar Pedidos**: Permite que um usuário consulte seus pedidos anteriores.
- **Consultar Detalhes do Pedido**: Permite que um usuário veja os detalhes de um pedido específico.
