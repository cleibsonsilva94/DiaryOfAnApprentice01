# 🧠 Conceitos Fundamentais: Jira + Xray para Testes de Software

Este guia traz os principais termos e conceitos utilizados em projetos de testes de software utilizando **Jira** e **Xray**. Ideal para quem está começando ou precisa revisar fundamentos importantes do dia a dia de QA.

---

## 📌 Conceitos do Jira

### 📌 Issue
Unidade de trabalho no Jira. Pode ser:
- **Bug** (erro ou defeito)
- **Task** (tarefa)
- **Story** (história de usuário)
- **Epic** (épico)

---

### 📌 Epic (Épico)
Representa uma **grande funcionalidade ou entrega**, que será dividida em várias *Stories*.

**Exemplo:**  
> Epic: “Módulo de Agendamento”  
> Stories: “Criar formulário de agendamento”, “Implementar calendário”, etc.

---

### 📌 Sprint
Ciclo de trabalho com tempo fixo (ex: 2 semanas) onde o time desenvolve e entrega funcionalidades.

**Exemplo:**  
> Sprint 5 (01/03 a 15/03): entrega da funcionalidade de login, testes de cadastro e correções de bugs da sprint anterior.

---

### 📌 Label (Etiqueta)
Marcação livre que você pode adicionar às issues para facilitar a filtragem.

**Exemplo de labels:**  
- `prioridade-alta`
- `regressao`
- `testes-xray`

---

### 📌 Component (Componente)
Área técnica ou módulo do sistema. São definidos por administradores e ajudam a categorizar onde a issue atua.

**Exemplos de Components:**
- `Frontend`
- `Backend`
- `Notificacoes`
- `Testes Automatizados`

---

### 📌 Release (Versão)
Versão do sistema entregue para produção ou homologação. No Jira, também chamada de **Version**.

**Exemplo de Releases:**
- `v1.0.0` – Cadastro + Login
- `v1.1.0` – Agendamento
- `v2.0.0` – App mobile

---

## 🧪 Conceitos do Xray (Plugin de Testes no Jira)

### 📌 Test
É um **caso de teste**. Define o que será testado, os passos e o resultado esperado.

---

### 📌 Test Set (Conjunto de Testes)
Conjunto de testes agrupados por critérios funcionais, técnicos ou lógicos.

**Exemplo:**  
> Test Set: `Testes de Login`  
> Inclui: `Login válido`, `Senha incorreta`, `Campo vazio`, etc.

---

### 📌 Test Plan (Plano de Teste)
Planejamento da execução de testes em uma determinada entrega/sprint.

**Exemplo:**  
> Test Plan: `Sprint 5`  
> Inclui: Test Set de Login, Cadastro, Notificações.

---

### 📌 Test Execution (Execução de Testes)
Registro de uma execução real de testes — mostra quais passaram, falharam ou ainda não foram executados.

---

### 📌 Traceability (Rastreabilidade)
Permite acompanhar a ligação entre:
- Requisitos ⇄ Casos de Teste ⇄ Execuções ⇄ Bugs encontrados

---

## 🔗 Relação: Sprint x Release

| Sprint                  | Release                         |
|-------------------------|----------------------------------|
| Curto prazo             | Médio/longo prazo                |
| Entrega parcial         | Entrega consolidada              |
| Iteração do desenvolvimento | Empacotamento final do sistema |

**Exemplo prático:**
- Sprint 1: cadastro + login
- Sprint 2: agendamento
- **Release v1.0.0:** inclui o que foi feito nas sprints 1 e 2

---
