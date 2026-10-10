# Baozi Store — API REST

Projeto da atividade prática de Desenvolvimento Web Back-End — UNINTER.

## Tecnologias

- Java 17
- Spring Boot
- Spring Web
- Spring Data JPA
- MySQL
- Maven
- Postman

## Estrutura

```text
src/main/java/br/com/baozi/store/
├── model
│   ├── Cliente.java
│   ├── Pedido.java
│   └── Produto.java
├── repository
│   ├── ClienteRepository.java
│   ├── PedidoRepository.java
│   └── ProdutoRepository.java
├── controller
│   ├── ClienteController.java
│   ├── PedidoController.java
│   └── ProdutoController.java
└── BaoziStoreApplication.java
```

## Banco

Crie o banco no MySQL:

```sql
CREATE DATABASE baozi_store;
```

Depois altere `src/main/resources/application.properties` e coloque a senha do seu MySQL.

## Executar

No terminal, dentro do projeto:

```bash
mvn spring-boot:run
```

A API ficará em:

```text
http://localhost:8080
```

## Endpoints

### Clientes

- POST `/clientes`
- GET `/clientes`
- GET `/clientes/{id}`
- DELETE `/clientes/{id}`

### Produtos

- POST `/produtos`
- GET `/produtos`
- GET `/produtos/{id}`
- DELETE `/produtos/{id}`

### Pedidos

- POST `/pedidos`
- GET `/pedidos`
- GET `/pedidos/{id}`
- DELETE `/pedidos/{id}`

## Exemplos para o Postman

### POST /clientes

```json
{
  "nome": "SEU_NOME+SEU_RU",
  "clienteDesde": "2026-09-22"
}
```

### POST /produtos

```json
{
  "nome": "Pão Baozi",
  "preco": 5.00,
  "estoque": true
}
```

### POST /pedidos

```json
{
  "clienteId": 1,
  "produtoId": 1,
  "quantidade": 3
}
```

> Antes da entrega, substitua `SEU_NOME+SEU_RU` pelo seu nome e RU e faça os prints reais do Postman. Não use prints fictícios.
