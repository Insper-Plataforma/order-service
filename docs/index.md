# Order Service

O `order-service` é o microsserviço responsável por registrar e consultar pedidos realizados pelos usuários. Ele integra-se com o `product-service` para verificar produtos e calcular totais, e com o `account-service` para associar pedidos a usuários autenticados.

---

## Funcionalidades

- **Registrar Pedido**: Permite que um usuário faça um pedido de produtos disponíveis.
- **Consultar Pedidos**: Permite que um usuário consulte seus pedidos anteriores.
- **Consultar Detalhes do Pedido**: Permite que um usuário veja os detalhes de um pedido específico.

---

## Integração com Jenkins

Este projeto conta com um arquivo Jenkinsfile (na raiz do repositório) que define uma pipeline de integração contínua para compilar automaticamente o módulo sempre que houver alterações no repositório.

### Para que serve?

- Compilação automatizada: toda alteração no repositório dispara o build do Maven, detectando problemas de compilação antes do merge.

- Imagens Docker consistentes: gera e publica automaticamente imagens multiplataforma, facilitando o deploy em diferentes ambientes (x86_64 e ARM).

- Segurança das credenciais: utiliza credenciais armazenadas no Jenkins (identificador dockerhub-credential), evitando exposição de senhas no código.

Dessa forma, a integração com Jenkins garante que o order-service esteja sempre compilando e empacotado corretamente, com uma imagem Docker pronta para ser implantada nos clusters de produção ou QA.
