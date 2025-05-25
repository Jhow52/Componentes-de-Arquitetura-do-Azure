# 🏗️ Componentes de Arquitetura do Azure

## 🌍 Regiões, Pares de Regiões e Regiões Soberanas

- **Regiões**: São locais geográficos que contêm um ou mais datacenters. O Azure possui mais de 60 regiões no mundo. Ao criar um recurso, é necessário escolher uma região.
- **Pares de regiões**: São duas regiões do mesmo continente separadas por no mínimo 300 milhas, com suporte a replicação automática e recuperação prioritária.
- **Regiões soberanas**: Regiões dedicadas para governos com requisitos especiais, como o **Azure Governamental** dos EUA.

## 🏢 Zonas de Disponibilidade

- São datacenters separados fisicamente dentro da mesma região.
- Oferecem alta disponibilidade, com energia, resfriamento e rede independentes.
- Garantem que aplicações críticas continuem funcionando mesmo em caso de falha em um datacenter.

## 🧩 Datacenters do Azure

- Infraestrutura física onde os recursos de nuvem operam.
- Distribuídos globalmente, interligados por redes de alta velocidade.
- Projetados para alta disponibilidade, segurança e escalabilidade.

## 📦 Recursos e Grupos de Recursos

- **Recursos**: Componentes individuais como VMs, bancos de dados, redes, etc.
- **Grupos de recursos**: Contêineres lógicos que agrupam e organizam recursos relacionados.
  - Um recurso pertence a **apenas um grupo de recursos**.
  - Os grupos facilitam o gerenciamento, monitoramento e controle de acesso.

## 🔐 Assinaturas e Grupos de Gerenciamento

- **Assinaturas**: Ligam uma conta a um conjunto de recursos e definem limites de cobrança e controle de acesso.
  - Uma conta pode ter várias assinaturas.
- **Grupos de gerenciamento**: Organizam múltiplas assinaturas.
  - Permitem aplicar políticas e controles hierárquicos.
  - Assinaturas herdam configurações do grupo de gerenciamento.
 
## 🛠️ Passo a Passo: Criando uma Arquitetura no Azure

### 1. 📌 Defina os Objetivos do Projeto
- Qual é o propósito da solução (web app, banco de dados, rede corporativa, etc)?
- Qual o nível de disponibilidade, escalabilidade e segurança esperado?

### 2. 🌍 Escolha a Região
- Escolha a **região do Azure** mais próxima dos seus usuários ou da sua organização.
- Verifique a disponibilidade dos serviços desejados na região.

### 3. 🧱 Planeje os Recursos
- Defina os principais **recursos que serão utilizados**:
  - Máquinas Virtuais (VMs)
  - Banco de Dados (SQL Database, Cosmos DB)
  - Armazenamento (Blob Storage, Files)
  - Redes Virtuais (VNet, Subnets)
  - Serviços gerenciados (App Service, Functions, etc.)

### 4. 📦 Organize com Grupos de Recursos
- Crie **grupos de recursos** lógicos para organizar os serviços por função, projeto ou ambiente (produção, homologação, dev).

### 5. 🔒 Configure Assinaturas e Controle de Acesso
- Utilize **assinaturas** separadas por equipe, cliente ou ambiente, se necessário.
- Aplique **RBAC (controle baseado em função)** para definir quem pode acessar e o que pode fazer.

### 6. ⚙️ Configure a Rede e Segurança
- Crie a **rede virtual (VNet)** com sub-redes adequadas.
- Adicione **NSGs (grupos de segurança de rede)**, **firewalls** e **VPNs** para proteger o ambiente.
- Use o **Azure Key Vault** para armazenar segredos e certificados.

### 7. 📈 Configure Escalabilidade e Alta Disponibilidade
- Utilize **Zonas de Disponibilidade** e **instâncias com balanceamento de carga**.
- Configure **Auto Scaling** para ajustar os recursos automaticamente conforme a demanda.

### 8. 🧩 Automatize e Padronize com Templates
- Use **Azure Resource Manager (ARM)** ou **Bicep** para criar templates de implantação.
- Configure **tags** para rastrear custos e finalidade de cada recurso.

### 9. 📝 Monitore e Gerencie
- Habilite **Azure Monitor** e **Log Analytics** para métricas e logs.
- Configure **alerts**, **dashboards** e **backup automatizado**.
