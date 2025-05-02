# 📘 7 Fundamentos dos Testes de Software

Este documento apresenta os sete princípios fundamentais que orientam o processo de testes de software. Eles ajudam a entender os limites, objetivos e boas práticas ao validar a qualidade de um sistema.

---

## 1. Testes demonstram a presença de defeitos, não sua ausência

O objetivo dos testes é identificar defeitos existentes no software. Mesmo que nenhum defeito seja encontrado, isso não significa que o sistema esteja livre de erros. Os testes aumentam a confiança na qualidade, mas não garantem perfeição.

**Exemplo:** Imagine testar uma calculadora com vários cálculos e não encontrar falhas. Isso apenas indica que os testes realizados não encontraram erros — o sistema pode conter defeitos em cenários não testados.

---

## 2. Testes exaustivos são impossíveis

Testar todas as combinações possíveis de entradas, fluxos e situações é inviável na maioria dos sistemas. Por isso, é necessário selecionar os testes com base em critérios como risco, impacto e frequência de uso.

**Exemplo:** Um campo que aceita números de 1 a 1.000.000 possui um milhão de entradas possíveis. Testar todas seria impraticável, então escolhemos valores representativos, como limites (1, 1.000.000) e valores médios.

> Técnicas como particionamento de equivalência, análise do valor limite e testes baseados em risco tornam os testes mais eficazes.

---

## 3. Testes antecipados economizam tempo e dinheiro

Iniciar os testes nas fases iniciais do projeto ajuda a identificar falhas cedo, quando ainda são mais fáceis e baratas de corrigir. Quanto mais tarde um defeito é descoberto, maior o custo do retrabalho.

**Exemplo:** Encontrar um erro em um requisito durante a fase de análise é muito mais barato do que corrigi-lo após o sistema estar em produção.

> Práticas como TDD (Test Driven Development) e revisões de requisitos são exemplos de prevenção eficaz.

---

## 4. Defeitos se concentram em áreas específicas

Em muitos projetos, uma pequena parte do sistema concentra a maioria dos defeitos. Identificar essas áreas críticas permite que os testes se concentrem onde há maior probabilidade de encontrar falhas.

**Exemplo:** Em um sistema de e-commerce, o módulo de pagamento pode apresentar mais falhas devido à sua complexidade e número de integrações.

> Analisar o histórico de bugs e a complexidade do código ajuda a priorizar essas áreas.

---

## 5. O paradoxo do pesticida

Se os mesmos testes forem repetidos continuamente, eles deixam de ser eficazes para descobrir novos defeitos. Assim como pragas agrícolas criam resistência a pesticidas, o sistema se “acostuma” aos testes repetitivos.

**Exemplo:** Se sempre testamos um app com os mesmos dados, podemos deixar de identificar erros que ocorreriam com combinações ou fluxos diferentes.

> Atualize os testes com frequência para manter sua eficácia.

---

## 6. Testes são dependentes do contexto

Não existe uma única maneira correta de testar. A abordagem deve ser adaptada ao tipo de software, ao ambiente, aos riscos envolvidos e aos objetivos do projeto.

**Exemplo:** Um sistema bancário exige testes rigorosos, validações legais e alta segurança. Já um jogo pode priorizar desempenho e experiência do usuário.

> Conhecer o contexto permite definir melhores estratégias e ferramentas de teste.

---

## 7. A ausência de defeitos não significa que o sistema seja utilizável

Mesmo que o software não apresente erros técnicos, ele pode falhar em atender às necessidades reais do usuário. Usabilidade, acessibilidade e clareza são aspectos essenciais da qualidade.

**Exemplo:** Um aplicativo sem erros técnicos, mas com uma interface confusa, pode ser rejeitado pelos usuários.

> Qualidade vai além de “funcionar”; significa também “ser útil e intuitivo”.

---

🧪 **Resumo:**  
Estes fundamentos formam a base para qualquer estratégia de testes eficiente. Ao compreendê-los, profissionais de QA, desenvolvedores e gerentes de projeto conseguem tomar decisões mais acertadas para garantir a qualidade do software.
