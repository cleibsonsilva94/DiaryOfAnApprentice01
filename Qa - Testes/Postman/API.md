## O que é uma API?

API (Application Programming Interface) é uma **interface de comunicação entre dois sistemas**. Ela permite que diferentes softwares "conversem" entre si, trocando informações e comandos.

Existem **APIs públicas** e **APIs privadas**:
- **Públicas**: podem ser acessadas por qualquer pessoa (com ou sem autenticação).
- **Privadas**: geralmente são de uso interno de uma empresa, acessadas apenas por funcionários ou sistemas autorizados.

---

## O que é o Postman?

O **Postman** é uma ferramenta muito utilizada para:
- Criar e testar APIs.
- Verificar se uma API está funcionando corretamente.
- Simular requisições HTTP e visualizar respostas.

Com ele, é possível testar uma API mesmo antes dela estar conectada a um front-end, por exemplo.

---

## Requisições HTTP

A comunicação entre cliente e servidor geralmente ocorre por meio de requisições **HTTP**, com dois principais elementos:

- **HTTP Request**: a requisição enviada do cliente para o servidor.
- **HTTP Response**: a resposta que o servidor devolve para o cliente.

---

## Linguagens de Programação

APIs são criadas com linguagens de programação como JavaScript, Java, Python, entre outras.  
Praticamente todas as linguagens modernas conseguem **criar APIs e também fazer requisições** para elas.

---

## Tipos de Requisição (Métodos HTTP)

Os principais métodos HTTP utilizados em APIs são:

- **GET** – Usado para **consultar/obter dados**.
- **POST** – Usado para **enviar dados/criar algo novo**.
- **PUT** – Usado para **atualizar totalmente** um recurso.
- **PATCH** – Usado para **atualizar parcialmente** um recurso.
- **DELETE** – Usado para **excluir** um recurso.
- **HEAD** – Retorna apenas os **cabeçalhos** da resposta (sem o corpo).
- **OPTIONS** – Retorna os **métodos permitidos** por um recurso.

---

## Parâmetros de Requisição

Muitas APIs aceitam **parâmetros** para filtrar ou modificar o comportamento da resposta.  
Eles são geralmente enviados como pares `Key: Value` (Chave e Valor).

### Tipos comuns de parâmetros:
- **Query Parameters**: enviados na URL após `?`.  
  Exemplo: `?nome=joao&idade=30`  
  Usado principalmente para filtros ou paginações.

- **Path Variables** (ou parâmetros de rota): fazem parte da URL.  
  Exemplo: `/usuarios/123` – O `123` é o ID do usuário.  
  São usados para acessar um recurso específico.

---

## Autenticação com Token

Algumas APIs exigem um **Token de autenticação** para liberar o acesso.  
Esse token funciona como uma **senha temporária**, e geralmente é informado nos **headers** da requisição.  
A forma de obter e usar o token é explicada na **documentação da API**.

---

## Exemplo de API pública

[https://github.com/escoladedevs/postman-em-1-hora](https://github.com/escoladedevs/postman-em-1-hora)
