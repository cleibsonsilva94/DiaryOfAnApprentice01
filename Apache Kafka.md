# Apache Kafka — Visão Geral

## O que é o Kafka?
O **Apache Kafka** é uma plataforma distribuída de **streaming de eventos**, usada para **publicar, armazenar e processar dados em tempo real** com alta performance e escalabilidade.

---

## Qual problema o Kafka resolve?
Sem Kafka, sistemas sofrem com:

- Acoplamento forte entre serviços
- Baixa escalabilidade
- Perda de mensagens
- Dificuldade em lidar com dados em tempo real

👉 O Kafka resolve isso atuando como um **hub central de eventos**, permitindo comunicação **assíncrona, confiável e desacoplada**.

---

## Para que o Kafka serve?

Principais usos:

- Mensageria entre microserviços
- Processamento de eventos em tempo real
- Integração de sistemas
- Pipelines de dados (ETL streaming)
- Event-driven architecture

---

## Como o Kafka funciona?

### Componentes:

- **Producer** → envia eventos
- **Topic** → canal/categoria de eventos
- **Partition** → divide dados para paralelismo
- **Broker** → servidor Kafka
- **Consumer** → processa eventos

---

### Fluxo:

1. Producer envia evento para um Topic  
2. Evento é armazenado em Partitions  
3. Consumers leem e processam os dados  

---

## Benefícios técnicos

- Desacoplamento entre sistemas  
- Alta performance (milhões de eventos/segundo)  
- Persistência e reprocessamento  
- Escalabilidade horizontal  
- Tolerância a falhas  

---

## Analogia (importante para entender)

Imagine o Kafka como um **sistema de correios**:

- **Producer** → pessoa enviando cartas  
- **Topic** → tipo de caixa postal (ex: "Contas", "Pedidos")  
- **Broker** → agência dos correios  
- **Consumer** → pessoa que recebe e lê as cartas  

📌 Como funciona:
- Você envia uma carta (evento)
- Ela vai para a caixa postal (topic)
- Várias pessoas podem acessar e ler essa carta em momentos diferentes

✅ Diferencial:
- A carta **não desaparece imediatamente** → fica armazenada
- Várias pessoas podem ler a mesma carta independentemente
- Não precisa saber quem vai consumir → desacoplamento total

---

## Exemplo prático

### E-commerce

Evento: `pedido_criado`

- Producer → sistema de checkout envia o evento
- Consumers:
  - Pagamento → processa cobrança
  - Estoque → atualiza inventário
  - Entrega → prepara envio
  - Notificação → envia email

✅ Vantagens:
- Serviços independentes
- Fácil escalar ou adicionar novos consumidores
- Sistema resiliente

---

## Resumo rápido

- Kafka = plataforma de eventos distribuída
- Resolve problemas de escala, acoplamento e confiabilidade
- Baseado em Producers + Topics + Consumers
- Ideal para sistemas distribuídos e tempo real
- Muito usado em arquiteturas modernas (microserviços)

---
