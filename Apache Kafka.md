# Apache Kafka — Visão Geral

## O que é o Kafka?
O **Apache Kafka** é uma plataforma distribuída de **streaming de eventos**. Ele permite publicar, armazenar e consumir dados em tempo real com alta performance e escalabilidade.

Na prática, funciona como um intermediário confiável entre sistemas, garantindo que eventos não sejam perdidos e possam ser processados no momento certo ou até reprocessados depois.

---

## Qual problema o Kafka resolve?
Em sistemas distribuídos tradicionais, é comum enfrentar acoplamento forte entre serviços, dificuldade para escalar, risco de perda de mensagens e baixa eficiência com dados em tempo real.

O Kafka resolve isso atuando como um hub central de eventos, permitindo comunicação assíncrona e desacoplada. Quem produz dados não precisa conhecer quem consome.

---

## Para que o Kafka serve?
O Kafka é usado principalmente para troca de dados em tempo real entre sistemas. É comum em comunicação entre microserviços, processamento de eventos em tempo real, integração de sistemas, pipelines de dados (ETL streaming) e arquiteturas orientadas a eventos.

---

## Como o Kafka funciona?
O funcionamento se baseia em alguns componentes principais:

- **Producer**: envia eventos  
- **Topic**: canal onde os eventos são armazenados  
- **Partition**: divisão do topic para permitir escala  
- **Broker**: servidor que armazena os dados  
- **Consumer**: lê os eventos  

O fluxo é simples: um producer envia um evento para um topic, esse evento é armazenado e os consumers podem lê-lo quando quiserem.

---

## Analogia
Imagine o Kafka como um sistema de correios:

O producer envia cartas, o topic é a caixa postal por assunto, o broker é a agência e o consumer é quem recebe. A diferença é que a carta não desaparece depois de lida — ela continua disponível para outros leitores ou para releitura.

Isso elimina dependência direta entre sistemas.

---

## Exemplo prático
Em um e-commerce, ao criar um pedido (`pedido_criado`), o sistema envia esse evento para o Kafka. Outros serviços consomem esse evento: pagamento processa a cobrança, estoque atualiza produtos, entrega inicia envio e notificação envia mensagens ao cliente.

Cada serviço funciona de forma independente.

---

# Tópicos, Partições e Offsets

## Tópicos (Topics)
Um topic é o canal onde os eventos são armazenados. Ele funciona como um log contínuo onde novas mensagens são adicionadas no final.

Exemplo:
pedidos → pedido_criado, pedido_pago, pedido_enviado

Vários produtores podem escrever e vários consumidores podem ler esse mesmo tópico.

---

## Partições (Partitions)
Um topic é dividido em partições para permitir escala e paralelismo.

Cada partição é um log ordenado independente, permitindo distribuição de carga e leitura paralela.

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

O consumer usa o offset para saber onde parou e continuar a leitura.

Exemplo:
último offset lido: 2  
próximo: 3  

---

## Por que isso é importante?
Esse modelo permite que o consumer controle sua leitura, que as mensagens permaneçam armazenadas e que eventos possam ser relidos.

Isso possibilita reprocessamento em caso de erro, algo essencial em sistemas distribuídos.

---

## Resumo final
Topic organiza os eventos.  
Partition permite escalabilidade e paralelismo.  
Offset controla a leitura.  

Esses três conceitos formam a base do Kafka e explicam sua alta performance, confiabilidade e flexibilidade.
