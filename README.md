# 🚀 AWS Generative AI & Cloud Solutions Portfolio
(AWS Bedrock, SageMaker, Lambda, IaC e Agentes de IA)

![Status: Concluído](https://img.shields.io/badge/Status-Concluído-success) 
![Área: Cloud & GenAI](https://img.shields.io/badge/Foco-Cloud%20%7C%20GenAI%20%7C%20SecOps-blue)

Este repositório consolida a experiência prática e as implementações realizadas nos laboratórios do AWS Cloud Quest com foco em **IA Generativa**, **DevOps** e **Segurança**. O projeto demonstra proficiência na construção e gestão de *pipelines* de IA ponta-a-ponta e soluções de Cloud Computing altamente disponíveis.

---

## 🛠️ Tecnologias e Serviços Utilizados

Este conjunto de projetos envolveu a orquestração dos seguintes serviços:

| Categoria | Serviço | Descrição |
| :--- | :--- | :--- |
| **Inteligência Artificial** | Amazon Bedrock, SageMaker, Amazon Q | Deployment de LLMs, Prompt Engineering, Criação de Agentes, Modelos Fundacionais (LLaMA 2, Mistral). |
| **Computação** | AWS Lambda, Amazon EC2 | Funções Serverless para ações de Agentes de IA; Implementação de IaaS (Infraestrutura como Serviço). |
| **Armazenamento/BD** | Amazon DynamoDB, Amazon S3 | Persistência de metadados e arquivos (Knowledge Base, Logs). |
| **Segurança/Rede** | IAM (Identity and Access Management) | Criação de políticas de acesso com o Princípio do Menor Privilégio. |

---

## 🧠 Módulo I: Construção de Agente Inteligente de IA (RAG & Ações)

**Referência:** Diagrama **"crie_agente_de_IA.png"**

### Desafio
Criar um assistente inteligente capaz de responder a perguntas usando uma base de conhecimento privada (técnica **RAG**) e executar ações transacionais (como enviar uma solicitação de férias).

### Implementação
1.  **Agente Bedrock:** Configurado para orquestrar o fluxo de interação com o usuário e a tomada de decisão.
2.  **Knowledge Base (RAG):** Utilizada para acessar documentos não estruturados armazenados no Amazon S3, garantindo que as respostas sejam factuais e baseadas em dados corporativos.
3.  **Grupo de Ações:** Utilização de duas funções **AWS Lambda** (`submit_leave` e `submit_benefits`) para processar e registrar solicitações, interagindo com o **Amazon DynamoDB**.

### Ganhos
Demonstração de arquitetura complexa de GenAI, combinando LLMs com sistemas transacionais para automatizar tarefas internas com segurança e controle de acesso via IAM.

#### Arquitetura Detalhada: Agente de IA



---

## 🧪 Módulo II: Deployment e Prompt Engineering (SageMaker)

**Referência:** Diagrama **"Serviços_de_IA_com_sagemaker.png"**

### Objetivo
Implantar um LLM (Meta LLaMA 3.2 1B Instruct) no Amazon SageMaker AI para configurar um endpoint robusto e testar diferentes técnicas de **Prompt Engineering** para otimização de saída.

### Implementação
* Uso do **SageMaker Studio** e **JupyterLab Notebook** para interagir, configurar e testar o modelo.
* Criação de um **Endpoint de Modelo** para permitir o consumo seguro da IA via API com o SageMaker Python SDK.

### Ganhos
Prova de habilidade em **ML Ops** e *deployment* de modelos de Machine Learning na nuvem, além do domínio na aplicação estratégica de prompts para melhoria de performance da GenAI.

#### Arquitetura Detalhada: SageMaker Deployment



---

## ☁️ Módulo III: Fundamentos de Cloud, Serverless e Multi-Serviços

Este módulo abrange a criação de infraestrutura básica, *pipelines* de processamento e a integração de código assistido por IA.

### A. Serverless e Amazon Q

**Referência:** Diagrama **"construindo_codigo_amazonQ.png"**

* **Implementação:** Utilização do **Amazon Q Developer** para assistência na criação de uma função **Lambda** que interage com o **Bedrock** (para gerar conteúdo) e armazena os dados gerados em S3/DynamoDB.
* **Ganhos:** Confirmação de *skills* em ambientes Serverless e uso de ferramentas de assistência de código (Amazon Q) para aumentar a produtividade.

#### Arquitetura: Lambda e Amazon Q



### B. Alta Disponibilidade e IaaS

**Referência:** Diagrama **"Passos_na_nuvem.png"**

* **Implementação:** Criação de duas instâncias **EC2** em **Zonas de Disponibilidade (AZs)** separadas para garantir resiliência contra falhas de infraestrutura.
* **Ganhos:** Domínio de conceitos de Cloud Foundations, como **Alta Disponibilidade (HA)** e o uso estratégico de Zonas de Disponibilidade.

#### Arquitetura: Alta Disponibilidade (EC2)



### C. Pipeline de Processamento de IA

**Referência:** Diagrama **"Serviços_de_IA_com_sagemaker.png"**

* **Implementação:** Criação de um *pipeline* complexo usando o SDK **Boto3** para orquestrar múltiplos serviços de IA (Polly, Textract, Comprehend, Translate, Transcribe) para processamento de texto, fala e sentimentos.
* **Ganhos:** Capacidade de criar soluções de IA multimodais e complexas integrando diversos serviços da AWS.

---

