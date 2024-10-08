<h1 align="center">Java Backend Spring (Desafio PicPay)</h1>

<p align="center">
  <img alt="GitHub language count" src="https://img.shields.io/github/languages/count/williamjayjay/java-backend-spring-picpay">

  <img alt="GitHub Top Language" src="https://img.shields.io/github/languages/top/williamjayjay/java-backend-spring-picpay" />

  <img alt="Repository size" src="https://img.shields.io/github/repo-size/williamjayjay/java-backend-spring-picpay">
  
  <a href="https://github.com/williamjayjay/Github-Blog/commits/master">
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/williamjayjay/java-backend-spring-picpay">
  </a>
    
   <a href="https://github.com/williamjayjay/java-backend-spring-picpay/stargazers">
    <img alt="Stargazers" src="https://img.shields.io/github/stars/williamjayjay/java-backend-spring-picpay?style=social">
  </a>
</p>

<p align="center"><p align="center">
Nesse projeto é possível depositar e realizar transferências de dinheiro entre usuários. Temos 2 tipos de usuários, os comuns e lojistas, ambos têm carteira com dinheiro e realizam transferências entre eles.</p>

<p align="center">
<img alt="api java + spring" src=".github/assets/cover.png" />
</p>

## VideoCase:
https://github.com/user-attachments/assets/b5d190ea-db3a-4f5f-8ebd-836aeba3de8a


## Backend Java:

**API:** Desenvolvi esse projeto para reforçar meu conhecimento com Java e Spring.
O Spring Web foi uma das depêndencias que escolhi para desenvolver essa API Restful.
O Spring Data JPA foi escolhido para termos a persistência dos nosso dados.
Ja o Lombok foi escolhido para gerar os getters,setters,constructors de forma mais simples .
O Spring Boot DevTools para ajudar no desenvolvimento.
Ja o H2 Database por mais que seja um banco de dados em memória, ele nos auxilia pela agilidade do desenvolvimento e no foco concentrado na regra de negócio da aplicação. 

## 🚀 Tecnologias

Principais tecnologias que utilizei para desenvolver esta aplicação

- [Maven]
- [Spring Web](https://start.spring.io/)
- [Spring Data JPA](https://start.spring.io/)
- [Lombok](https://start.spring.io/)
- [Spring Boot DevTools](https://start.spring.io/)
- [H2 Database](https://start.spring.io/)


## Guia de inicialização

Para instalar e configurar uma cópia local, siga estas etapas simples:

### Prerequisitos

Para garantir o funcionamento adequado da nossa aplicação, verifique abaixo:

1. **Clone o repositório**:
  ```sh
  git clone https://github.com/williamjayjay/java-backend-spring-picpay
  ```

2. **Instale os módulos com o maven:**

3. **A API estará acessível em:**
  ```sh
  http://localhost:8080
  ```

## Roadmap

- [x] Conseguir criar um usuário.

- [x] Não permitir usuários duplicados.

- [x] Permitir criar usuários COMMON e MERCHANT.

- [x] Não permitir que o usuário MERCHANT realize transferências.

- [x] Tratar os erros exception para uma forma amigável como response.


## API Endpoints
A api provê os seguintes endpoints:

**GET USERS**
```markdown
GET /users - Recupera uma lista de todos os usuários.
```
```json
[
    {
        "id": 1,
        "firstName": "William",
        "lastName": "Silva",
        "document": "123456787",
        "email": "william@mail.com",
        "password": "senha123",
        "balance": 10.00,
        "userType": "MERCHANT"
    },
    {
        "id": 4,
        "firstName": "Jorge",
        "lastName": "Silva",
        "document": "12342223",
        "email": "jorge@mail.com",
        "password": "senha321",
        "balance": 50.00,
        "userType": "COMMON"
    }
]
```

**POST USERS**
```markdown
POST /users - Registrar um novo usuário na aplicação
```
```json
{
    "firstName": "William",
    "lastName": "Silva",
    "password": "senha123",
    "document": "123456787",
    "email": "william@mail.com",
    "userType": "COMMON",
    "balance": 10
}
```

**POST TRANSACTIONS**
```markdown
POST /transactions - Registra uma nova transação entre os usuários (COMMON para COMMON ou COMMON para MERCHANT)
```

```json

{
  "senderId": 4,
  "receiverId": 1,
  "value": 10
}
```
