# Setup e Execução - Order Service

---

## Requisitos

- Java 17+
- Spring Boot
- Spring Data JPA
- OpenFeign
- PostgreSQL
- Flyway
- Lombok

---

## Dependências principais

- `spring-boot-starter-data-jpa`
- `spring-boot-starter-web`
- `spring-boot-starter-validation`
- `spring-cloud-starter-openfeign`
- `flyway-core`
- `lombok`

---

## Como compilar

```bash
mvn clean package
```

---

## Observações

- O serviço depende do header `id-account` para associar pedidos

- Integra com `product-service` para validação dos produtos e preços

- Tokens são verificados pelo `gateway-service`
