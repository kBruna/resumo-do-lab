# Modulo 2: Arquitetura e serviços do Azure

##Roteiro de Aprendizagem
- Componentes de arquitetura do Azure
  1. Regiões e zonas de disponibilidade
  2. Assinaturas e grupos de recursos

## Componentes de Arquitetura do Azure

Principais componentes arquitetônicos do Azure
  - Descrever os recursos e os grupos de recursos do Azure
  - Descrever as assinaturas
  - Descrever os grupos de gerenciamento
  - Descrever a hierarquia de grupos de recursos, assinaturas e grupos de gerenciamento.

## Contas do Azure
  - Conta do Azure
  - Conta gratuita do Azure
  - Conta de estudante gratuita do Azure
  - Área restrita do Microsoft Learn

## Regiões
  - Existem recursos que não estão disponíveis para todas as regiões
  - General Availability (Recurso liberado para a maioria das regiões).
  - O Azure oferece mais regiões globais do que qualquer outro provedor de nuvem, com mais de 60 regiões representando mais de 140 países.
  - As regiões são compostas de um ou mais datacenters muito próximos (3 datacenters por região)
  - Eles fornecem flexibilidade e escala para reduzir a latência do cliente
  - As regiões preservam a residência dos dados com uma oferta abrangente de conformidade
  - Backbone da Microsoft (uma exclusiva da Microsoft que garante a comunicação entre datacenters)
  - Disaster Recovery - Ter uma réplica de recursos essenciais em outra região, para que quando meu ambiente fique fora, eu consiga ativar esses recursos em outra região.

### Zonas de Disponibilidade
  - Fornece proteção contra tempo de inatividade devido a falha do datacenter
  - Separe fisicamente os datacenters dentro da mesma região
  - Cada datacenter é equipado com alimentação, resfriamento e rede independentes
  - Conectadas por meio de redes privadas de fibra óptica

### Pares de Regiões
  - No mínimo 300 milhas de separação entre pares de regiões
  - Replicação automática para alguns serviços
  - Recuperação de região priorizada em caso de interrupção
  - As atualizações são distribuídas sequencialmente para minimizar o tempo de inatividade
  - Em muitos casos, o sistema fica indisponível até que o Par fique configurado corretamente

### Regiões soberanas do Azure

#### Serviços Governamentais dos EUA - Azure Governamental
Atende às necessidades de segurança e conformidade das agências federais, governos estaduais e locais dos EUA e seus provedores de soluções
  - Instância separada do Azure
  - Fisicamente isolada de implantações que não sejam do governo dos EUA
  - Acessível somente a pessoal verificado e autorizado

#### Azure China
A Microsoft é o primeiro provedor estrangeiro de serviços de nuvem pública da China, em conformidade com as regulamentações governamentais
  Recursos do Azure China:
  - Instância fisicamente separada dos serviços de nuvem do Azure operados pela 21Vianet
  - Todos os dados permanecem dentro da China para garantir a conformidade

### Recursos do Azure
  - Os recursos do Azure são componentes como armazenamento, máquinas virtuais e redes que estão disponíveis para criar soluções de nuvem
  - Máquinas virtuais, Contas de armazenamento, Redes virtuais, Serviços de Aplicativos, Banco de Dados SQL, Funções.

#### Grupos de Recursos
  - Grupo de recursos (Web mais BD, VM, Armazenamento) em um grupo OU
  - Grupo de recursos de Web e Banco de Dados
  - Grupo de recursos de máquina virtual
  - Grupo de recursos de armazenamento
  - Não é possível Renomear um Grupo de Recursos (Resource Group)
  - Não é necessário que estejam na mesma região
  - Um grupo de Recursos é um container que você usa para gerenciar e agregar recursos em uma única unidade
  - Os recursos podem existir em apenas um grupo de recursos
  - Os recursos podem existir em diferentes regiões
  - Os recursos podem ser movidos para diferentes grupos de recursos
  - Os aplicativos podem utilizar vários grupos de recursos

### Assinaturas do Azure
  - Conta do Azure
    1. Assinatura do desenvolvimento
    2. Assinatura do teste
    3. Assinatura da produção
  - Uma conta pode ter diversas assinaturas, mas uma assinatura está associada a apenas uma conta.
  - Uma das estratégias para gerenciamento de contas é que cada grupo de trabalho seja criado uma assinatura diferente
  - Uma assinatura do Azure fornece a você acesso autenticado e autorizado às contas do Azure
  - Limite de cobrança: Gere relatórios de cobrança e faturas separadas para cada assinatura
  - Limite do controle de acesso: Gerenciar e controlar o acesso aos recursos que os usuários podem provisionar com assinaturas específicas

### Grupos de Gerenciamento
  - Organização, também relacionado a Segurança
  - Os grupos de gerenciamento podem incluir várias assinaturas do Azure
  - As assinaturas herdam as condições aplicadas ao grupo de gerenciamento

## Componentes de arquitetura do Azure
  - Criar Grupo de Recursos no Azure
  - East US 2
  - Nome : Valor = Não é obrigatório, mas possui várias funcionalidades. Marcações/Tags = Subtítulo para Descrever melhor o recurso
  - IAM (Controle de acesso)

## Atividades
  - Criar uma conta gratuíta no Microsoft Azure ✅
  - Criar um Resource Group ✅
  - Criar uma Rede Virtual ✅
