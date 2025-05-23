# Fluxo de Criação de Pedido

### 1. O cliente envia um `OrderIn` contendo os produtos e quantidades.

### 2. O `OrderResource` converte para `Order` e injeta o `idAccount` do header.

### 3. O `OrderService`:

- Busca cada `ProductOut` pelo `idProduct` via `ProductController`
- Valida existência e calcula `total` de cada item
- Soma o `total` geral
- Persiste a `OrderModel`
- Persiste os `OrderItemModel` com `id_order` referenciado

### 4. Retorna um `OrderOut` com o pedido criado.

---

## Fluxo de Busca

- `findAll()`: retorna todos os pedidos
- `findById()`: exige `id-account` e verifica propriedade do pedido
