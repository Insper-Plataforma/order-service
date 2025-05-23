# Entidades e Modelos

---

## Order

Entidade de domínio de um pedido.

- `id`
- `date`
- `items: List<OrderItem>`
- `account: AccountOut`
- `total`

---

## OrderItem

Item de um pedido.

- `id`
- `product: ProductOut`
- `order: Order`
- `quantity`
- `total`

---

## OrderModel

Entidade JPA (tabela `orders`)

- `id_order`, `id_account`, `dt_date`, `db_total`

---

## OrderItemModel

Entidade JPA (tabela `order_item`)

- `id_order_item`, `id_order`, `id_product`, `int_quantity`, `nr_price_product`, `nr_total`

---

## Conversores

A conversão entre DTOs e entidades/domínio é feita por `OrderParser`.
