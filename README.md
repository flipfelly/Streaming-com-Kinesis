# Sistema de Produção e Consumo de Dados com Kinesis

Este repositório contém dois exemplos de código para demonstrar como usar o **Amazon Kinesis** para implementar sistemas de **produção** e **consumo** de dados em tempo real.

## 📋 Descrição

As aplicações descritas nos dois códigos são **desacopladas** e **independentes** entre si, comunicando-se através de um serviço intermediário: o **Kinesis Stream**.

- A **primeira aplicação** atua como **produtora de dados**, enviando informações para o fluxo de dados do Kinesis.
- A **segunda aplicação** é o **consumidor**, que se conecta ao Kinesis, escuta os dados transmitidos e imprime os resultados à medida que são recebidos.

O **Kinesis Stream** age como intermediário entre essas aplicações, garantindo a comunicação em tempo real. Vale destacar que, no modelo de design, é possível ter diversas **aplicações consumidoras** (assinantes), todas recebendo os dados do mesmo fluxo, sem que haja uma relação direta entre elas.

## 🔄 O que é Streaming de Dados?

**Streaming de dados** é o processo de capturar, processar e analisar dados **continuamente** à medida que são gerados. Diferente dos tradicionais modelos de processamento em lote, onde os dados são processados em intervalos definidos, o **streaming** permite a análise **em tempo real**, proporcionando insights imediatos.

### Características do Streaming de Dados:
- **Transmissão Contínua**: Dados são transmitidos em tempo real, o que permite respostas imediatas a eventos à medida que ocorrem.
- **Escalabilidade**: O modelo de streaming é altamente escalável, permitindo que múltiplas aplicações leiam dados de um mesmo fluxo simultaneamente.
- **Processamento em Tempo Real**: Os dados são processados à medida que são gerados, sem a necessidade de esperar o término de grandes lotes de dados.

O **Amazon Kinesis** é uma plataforma gerenciada da AWS que facilita a ingestão, processamento e análise de grandes volumes de dados em tempo real. Com ele, você pode construir e gerenciar sistemas de streaming com alta disponibilidade e baixo custo.

## 🚀 Como Funciona?

1. **Aplicação Produtora**: Envia dados para o **Kinesis Stream**, que é o serviço de fluxo de dados da AWS.
2. **Kinesis Stream**: Atua como intermediário, recebendo e armazenando os dados enviados pela aplicação produtora.
3. **Aplicação Consumidora**: Conecta-se ao **Kinesis Stream**, escuta os dados em tempo real e os processa conforme necessário.


## 🛠️ Como Usar

### Passos:

1. **Configuração da AWS**: Crie um fluxo de dados no **Amazon Kinesis**.
2. **Credenciais de Acesso**: Certifique-se de que suas credenciais de acesso à AWS estejam corretamente configuradas no seu ambiente.
3. **Execução do Código**:
   - **Execute o código do Produtor** para enviar dados para o fluxo do Kinesis.
   - **Execute o código do Consumidor** para escutar e processar os dados em tempo real.

## ✅ Conclusão:

O uso do **Amazon Kinesis** para streaming de dados oferece uma maneira poderosa e escalável de trabalhar com dados em tempo real. Ainda existe a opção de criar um serviço de entrega com o Amazon Data Firehose, assim ele armazena os dados produzidos diretamente em um bucket S3 ou em outro serviço AWS, sem precisar de codificação e das aplicações criadas aqui, conforme a vontade do usuário.

---

Para mais informações sobre o **Amazon Kinesis**, consulte a [documentação oficial da AWS](https://aws.amazon.com/kinesis/).
