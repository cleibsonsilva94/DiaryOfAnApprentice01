# Apache Kafka — Visão Geral

## O que é o Kafka?
O **Apache Kafka** é uma plataforma distribuída de **streaming de eventos**. Ele permite publicar, armazenar e consumir dados em tempo real com alta performance e escalabilidade ⚡.

Na prática, funciona como um intermediário confiável entre sistemas, garantindo que eventos não sejam perdidos e possam ser processados no momento certo ou até reprocessados depois.

---

## Qual problema o Kafka resolve?
Em sistemas distribuídos tradicionais, é comum enfrentar:

- Forte acoplamento entre serviços  
- Dificuldade para escalar 📈  
- Risco de perda de mensagens  
- Baixa eficiência com dados em tempo real  

O Kafka resolve isso atuando como um hub central de eventos, permitindo comunicação assíncrona e desacoplada 🔄. Quem produz dados não precisa conhecer quem consome.

---

## Para que o Kafka serve?
O Kafka é usado principalmente para troca de dados em tempo real entre sistemas.

Cenários comuns:

- Comunicação entre microserviços  
- Processamento de eventos em tempo real  
- Integração de sistemas  
- Pipelines de dados (ETL streaming)  
- Arquitetura orientada a eventos  

---

## Como o Kafka funciona?
O funcionamento se baseia em alguns componentes principais:

- **Producer**: envia eventos 📤  
- **Topic**: canal onde os eventos são armazenados  
- **Partition**: divisão do topic para permitir escala  
- **Broker**: servidor que armazena os dados  
- **Consumer**: lê os eventos 📥  

Fluxo básico:

1. O producer envia um evento para um topic  
2. O evento é armazenado  
3. Os consumers leem quando necessário  

---

## Analogia
Imagine o Kafka como um sistema de correios 📬:

O producer envia cartas, o topic é a caixa postal por assunto, o broker é a agência e o consumer é quem recebe.

A diferença é que a carta não desaparece depois de lida — ela continua disponível para outros consumidores ou para releitura.

Isso elimina dependência direta entre sistemas 🔗❌.

---

## Exemplo prático
Em um e-commerce, ao criar um pedido (`pedido_criado`):

- O sistema envia o evento para o Kafka  
- Outros serviços consomem:
  - Pagamento processa cobrança 💳  
  - Estoque atualiza produtos 📦  
  - Entrega inicia envio 🚚  
  - Notificação envia mensagem 📧  

Cada serviço funciona de forma independente, tornando o sistema mais escalável e resiliente.

---

# Tópicos, Partições e Offsets

## Tópicos (Topics)
Um topic é o canal onde os eventos são armazenados. Ele funciona como um log contínuo onde novas mensagens são adicionadas no final 🧾.

Exemplo:
pedidos → pedido_criado, pedido_pago, pedido_enviado

Vários producers podem escrever e vários consumers podem ler o mesmo tópico.

---

## Partições (Partitions)
Um topic é dividido em partições para permitir escala e paralelismo ⚙️.

Cada partição é um log ordenado e independente.

Exemplo:

Topic: pedidos  
Partition 0 → evento1, evento2  
Partition 1 → evento3, evento4  
Partition 2 → evento5, evento6  

A ordem é garantida apenas dentro da partição.

---

## Offset
O offset é a posição de cada mensagem dentro da partição.

Exemplo:

Partition 0  
Offset 0 → evento1  
Offset 1 → evento2  
Offset 2 → evento3  

O consumer usa o offset para saber onde parou e continuar a leitura ▶️.

Exemplo:
último offset lido: 2  
próximo: 3  

---

## Por que isso é importante?
Esse modelo permite:

- Controle total de leitura pelo consumer  
- Mensagens persistidas (não somem) 💾  
- Reprocessamento de eventos  

Isso é essencial para lidar com falhas e consistência de dados.

---

## Resumo final
Topic organiza os eventos 🧭  
Partition permite escalabilidade e paralelismo ⚡  
Offset controla a leitura 📍  

Esses três conceitos são a base do Kafka e explicam sua performance, confiabilidade e flexibilidade.
