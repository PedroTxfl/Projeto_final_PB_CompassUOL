# Projeto para Fast Engineering S/A
### Escopo:
O objetivo é estabelecer a infraestrutura de servidores para a empresa "Fast Engineering S/A" na plataforma AWS, seguindo as práticas DevOps recomendadas, a fim de assegurar alta disponibilidade, escalabilidade e segurança.

### Arquitetura:
<div align= "center">
<img src="https://github.com/PedroTxfl/Projeto_final_PB_CompassUOL/issues/1#issue-1845653082" width="200" />
</div>div>
- Ambiente Kubernetes (EKS):
   - Aproveitar o serviço Amazon Elastic Kubernetes Service (Amazon EKS) para coordenar e administrar os contêineres da aplicação em um ambiente com alta disponibilidade e escalabilidade.

- Banco de dados PaaS:
   - Empregar o serviço Amazon Relational Database Service (Amazon RDS) para alojar o banco de dados MySQL. O RDS oferece gestão automatizada, expansibilidade e backups automáticos.

- MultiAZ:
   - Estabelecer o RDS com alta disponibilidade MultiAZ, assegurando que réplicas do banco de dados sejam configuradas em diferentes zonas de disponibilidade para aumentar a resiliência a falhas.

- Persistência dos Dados:
   - Utilizar o Elastic Block Store (EBS) para prover armazenamento persistente aos contêineres, garantindo a segurança dos dados mesmo após a reinicialização das instâncias.

- Balanceamento de carga com healthcheck:
   - Implantar o Amazon Elastic Load Balancing (ELB) para distribuir o tráfego de entrada entre as instâncias dos contêineres, realizando verificações de saúde para garantir a disponibilidade dos serviços.

- Segurança:
   - Configurar grupos de segurança da AWS para limitar o acesso somente aos serviços e portas essenciais, assegurando a proteção do ambiente. Além disso, o IAM será configurado para gerenciar permissões e acesso aos recursos da AWS. Serão criados grupos de usuários e políticas de acesso que concedem o mínimo necessário para cada função e serviço na empresa.

- Resolução de Nomes e DNS (Amazon Route 53):
   - Utilizar o Amazon Route 53 para administrar o sistema de nomes e DNS da empresa. Isso envolve a resolução de nomes de domínio, a configuração de registros DNS, a organização de zonas hospedadas e a rota do tráfego de entrada para os serviços mantidos na AWS, garantindo alta disponibilidade e mínima latência.

### Valores:
A estimativa mensal para os custos dessa configuração é de aproximadamente 755.00 USD, e o custo anual é projetado em 9,070.00 USD (lembrando que os valores podem variar conforme a carga e a demanda).

### Cronograma de macro-integras:
- Prova de conceito (POC): A POC servirá para validar a arquitetura criada, expondo possíveis falhas e indicando possíveis mudanças antes de criarmos o MVP. Para a prova de conceito será necessário 3 dias e meio.
- Mínimo produto viável (MVP): Na MVP, teremos apenas os recursos mínimos, com suas funcionalidades básicas, sendo assim - uma versão enxuta do Produto final. Para a criação do Mínimo produto viável será necessário 3 dias e meio.
- Produto final: O produto final será a implementação da arquitetura apresentada. Para construir a arquitetura apresentada, será necessário aproximadamente uma semana.
