# Arquitetura

## Estrutura de Pastas

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
└── resources/
│ ├── application.yaml # Configurações de ambiente
│ └── db/migration/ # Scripts Flyway
```

---

## Integrações

- `ProductController` (Feign) → busca preço do produto
- `AccountOut` → representa o dono do pedido (id vem via header)

---
