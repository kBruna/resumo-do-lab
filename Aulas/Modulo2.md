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

-----

# Computação e Rede

## Roteiro de Aprendizagem
Computação e Rede:
  - Tipos de computação
  - Hospedagem de aplicativos
  - Redes Virtuais
  - Comparar tipos de computação, incluindo instâncias de container, máquinas virtuais e funções
  - Descrever os recursos exigidos para as máquinas virtuais
  - Definir pontos de extremidade públicos e privados
  - Descrever as opções de máquina virtual, incluindo VMs (máquinas virtuais), conjuntos de dimensionamento de máquinas virtuais, conjuntos de disponibilidade de máquinas virtuais e a Área de Trabalho Virtual do Azure

## Serviços de Computação e Máquinas Virtuais do Azure
A Computação do Azure é um serviço sob demanda que fornece recursos de computação, como discos, processadores, memória, rede e sistemas operacionais.
  - Virtual - Virtuais
  - Aplicativo - Serviços
  - Contêiner - Instâncias
  - Serviços de Kubernetes do Azure (AKS)
  - Área de Trabalho Virtual do Azure

### Máquinas Virtuais do Azure
  - As máquinas virtuais do Azure (VMs) são emulações de software de computadores físicos
  - Inclui processador virtual, memória, armazenamento e rede
  - Oferta de IaaS que oferece personalização e controle total

#### Conjuntos de Dimensionamento de VMs
Os conjuntos de dimensionamento oferecem uma oportunidade de balanceamento de carga para dimensionar os recursos automaticamente.
  - Escalar horizontalmente quando o recurso precisar aumentar
  - Reduzir horizontalmente quando o recurso precisar diminuir

## Conjuntos de Disponibilidade de Máquinas Virtuais do Azure
  - Dominio de falha: o rack em si
  - Dominio de atualização (horizontal entre racks)
  - Não existe custo adicional, paga-se apenas pelas instâncias

## Área de Trabalho Virtual e Containers do Azure
A Área de Trabalho Virtual do Azure é uma virtualização de área de trabalho e aplicativo executada na nuvem.
  - Crie um ambiente completo de virtualização da área de trabalho sem precisar executar outros servidores de gateway
  - Reduza o risco de que o recurso seja deixado para trás
  - Implantações reais de várias sessões

### Serviços de containers do Azure
Os containers do Azure fornecem um ambiente leve e virtualizado que não exige o gerenciamento do sistema operacional e pode responder a alterações sob demanda.
  - Consome recursos de uma forma mais silenciosa que uma área de trabalho virtual.
  - Projetado para atender uma computação sob-demanda
  - Docker é um exemplo de contêiner
  - Não necessita de um SO a parte

Instâncias de Contêiner do Azure: uma oferta de PaaS que executa um contêiner ou pod de contêineres no Azure.

Aplicativos de Contêiner do Azure: uma oferta de PaaS, como instâncias de contêineres, que pode balancear a carga e escalar. (Remove a parte de gerenciamento de contêiners) 

Serviço de Kubernetes do Azure: um serviço de orquestração para contêineres com arquiteturas distribuídas e grandes volumes de contêineres. Orquestracão = organizar o ciclo de vida dos contêineres.

## Azure Functions e Serviços de Aplicativo do Azure
Azure Functions: uma oferta de Paas que dá suporte a operações de computação sem servidor.
O código baseado em eventos é executado quando chamado, sem exigir uma infraestrutura de servidor durante períodos inativos. Automatização de atividades engatilhada para realizar uma atividade como "reação" a algo que aconteça.

### Comparar opções de computação do Azure

#### Máquinas virtuais
  - Servidor baseado em nuvem que dá suporte a ambientes Windows ou Linux.
  - Útil para migrações de lift-and-shift para a nuvem.
  - Pacote do sistema operacional completo, incluindo o sistema operacional do host.

#### Área de Trabalho Virtual
  - Fornece uma experiência de área de trabalho do Windows baseada em nuvem.
  - Aplicativos dedicados para conexão e uso ou acessíveis de qualquer navegador moderno.
  - O logon de vários clientes permite que vários usuários façam logon no mesmo computador ao mesmo tempo.

#### Contêineres
  - Ambiente leve e em miniatura adequado para a execução de microsserviços.
  - Projetado para escalabilidade e resiliência por meio da orquestração.
  - Os aplicativos e serviços são empacotados em um contêiner que fica na parte superior do sistema operacional do host. Vários contêiners podem ficar em um sistema operacional do host.

### Serviços de Aplicativo do Azure
Os Serviços de Aplicativos do Azure consistem em uma plataforma totalmente gerenciada para criar, implantar e dimensionar aplicativos Web e APIs rapidamente.
  - Trabalha com .NET, .NET Core, Node.js, Java, Python ou php.
  - Oferta de PaaS com requisitos de nível corporativo de desempenho, segurança e conformidade.

### Serviços de rede do Azure
A Rede Virtual do Azure (VNet) permite que os recursos do Azure se comuniquem uns com os outros, com a Internet e com as redes locais.
Pontos de extremidade públicos, acessíveis de qualquer lugar na Internet.
Pontos de extremidade privados, acessíveis somente dentro da sua rede.
As sub-redes virtuais segmentam sua rede para atender às suas necessidades.
O emparelhamento de rede conecta suas redes privadas diretamente.

#### Gateway de VPN
O Gateway de VPN é usado para enviar tráfego criptografado entre uma rede virtual do Azure e uma no local pela Internet pública.

#### ExpressRoute
O ExpressRoute estende as redes locais para o Azure por meio de uma conexão privada facilidade por um provedor de conectividade.

### DNS do Azure
  - Confiabilidade e desempenho aproveitando uma rede global de servidores de nome DNS usando a rede Anycast.
  - A segurança do DNS do Azure baseia-se no gerenciador de recursos do Azure, habilitando o controle de acesso baseado em função e o monitoramento e o registro do log.
  - Facilidade de uso para gerenciar seus recursos externos e do Azure com um único serviço DNS.
  - As redes virtuais personalizáveis permitem que você use nomes de domínio privados e totalmente personalizados em suas redes virtuais privadas.
  - Os registros de alias dão suporte a conjuntos de registros de alias para apontar diretamente para um recurso do Azure.

### Laboratório
  - Máquina Virtual do Azure:
      1. Assinatura e Grupo de Recursos
      2. Nome da máquina
      3. Região (Já aparece uma região padrão)
      4. Opções de Disponibilidade: Conjunto de Dimensionamento de máquinas virtuais
      5. Conjunto de Dimensionamento de Máquinas Virtuais: Criar novo
      6. Modo de Dimensionamento: Dimensionamento Automático
      7. Excluir com VM: Evitar Discos Órfãos.
      8. Interface de Rede: Rede Virtual é criado uma caso não exista. Precisam estar na mesma região.
      9. Selecione portas de entradas: Selecionar quais IPs conseguem acessar a MV.
      10. Excluir o IP público e a NIC quando a VM for excluida.
      11. Desligamento Automático: Pode ser ajustado horário e notificações para o usuário.
      12. Habilitar Backup
    - Área Virtual do Azure:
      1. Host Pessoal: Individual/Utilização Específica.
      2. Host Pool: Pode ser utilizado por vários usuários.
    - Aplicativos de Função:
      1.  Código ou Contêiner
      2.  Pilha de Runtime: Linguagem de programação, o Sistema Operacional será selecionado automaticamente.
