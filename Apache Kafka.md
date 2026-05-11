# Apache Kafka — Visão Geral

## O que é o Kafka?
O **Apache Kafka** é uma plataforma distribuída de **streaming de eventos** (event streaming), usada para **publicar, armazenar e processar grandes volumes de dados em tempo real** de forma escalável e resiliente.

---

## Qual problema o Kafka resolve?
Antes do Kafka, sistemas distribuídos enfrentavam problemas como:

- Forte acoplamento entre serviços (um sistema dependia diretamente do outro)
- Dificuldade para lidar com **altos volumes de dados em tempo real**
- Perda de mensagens em sistemas não resilientes
- Complexidade para integrar múltiplos produtores e consumidores
- Baixa escalabilidade em filas tradicionais

👉 O Kafka resolve esses problemas ao atuar como um **intermediário desacoplado**, garantindo:

- Alta **durabilidade** (dados persistidos em disco)
- **Escalabilidade horizontal**
- **Tolerância a falhas**
- Processamento de dados **em tempo real**

---

## Para que o Kafka serve?
Principais usos:

- **Mensageria assíncrona** (substituindo filas como RabbitMQ em alguns cenários)
- **Integração entre microserviços**
- **Streaming de dados em tempo real**
- **Event sourcing**
- **Data pipelines** (ETL em tempo real)
- **Monitoramento e logging distribuído**

---

## Como o Kafka funciona?

### Componentes principais:

- **Producer (Produtor)**  
  Envia mensagens (eventos) para o Kafka

- **Consumer (Consumidor)**  
  Lê e processa essas mensagens

- **Topic (Tópico)**  
  Categoria ou canal onde os eventos são armazenados

- **Partition (Partição)**  
  Divide o tópico para permitir paralelismo e escalabilidade

- **Broker**  
  Servidor Kafka que armazena e entrega dados

- **Cluster**  
  Conjunto de brokers trabalhando juntos

---

### Fluxo básico:

1. O **Producer** envia um evento para um **Topic**
2. O evento é persistido em uma **Partition**
3. Um ou mais **Consumers** leem esse evento de forma independente

---

## Como o Kafka "serve" (benefícios técnicos)

- **Desacoplamento**: produtores e consumidores não dependem diretamente
- **Persistência**: dados ficam armazenados por tempo configurável
- **Reprocessamento**: consumidores podem reler eventos antigos
- **Alta vazão**: suporta milhões de eventos por segundo
- **Escalável**: basta adicionar mais brokers/partições

---

## Exemplo prático

### Cenário: E-commerce

Quando um cliente realiza uma compra:

1. O sistema de checkout envia um evento `pedido_criado` para o Kafka
2. Diferentes serviços consomem esse evento:
   - Serviço de pagamento → processa cobrança
   - Serviço de estoque → atualiza inventário
   - Serviço de envio → prepara entrega
   - Serviço de notificações → envia email ao cliente

✅ Benefícios:
- Serviços independentes
- Fácil adicionar novos consumidores (ex: analytics)
- Sistema resiliente e escalável

---

## Resumo rápido

- Kafka = plataforma de **streaming distribuído**
- Resolve problemas de **escala, acoplamento e perda de dados**
- Funciona com **producers, topics e consumers**
- Usado para **event-driven architecture** e dados em tempo real
- Extremamente eficiente para **microserviços e pipelines de dados**

---
