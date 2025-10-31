#  Desafio Bootcamp Code Girl 2025 – Instâncias EC2

Este repositório faz parte de um desafio do Bootcamp Code Girl 2025, com foco em compreender e representar graficamente os principais serviços de infraestrutura da Amazon Web Services (AWS).  

O objetivo deste desafio é explorar conceitos de computação em nuvem**, utilizando diagramas criados no Draw.io para visualizar a arquitetura e o funcionamento dos recursos EC2, EBS e S3.  

---
## Diagrama 1 — EC2 com EBS e RDS

![image](EBS.png)

### Descrição do Fluxo

1. **Ator (Usuário)**: Interage com o sistema, enviando arquivos ou dados.
2. **Instância EC2 (Elastic Compute Cloud)**: Responsável pelo processamento central.  
   - Atua como o servidor que recebe e processa os arquivos enviados.
3. **EBS (Elastic Block Store)**:  
   - O **Disco D (EBS)** é usado como armazenamento de entrada, onde os arquivos são recebidos.
   - O **Disco E (EBS)** atua como armazenamento de saída, guardando os resultados processados.
4. **RDS (Relational Database Service)**:  
   - Mantém os dados estruturados e persistentes, como logs, metadados ou resultados processados.
5. Todo o ambiente está hospedado dentro da **nuvem AWS**, garantindo escalabilidade e segurança.

### Serviços AWS Utilizados

| Serviço | Função Principal |
|----------|------------------|
| **EC2** | Servidor virtual para execução de aplicações e processamento de dados. |
| **EBS** | Armazenamento em blocos persistente, acoplado à instância EC2. |
| **RDS** | Banco de dados relacional gerenciado pela AWS. |

---

## Diagrama 2 — S3, Lambda e DynamoDB

(S3.png)

### Descrição do Fluxo

1. **Sistema de Arquivos (Usuário ou Aplicação)**:  
   - Gera ou disponibiliza o arquivo que será enviado.
2. **Amazon S3 (Simple Storage Service)**:  
   - O arquivo é transferido via **AWS CLI** ou **Transfer File** para um bucket S3.
   - O upload de um novo arquivo aciona automaticamente um evento *trigger*.
3. **AWS Lambda (Função Serverless)**:  
   - Desenvolvida em **Node.js**, **.NET Core** ou **Python**.  
   - É executada automaticamente quando ocorre um novo upload no S3.
   - Processa o conteúdo do arquivo e extrai informações relevantes.
4. **Amazon DynamoDB**:  
   - Recebe e armazena as informações processadas pela função Lambda em formato NoSQL.
   - Permite consultas rápidas e escaláveis.

### Serviços AWS Utilizados

| Serviço | Função Principal |
|----------|------------------|
| **S3** | Armazenamento de objetos e ponto de entrada dos arquivos. |
| **Lambda** | Função serverless que processa os arquivos sem necessidade de servidor dedicado. |
| **DynamoDB** | Banco de dados NoSQL para armazenar dados estruturados processados pela Lambda. |

---


##  Objetivo do projeto

Este desafio tem como finalidade:  
- Reforçar o entendimento sobre a **arquitetura dos serviços da AWS**;  
- Exercitar a **documentação visual de soluções em nuvem**;  
- Promover boas práticas de **organização e versionamento de artefatos técnicos** usando o **GitHub**.  

---

## Ferramentas utilizadas

- **Draw.io** – criação dos diagramas  
- **Git & GitHub** – versionamento e publicação dos arquivos  
- **AWS Cloud Concepts** – base teórica para a representação dos serviços  

---

## Próximos passos

- Criar novos diagramas explorando outros serviços AWS (como VPC, RDS e Lambda);  
- Aprimorar a documentação com descrições mais detalhadas das conexões entre recursos;  
- Adicionar anotações explicativas dentro dos diagramas.  
