# Checkpoint 2 - API REST de Pedidos

Disciplina: Arquitetura SOA e Web Services

## Integrantes

- Fabricio Bettarello RM 554638
- Enzo Miletta RM 98677

## Descrição

API REST desenvolvida com Spring Boot para cadastrar e gerenciar pedidos de clientes.

## Tecnologias

- Java 21
- Spring Boot
- Spring Web
- Spring Data JPA
- Bean Validation
- Lombok
- H2 Database
- Maven

## Como executar

```bash
mvn spring-boot:run
```

A aplicação será executada em:

```text
http://localhost:8085
```

Console H2:

```text
http://localhost:8085/h2-console
```

Configuração do H2:

```text
JDBC URL: jdbc:h2:mem:checkpoint2db
User Name: sa
Password: password
```

## Endpoints

### Criar pedido

```http
POST /pedidos
Content-Type: application/json
```

```json
{
  "clienteNome": "Fabricio Bettarello",
  "valorTotal": 150.75
}
```

### Listar pedidos

```http
GET /pedidos
```

### Buscar pedido por ID

```http
GET /pedidos/1
```

### Atualizar pedido

```http
PUT /pedidos/1
Content-Type: application/json
```

```json
{
  "clienteNome": "Enzo Miletta",
  "valorTotal": 250.00
}
```

### Deletar pedido

```http
DELETE /pedidos/1
```
