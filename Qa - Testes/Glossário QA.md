
# 📘 Glossário de Termos Técnicos para QAs

## 🔍 Testes

- **Testes Manuais**  
  Processo de execução dos casos de teste sem o uso de ferramentas automatizadas. É o testador quem verifica, passo a passo, se o sistema funciona corretamente.

- **Testes Automatizados**  
  São testes realizados por scripts usando ferramentas automatizadas. Garantem maior cobertura e repetibilidade.

- **Teste de Regressão**  
  Verifica se uma nova alteração no sistema não quebrou funcionalidades que antes funcionavam corretamente.

- **Teste de Integração**  
  Avalia se diferentes módulos ou sistemas interagem corretamente entre si.

- **Teste de Unidade (Unit Test)**  
  Foca em pequenas partes isoladas do código, geralmente funções ou métodos, para garantir que cada parte funcione individualmente.

- **Teste Funcional**  
  Verifica se o sistema realiza corretamente as funções esperadas pelo usuário.

- **Teste Não Funcional**  
  Avalia atributos como desempenho, usabilidade, escalabilidade, entre outros.

- **Teste Exploratório**  
  Técnica onde o QA explora o sistema de forma livre, tentando encontrar erros sem seguir um roteiro fixo.

## 💬 Documentação e Planejamento

- **Plano de Testes**  
  Documento que descreve o escopo, a abordagem, os recursos e o cronograma das atividades de teste.

- **Caso de Teste (Test Case)**  
  Conjunto de condições e ações específicas para validar uma funcionalidade.

- **Roteiro de Testes (Test Script)**  
  Passo a passo detalhado com os dados necessários para executar um teste.

- **Matriz de Rastreamento (Traceability Matrix)**  
  Mapeia os requisitos aos casos de teste, garantindo cobertura completa.

## 🛠️ Ferramentas e Tecnologias

- **Selenium**  
  Ferramenta para automação de testes em navegadores web.

- **Cypress**  
  Framework moderno de automação para testes end-to-end em aplicações web.

- **JIRA**  
  Ferramenta de gestão de projetos e rastreamento de bugs.

- **Postman**  
  Utilizado para testar APIs REST, criando requisições e validando respostas.

- **Appium**  
  Ferramenta para automação de testes em aplicativos mobile (Android e iOS).

- **Git e GitHub**  
  Sistema de controle de versão e plataforma de hospedagem de código.

## 🧪 Conceitos de Qualidade

- **Bug / Defeito**  
  Erro no sistema que provoca comportamentos inesperados.

- **Severity**  
  Nível de impacto que o defeito causa no sistema.

- **Priority**  
  Urgência com que o defeito deve ser corrigido.

- **Smoke Test**  
  Testes rápidos para verificar se o sistema está estável o suficiente para testes mais profundos.

- **Sanity Test**  
  Verificações rápidas em uma funcionalidade específica para confirmar que ela funciona após uma mudança.

- **Ambiente de Homologação**  
  Ambiente semelhante ao de produção onde o sistema é testado antes de ir ao ar.

## 🔁 Metodologias e Processos

- **Agile / Scrum**  
  Metodologias ágeis focadas em entregas rápidas e contínuas com foco na colaboração.

- **Sprint**  
  Ciclo de trabalho dentro do Scrum, normalmente com duração de 1 a 4 semanas.

- **Daily Meeting**  
  Reunião diária para alinhamento da equipe.

- **PO (Product Owner)**  
  Responsável por definir as prioridades do produto e garantir que as entregas tragam valor ao negócio.

## 📦 Tipos de Teste

- **Teste de Carga (Load Testing)**  
  Avalia como o sistema se comporta com um volume esperado de usuários ou transações.

- **Teste de Estresse (Stress Testing)**  
  Verifica a estabilidade do sistema ao operar além dos limites normais de carga.

- **Teste de Performance**  
  Mede tempo de resposta, uso de recursos e escalabilidade do sistema.

- **Teste de Segurança**  
  Identifica vulnerabilidades, riscos e falhas de segurança no sistema.

- **Teste de Usabilidade**  
  Avalia a facilidade com que os usuários interagem com o sistema.

- **Teste de Compatibilidade**  
  Garante que o sistema funcione corretamente em diferentes navegadores, dispositivos e sistemas operacionais.

- **Teste de Aceitação (UAT - User Acceptance Testing)**  
  Realizado pelo cliente ou usuário final para validar se o sistema atende aos requisitos.

- **Teste de Caixa Preta (Black Box)**  
  Foca nos resultados da aplicação sem considerar a lógica interna do código.

- **Teste de Caixa Branca (White Box)**  
  Analisa o código-fonte e sua lógica interna para garantir a cobertura de execução.

- **Teste de Caixa Cinza (Gray Box)**  
  Combina técnicas de caixa preta e branca, com algum conhecimento do sistema interno.

## 🧱 Conceitos Técnicos

- **CI/CD (Integração e Entrega Contínua)**  
  Prática de desenvolvimento que permite que mudanças de código sejam integradas, testadas e entregues automaticamente.

- **Pipeline de Testes**  
  Conjunto de etapas automatizadas executadas para validar e entregar o software.

- **Mock**  
  Objeto simulado usado em testes para imitar o comportamento de componentes reais.

- **Staging**  
  Ambiente de testes que simula a produção, utilizado antes da liberação final.

- **Hotfix**  
  Correção urgente aplicada diretamente na produção.

- **Rollback**  
  Reversão do sistema para uma versão anterior em caso de falha.

- **Versionamento Semântico (SemVer)**  
  Convenção para nomear versões no formato MAJOR.MINOR.PATCH.

- **Pull Request (PR)**  
  Requisição para mesclar alterações de uma branch para outra em um repositório Git.

- **Branch**  
  Ramificação do código usada para desenvolver funcionalidades de forma isolada.

- **Merge**  
  Processo de unir alterações de uma branch com outra.

## 🗂️ Tipos de Artefatos

- **Backlog**  
  Lista de funcionalidades, melhorias e correções pendentes do projeto.

- **História de Usuário (User Story)**  
  Descrição simples de uma necessidade do usuário final.

- **Critérios de Aceitação**  
  Condições que devem ser atendidas para considerar uma história como "concluída".

- **Definição de Pronto (Definition of Ready)**  
  Critérios que uma tarefa precisa cumprir para entrar no sprint.

- **Definição de Pronto (Definition of Done)**  
  Critérios que indicam quando uma tarefa está verdadeiramente finalizada.

## 📋 Tipos de Erros

- **Erro Crítico**  
  Impede a continuidade do uso do sistema.

- **Erro Grave**  
  Impacta significativamente a funcionalidade, mas pode haver uma alternativa.

- **Erro Médio**  
  Causa transtorno, mas não impede o uso.

- **Erro Leve**  
  Pequeno problema estético ou de usabilidade.

- **Erro Intermitente**  
  Ocorre de forma aleatória ou apenas em certas condições.
