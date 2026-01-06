# Study Spring Boot CRUD


## 💻 Sobre o projeto

Este é um projeto desenvolvido para fins de estudo, focando na construção de uma **API RESTful** completa utilizando o ecossistema **Spring Boot**.

O sistema consiste em um modelo de domínio complexo que aborda diversos tipos de relacionamentos entre entidades (One-to-One, One-to-Many, Many-to-Many), tratamento de exceções personalizado e operações de CRUD (Create, Read, Update, Delete).

### Principais conceitos aplicados:
- **Mapeamento Objeto-Relacional (ORM)** com JPA e Hibernate.
- **Injeção de Dependência** e Inversão de Controle.
- **Padrão de Camadas** (Resource, Service, Repository, Entity).
- **Tratamento de Exceções** globais com `@ControllerAdvice`.
- **DTOs** e serialização JSON (Jackson).

## ⚙️ Modelo de Domínio

O projeto implementa o seguinte modelo de entidades:

- **User**: Cliente que realiza pedidos.
- **Order**: Pedido realizado pelo usuário (contém status e momento).
- **Payment**: Pagamento do pedido (Relacionamento 1:1 com Order).
- **Product**: Produtos disponíveis.
- **Category**: Categorias dos produtos (Relacionamento N:N com Product).
- **OrderItem**: Item de pedido, contendo a quantidade e preço no momento da compra (Relacionamento N:N entre Order e Product com atributos extras).

## 🛠 Tecnologias Utilizadas

- **Java**
- **Spring Boot** (Web, Data JPA)
- **H2 Database** (Banco de dados em memória para testes)
- **Maven** (Gerenciamento de dependências)
- **Postman** (Para teste das requisições)

## 🚀 Como executar o projeto

### Pré-requisitos
- Java JDK 17 ou superior instalado.
- Maven instalado (ou utilizar o wrapper `./mvnw` incluso no projeto).

### Passos
1. Clone o repositório:
```bash
git clone https://github.com/seu-usuario/Study-SpringBoot-CRUD.git
```

2. Acesse a pasta do projeto:
```bash
cd Study-SpringBoot-CRUD
```

3. Execute a aplicação:
```bash
./mvnw spring-boot:run
```

A API estará acessível em: `http://localhost:8080`

## 📡 Endpoints Principais

| Método | Rota | Descrição |
|---|---|---|
| GET | `/users` | Lista todos os usuários |
| GET | `/users/{id}` | Busca usuário por ID |
| POST | `/users` | Cria um novo usuário |
| PUT | `/users/{id}` | Atualiza um usuário |
| DELETE | `/users/{id}` | Deleta um usuário |
| GET | `/products` | Lista produtos |
| GET | `/orders` | Lista pedidos |
| GET | `/categories` | Lista categorias |

---
Desenvolvido para fins de aprendizado.
