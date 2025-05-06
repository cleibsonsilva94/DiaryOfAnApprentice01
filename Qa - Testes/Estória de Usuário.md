# 📘 Estória de Usuário (ou História)

Uma **estória de usuário** é uma narrativa simples onde o cliente descreve como os usuários utilizarão determinada funcionalidade do sistema. Trata-se de um passo a passo claro e objetivo sobre como a funcionalidade será usada na prática.

---

## 📌 INVEST

O acrônimo **INVEST** resume as características ideais de uma boa estória de usuário:

### 🧩 I - Independente
A estória deve conter informações suficientes para que a equipe de desenvolvimento consiga compreendê-la e implementá-la sem depender de outros requisitos, histórias ou contextos. Isso evita bloqueios e facilita a organização do trabalho.

### 🤝 N - Negociável
Estórias de usuário não são contratos fechados. Elas devem ser abertas a ajustes e melhorias durante as conversas entre equipe e cliente. O mais importante é que todos concordem que a funcionalidade tem valor para o usuário final.

### 💎 V - Valiosa
Cada estória precisa entregar algo que agregue valor ao cliente ou usuário. Deve estar clara a importância daquela funcionalidade dentro do sistema, seja pela experiência do usuário, por facilitar tarefas ou por atender a uma necessidade específica.

### 📏 E - Estimável
É fundamental que a estória possa ser estimada em termos de esforço técnico. A equipe deve conseguir avaliar quanto tempo e recursos serão necessários para desenvolver a funcionalidade, considerando complexidade, riscos e impacto.

### 📦 S - Small (Pequena)
Estórias devem ser curtas e objetivas. Se forem muito longas ou complexas, é melhor dividi-las em partes menores e mais fáceis de implementar. Estórias pequenas facilitam a organização, o planejamento e a entrega contínua.

### ✅ T - Testável
A estória deve permitir testes claros e objetivos. Isso inclui:
- O que exatamente será testado;
- Quais os critérios de aceitação;
- Quais os resultados esperados.

**Exemplo:**
> Se tivermos 500 usuários acessando simultaneamente, a página deve carregar em até 4 segundos em dispositivos móveis com conexão 4G.

**Outro exemplo:**
> A disponibilidade do sistema deve ser monitorada e mantida em um nível acordado. 100% não é realista, mas métricas confiáveis devem ser utilizadas para garantir qualidade.

Esse modelo ajuda a equipe a entender melhor o que precisa ser feito, priorizar o que realmente importa e entregar software de forma mais ágil, com qualidade e foco no usuário.

---

## 🛠️ Pre-Game (Planejamento Inicial)

Etapa anterior às sprints, onde as estórias são pensadas e planejadas pelo **PO** e pelos clientes.

Também chamada de **Sprint de Planejamento** ou **Sprint 0**. Em algumas metodologias, é conhecida como **Inception** (início).

🎯 O objetivo principal é criar as estórias de usuário.

Uma vez criadas, elas vão para o **Backlog** e devem ser priorizadas pelo PO conforme sua importância.

---

## 🔁 Sprint

Ciclo de desenvolvimento com foco em entendimento e execução.

- Pode variar de **2 a 4 semanas** (Scrum).
- No **Extreme Programming**, geralmente é de **1 semana**.
- No **Kanban**, pode ou não existir o conceito de sprint, pois o foco está em entregas contínuas e incrementais.

---

## 📋 Sprint Backlog

Contém exatamente a quantidade de trabalho que a equipe pode realizar sem sobrecarga.

- Novas estórias podem surgir.
- Estórias podem ser substituídas ou corrigidas.
- Os **critérios de aceitação** precisam ser claros, mesmo diante dessa fluidez.

**Pergunta-chave:**
> O que eu preciso testar para garantir que o sistema está de fato funcionando?

---

## 🧱 Épicos

São visões amplas e completas: várias estórias que, juntas, formam uma funcionalidade ou módulo maior do sistema.

🔍 Imagine um quebra-cabeça. O épico é a **imagem completa da caixa** — o que orienta a construção.

---

## ⚙️ Features

Subdivisões de um épico. Um épico pode conter várias **features**, e cada feature pode ter várias **estórias de usuário**.

São partes visíveis de uma funcionalidade que têm valor para o cliente.


# ⚠️ Análise de Risco

## 📌 O que é risco?

**Risco** é um evento incerto e geralmente negativo que pode impactar negativamente a entrega de um projeto ou o funcionamento de uma funcionalidade específica do sistema.

---

## 🧠 Como lidar com riscos?

Para que os riscos sejam tratados de forma eficiente, é necessário:

- 📊 **Avaliar** o risco;
- 🏷️ **Classificá-lo** conforme sua gravidade e probabilidade;
- 📋 **Organizá-lo** do maior para o menor impacto;
- 👤 **Atribuí-lo** a alguém responsável pelo monitoramento.

---

## 🔢 Mensuração do risco

Riscos também podem ser **mensurados com valores numéricos**, permitindo uma análise mais objetiva e técnica. Por exemplo:

- Probabilidade (de 0 a 1);
- Impacto (pontuação de 1 a 5);
- Risco total = Probabilidade × Impacto.

---

## ✅ Ações possíveis diante de um risco

Existem quatro abordagens principais que podemos adotar frente a um risco identificado:

- 🔽 **Mitigar:** Reduzir a probabilidade ou o impacto do risco;
- ❌ **Eliminar:** Remover completamente a causa do risco;
- 🔁 **Transferir:** Delegar a responsabilidade do risco a terceiros (ex: seguros, contratos);
- 🤷‍♂️ **Aceitar:** Reconhecer o risco e seguir com o plano, ciente das possíveis consequências.

---

## 🎯 Conclusão

Uma boa **análise de risco** é essencial para garantir a estabilidade, previsibilidade e sucesso de qualquer projeto. Antecipar problemas potenciais é uma forma inteligente de proteger entregas e gerar valor com mais segurança.
