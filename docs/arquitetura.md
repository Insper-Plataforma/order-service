# Arquitetura

## Estrutura de pastas

```bash
src/main/java/store/order/
├── Order.java # Entidade de domínio
├── OrderModel.java # Entidade JPA
├── OrderRepository.java # Persistência da Order
├── OrderItem.java
├── OrderItemModel.java
├── OrderItemRepository.java
├── OrderService.java # Lógica de negócio
├── OrderParser.java # Conversão DTO ↔ Domínio
├── OrderResource.java # Controlador REST
├── OrderApplication.java # Classe principal
```

---

## Integrações

- `ProductController` (Feign) → busca preço do produto
- `AccountOut` → representa o dono do pedido (id vem via header)

---

## Banco de Dados

- Tabela `orders`
- Tabela `order_item`

Usa **Spring Data JPA** e **Flyway** para versionamento.
