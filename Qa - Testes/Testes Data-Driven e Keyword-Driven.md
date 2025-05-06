# Testes Data-Driven e Keyword-Driven

Neste documento, explicamos as abordagens **Data-Driven** e **Keyword-Driven** para testes automatizados, especialmente no contexto de BDD com Gherkin. Ambas as técnicas visam tornar os testes mais organizados, reutilizáveis e de fácil manutenção.

---

## 🧪 O que é um teste Data-Driven?

Testes **Data-Driven** (dirigidos por dados) consistem em um único cenário de teste executado diversas vezes com diferentes conjuntos de dados. Cada linha da tabela representa uma variação de dados usada pelo mesmo caso de teste.

### ✅ Vantagens:
- Redução de duplicação de código.
- Facilidade na adição de novos cenários com apenas uma nova linha de dados.
- Melhora na manutenção dos testes.

### 📘 Exemplo com Gherkin:

```gherkin
Funcionalidade: Login do usuário

  Esquema do Cenário: Autenticação com diferentes credenciais
    Dado que o usuário acessa a página de login
    Quando o usuário preenche o campo "usuário" com "<usuario>"
    E preenche o campo "senha" com "<senha>"
    E clica no botão de login
    Então o sistema deve exibir a mensagem "<mensagem>"

    Exemplos:
      | usuario     | senha       | mensagem                        |
      | admin       | 123456      | Login realizado com sucesso     |
      | convidado   | abc123      | Login realizado com sucesso     |
      | admin       | senhaerrada | Usuário ou senha incorretos     |
```

---

## 🧩 O que é um teste Keyword-Driven?

Testes **Keyword-Driven** (dirigidos por palavras-chave) usam comandos abstratos (palavras-chave) que representam ações a serem executadas. As palavras-chave podem estar mapeadas para funções ou métodos definidos em código, tornando o teste mais legível e reutilizável.

Essa abordagem é muito comum em frameworks como **Robot Framework** ou em arquiteturas personalizadas.

### ✅ Vantagens:
- Separação clara entre lógica do teste e dados.
- Aumento da legibilidade.
- Possibilidade de reutilização das palavras-chave em diferentes testes.

### 📘 Exemplo com Robot Framework:

```robot
*** Settings ***
Library    SeleniumLibrary

*** Variables ***
${URL}     https://minhaaplicacao.com/login

*** Test Cases ***
Login Válido com Admin
    Acessar Página de Login
    Preencher Campo de Texto    id=usuario    admin
    Preencher Campo de Texto    id=senha      123456
    Clicar no Botão             id=login
    Verificar Mensagem na Tela  Login realizado com sucesso

Login Inválido com Senha Errada
    Acessar Página de Login
    Preencher Campo de Texto    id=usuario    admin
    Preencher Campo de Texto    id=senha      senhaerrada
    Clicar no Botão             id=login
    Verificar Mensagem na Tela  Usuário ou senha incorretos

*** Keywords ***
Acessar Página de Login
    Open Browser    ${URL}    chrome
    Maximize Browser Window

Preencher Campo de Texto
    [Arguments]    ${elemento}    ${valor}
    Input Text     ${elemento}    ${valor}

Clicar no Botão
    [Arguments]    ${elemento}
    Click Button   ${elemento}

Verificar Mensagem na Tela
    [Arguments]    ${mensagem}
    Page Should Contain    ${mensagem}
```

---

## 🔗 Conclusão

- A abordagem **Data-Driven** é excelente para quando você quer **repetir o mesmo teste com dados diferentes**.
- A abordagem **Keyword-Driven** é ideal para **separar lógica de teste e facilitar a leitura** por não programadores.
- Ambas podem ser combinadas para alcançar testes mais robustos, claros e fáceis de manter.
