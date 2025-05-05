# 🌐 Entendendo APIs: Body, Auth, Query, Header e Docs

Este documento reúne os principais conceitos usados no consumo de APIs REST, explicando de forma clara o que são **Body**, **Auth**, **Query**, **Header** e **Docs**, com um exemplo prático no final para consolidar o aprendizado.

---

## 🔸 Body (Corpo da Requisição)

O **Body** é a parte da requisição onde enviamos **dados** para o servidor, normalmente no formato **JSON**. Ele é usado principalmente em requisições do tipo `POST`, `PUT` ou `PATCH`.

### Exemplo:
```json
{
  "nome": "Cleidson",
  "idade": 30
}
```

Esse conteúdo pode representar, por exemplo, os dados de um novo usuário a ser criado na API.

---

## 🔸 Auth (Autenticação)

A **Auth** (Autenticação) garante que apenas usuários autorizados possam acessar os recursos da API.  
As formas mais comuns são:

- **Bearer Token (JWT)**: um token de acesso enviado no header
- **Basic Auth**: usuário e senha codificados em base64
- **OAuth2**: usado em sistemas mais robustos com login externo

### Exemplo de header com token:
```
Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6...
```

---

## 🔸 Query (Parâmetros de Consulta)

**Query** são os parâmetros enviados **na URL** para fazer filtros, buscas ou paginações. São usados geralmente com `GET`.

### Exemplo:
```
GET /usuarios?idade=30&cidade=Recife
```

Aqui, os parâmetros `idade` e `cidade` estão sendo usados para filtrar usuários.

---

## 🔸 Header (Cabeçalho da Requisição)

O **Header** são informações adicionais enviadas junto com a requisição. Ele pode indicar o formato dos dados, idioma, token de autenticação, entre outros.

### Exemplo de headers:
```
Content-Type: application/json
Authorization: Bearer eyJhbGciOiJIUzI1NiIs...
```

---

## 🔸 Docs (Documentação da API)

As **Docs** são a **documentação oficial da API**, onde é possível ver os endpoints disponíveis, os métodos permitidos (`GET`, `POST`...), os parâmetros necessários e exemplos de requisições e respostas. Ferramentas como Swagger ou Postman são comumente usadas para isso.

### Exemplo:
```
https://api.exemplo.com/docs
```

---

## ✅ Exemplo Prático: API de Usuários

### 🔹 1. Buscar Usuários

**GET** `/usuarios`

#### Exemplo de requisição:
```
GET https://api.exemplo.com/usuarios?idade=30&cidade=Recife
```

#### Headers:
```http
Content-Type: application/json
Authorization: Bearer eyJhbGciOiJIUzI1NiIs...
```

#### Explicação:
- **Query**: envia os filtros de idade e cidade pela URL
- **Header**: inclui autenticação com token e tipo de conteúdo

---

### 🔹 2. Criar Novo Usuário

**POST** `/usuarios`

#### Exemplo de requisição:
```
POST https://api.exemplo.com/usuarios
```

#### Headers:
```http
Content-Type: application/json
Authorization: Bearer eyJhbGciOiJIUzI1NiIs...
```

#### Body:
```json
{
  "nome": "Cleidson Silva",
  "email": "cleidson@example.com",
  "idade": 30,
  "cidade": "Recife"
}
```

#### Explicação:
- **Body**: contém os dados do usuário a ser criado
- **Header**: autentica a requisição e define o formato como JSON

---

### 🔹 3. Documentação da API

Acesse a documentação completa em:
```
https://api.exemplo.com/docs
```

Lá você pode explorar todos os endpoints, ver exemplos de uso e testar requisições diretamente no navegador (se estiver usando Swagger, por exemplo).

---

## 📘 Conclusão

Neste guia, aprendemos os conceitos essenciais do uso de APIs:

- `Body`: dados enviados ao servidor
- `Auth`: autenticação de acesso
- `Query`: parâmetros na URL
- `Header`: metadados e informações da requisição
- `Docs`: documentação para referência

Esses elementos formam a base para trabalhar com APIs REST em qualquer linguagem ou projeto moderno.
