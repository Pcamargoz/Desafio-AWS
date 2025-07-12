# RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS

**Data:** 12/07/2025  
**Empresa:** Abstergo Industries  
**Responsável:** Pedro Cesar Camargo dos Santos

# Introdução
Este relatório apresenta o processo de implementação de soluções na empresa Abstergo Industries, realizado por Pedro Cesar Camargo dos Santos. O objetivo do projeto foi selecionar e configurar três serviços AWS a fim de reduzir imediatamente os custos operacionais e, ao mesmo tempo, preparar a farmácia para expansão de mercado e melhoria na experiência dos clientes.

## Descrição do Projeto
O projeto de implementação foi dividido em três etapas, cada uma com foco em um serviço AWS específico:

### Etapa 1: Amazon EC2  
- **Foco da ferramenta:** Infraestrutura de servidores em nuvem (IaaS) no modelo híbrido.  
- **Caso de uso:** Migrar parte da infraestrutura on‑premises (servidores internos da farmácia) para instâncias EC2, permitindo escalabilidade sob demanda.  
  - Durante horários de pico, sobe-se a quantidade de instâncias; em horários de menor uso, reduz-se, gerando economia de até 40 % em comparação a servidores 100 % dedicados. É usando somente o que realmente e nescessitado e usado.
  - Integração de VPN entre data center local e VPC na AWS garante segurança e alta disponibilidade.

### Etapa 2: Amazon Aurora Serverless  
- **Foco da ferramenta:** Banco de dados relacional gerenciado, que ajusta automaticamente capacidade de acordo com a demanda (serverless).  
- **Caso de uso:**  
  - Centralizar o armazenamento de dados de clientes, estoque e transações da farmácia.  
  - Pagar apenas pelo consumo efetivo de vCPU e I/O, diminuindo custos em períodos de baixa movimentação (ex.: madrugada).  
  - Automação de backups e replicação em múltiplas zonas de disponibilidade para garantir durabilidade e continuidade de negócios.

### Etapa 3: Amazon CloudFront  
- **Foco da ferramenta:** Content Delivery Network (CDN) global da AWS.  
- **Caso de uso:**  
  - Distribuir conteúdo estático e dinâmico (site, portal de clientes, imagens de produtos) por meio de edge locations em diversos países.  
  - Reduzir latência para usuários internacionais e melhorar a performance do site, contribuindo para expansão de vendas fora do Brasil.  
  - Diminuição de carga nos servidores de origem (EC2), gerando ainda mais economia de banda e processamento.

## Anexos
1. **Amazon EC2 User Guide** (documentação oficial):  
   https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/concepts.html

2. **Amazon Aurora Serverless** (documentação oficial):  
   https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Introduction.html#DAX.Serverless  
   *(para Aurora Serverless v2 veja também: https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-serverless.html)*

3. **Amazon CloudFront Developer Guide** (documentação oficial):  
   https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html

**Assinatura do responsável pelo projeto:**  
Pedro Cesar Camargo dos Santos
