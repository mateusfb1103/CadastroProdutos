# 🛒 API de Produtos - Spring Boot

Esta é uma API RESTful desenvolvida com **Spring Boot** para gerenciar produtos em um sistema simples de estoque. Ela permite realizar operações básicas de CRUD: **Criar**, **Listar**, **Atualizar** e **Excluir** produtos.

---

## 🚀 Tecnologias utilizadas

- Java 17+
- Spring Boot
- Spring Web
- Spring Data JPA
- H2 Database (banco em memória)
- Lombok (opcional)

---

## 📦 Estrutura da Entidade `Produto`

```json
{
  "id": 1,
  "nome": "Teclado Gamer",
  "preco": 199.99,
  "quantidadeEmEstoque": 10
}
```

---

## 🔧 Endpoints e Testes com Postman

### ▶️ Criar Produto

- **Método:** `POST`
- **Endpoint:** `/produtos`
- **Body (JSON):**
```json
{
  "nome": "Mouse sem fio",
  "preco": 99.90,
  "quantidadeEmEstoque": 25
}
```

---

### 📋 Listar Todos os Produtos

- **Método:** `GET`
- **Endpoint:** `/produtos`
- **Resposta esperada:**
```json
[
  {
    "id": 1,
    "nome": "Mouse sem fio",
    "preco": 99.90,
    "quantidadeEmEstoque": 25
  },
  {
    "id": 2,
    "nome": "Teclado Mecânico",
    "preco": 250.00,
    "quantidadeEmEstoque": 12
  }
]
```

---

### 🔁 Atualizar Produto

- **Método:** `PUT`
- **Endpoint:** `/produtos/{id}`
- **Exemplo:** `/produtos/1`
- **Body (JSON):**
```json
{
  "nome": "Mouse sem fio recarregável",
  "preco": 129.90,
  "quantidadeEmEstoque": 30
}
```

---

### ❌ Deletar Produto

- **Método:** `DELETE`
- **Endpoint:** `/produtos/{id}`
- **Exemplo:** `/produtos/1`

Resposta esperada: `204 No Content` (sem conteúdo, deletado com sucesso).

---

## 🧪 Acessando o banco de dados H2

- Após iniciar a aplicação, acesse:  
  `http://localhost:8080/h2-console`

- **JDBC URL:** `jdbc:h2:mem:produto-db`  
- **User:** `sa`  
- **Password:** *(deixe em branco)*

---

## 💡 Observações

- A aplicação utiliza banco de dados **em memória**, ou seja, os dados são apagados ao reiniciar o servidor.
- Ideal para testes, aprendizado ou validação rápida de lógica REST com Spring Boot.
