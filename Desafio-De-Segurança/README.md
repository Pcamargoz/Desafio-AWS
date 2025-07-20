# RELATÓRIO DE IMPLEMENTAÇÃO DE MEDIDAS DE SEGURANÇA  

**Data:** 20/07/2025  
**Empresa:** Abstergo Industries  
**Responsável:** Pedro Cesar Camargo dos Santos  

---

## 🧾 Introdução  
Este relatório apresenta o processo de implementação de ferramentas na empresa **Abstergo Industries**, realizado por **Pedro Cesar Camargo dos Santos**. O objetivo do projeto foi elencar **3 medidas de segurança integradas aos serviços da AWS**, com a finalidade de aumentar a proteção da empresa.

---

## 🔐 Descrição do Projeto  
O projeto de implementação de ferramentas foi dividido em **3 medidas de segurança**, além de um bônus útil para arquiteturas de banco de dados.

### ✅ Medida 1: AWS WAF (Web Application Firewall)  
- **Caso de uso:** Proteger aplicações web contra **SQL Injection, XSS, bots maliciosos**, entre outras ameaças à camada de aplicação.  
- **Implementação:**  
  - Configuração de **Web ACLs** com regras pré-definidas e personalizadas.  
  - Integração nativa com **CloudFront, ALB, API Gateway e EC2**, defendendo o backend antes dos acessos.  

🔗 [Documentação AWS WAF](https://docs.aws.amazon.com/waf/latest/developerguide/what-is-aws-waf.html)

---

### ✅ Medida 2: AWS Shield Advanced  
- **Caso de uso:** Defesa contra **ataques DDoS sofisticados** nas camadas 3, 4 e 7, com suporte especializado.  
- **Implementação:**  
  - Proteção para **EC2, ALB, CloudFront e Route 53**.  
  - Integração com AWS WAF para auto bloqueios por taxa de requisição.  
  - Alertas via **CloudWatch** e **SNS**.  

🔗 [Documentação AWS Shield Advanced](https://docs.aws.amazon.com/waf/latest/developerguide/getting-started-ddos.html)

---

### ✅ Medida 3: AWS Macie  
- **Caso de uso:** Descobrir, classificar e proteger **dados sensíveis** (PII, financeiros, etc.) armazenados no **Amazon S3**.  
- **Implementação:**  
  - Ativação do Macie.  
  - Criação de jobs automatizados para escanear e classificar dados.  
  - Integração com **CloudWatch** para alertas e respostas.  

🔗 [Documentação AWS Macie](https://docs.aws.amazon.com/macie/latest/user/what-is-macie.html)

---

### 🌟 Bônus: Read Replicas (Amazon RDS)  
- **Caso de uso:** Escalar leitura de bancos relacionais para reduzir carga, elevar disponibilidade e distribuir consultas por região/AZ.  
- **Implementação:**  
  - Criação de **Read Replicas** (cópias somente leitura) do RDS para MySQL, PostgreSQL, Oracle, SQL Server, etc.  
  - Direcionamento de tráfego de leitura para essas réplicas, aliviando o banco principal.  
  - Configuração de réplicas em múltiplas **Availability Zones** ou **Regiões**, com failover manual quando necessário. 

🔗 [Documentação: Working with DB instance read replicas](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_ReadRepl.html)

---

## 🧩 Conclusão  
A implementação do **AWS WAF**, **Shield Advanced**, **Macie** (e o bônus de Read Replicas) na Abstergo Industries resultou em:

- Defesa multicamadas (aplicação, rede e dados);  
- Capacidade de resposta a ataques DDoS complexos;  
- Governança aprimorada de dados sensíveis;  
- Escalabilidade e alta disponibilidade para operações de leitura do banco de dados.

Essas medidas incrementam consideravelmente a **postura de segurança e resiliência** da empresa.

---

## 📎 Anexos  

- [AWS WAF – Documentação](https://docs.aws.amazon.com/waf/latest/developerguide/what-is-aws-waf.html)  
- [AWS Shield Advanced – Documentação](https://docs.aws.amazon.com/waf/latest/developerguide/getting-started-ddos.html)  
- [AWS Macie – Documentação](https://docs.aws.amazon.com/macie/latest/user/what-is-macie.html)  
- [Amazon RDS Read Replicas](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_ReadRepl.html)

---

## ✍️ Assinatura do responsável pelo projeto  
**Pedro Cesar Camargo dos Santos**
