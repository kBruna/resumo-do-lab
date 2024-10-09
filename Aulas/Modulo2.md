# Modulo 2: Arquitetura e serviços do Azure

## Roteiro de Aprendizagem
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

---------------

## Armazenamento
### Roteiro de Aprendizagem
  - Serviços de Armazenamento
  - Opções de redundância
  - Gerenciamento e migração de arquivos 
  - Comparar os serviços de armazenamento do Azure
  - Descrever as camadas de armazenamento
  - Descrever as opções de redundância
  - Descrever as opções de conta de armazenamento e os tipos de armazenamento
  - Identificar opções para mover arquivos, incluindo o AzCopy, o Gerenciados de Armazenamento do Azure e a Sincronização de Arquivos do Azure
  - Descrever as opções de migração, incluindo as Migrações para Azure e o Azure Data Box

### Contas de Armazenamento
  - Deve ter um nome globalmente exclusivo
  - Fornecer acesso à Internet em todo o mundo
  - Determinar os serviços de armazenamento e as opções de redundância

### Redundância de Armazenamento
|Configuração de Redundância | Implantação | Durabilidade |
|----------------------------|-------------|--------------|
|LRS (Armazenamento com redundância local) | Datacenter individual na região primária | 11 Noves |
| ZLS (Armazenamento com redundância de zona) | Três zonas de disponibilidade na região primária | 12 Noves |
| GRS (Armazenamento com redundância geográfica) | Datacenter único no primário e região secundária | 16 Noves |
| GZRS (Armazenamento com redundância de zona geográfica) | Três zonas de disponilidade na região primária e um único datacenter na região secundária | 16 Noves |

## Redundância e Serviços de Armazenamento

**Serviços de armazenamento do Azure:**
  - **Blob do Azure:** Otimizado para o armazenamento de quantidades massivas de dados não estruturados, como texto ou dados binários.
  - **Disco do Azure:** Fornece discos para máquinas virtuais, aplicativos e outros serviços acessarem e utilizarem.
  - **Fila do Azure:** Serviço de armazenamento de mensagens que fornece armazenamento e recuperação para grandes quantidades de mensagens, cada uma com até 64 KB.
  - **Arquivos do Azure:** Configura um compartilhamento de arquivos de rede altamente disponível que pode ser utilizado usando o protocolo Bloco de Mensagens do Servidor.
  - **Tabelas do Azure:** Fornece uma opção de chave/atributo para o armazenamento de dados estruturados não relacionais com um design sem esquema.

## Pontos de Extremidades Públicos e Camadas de Acesso
|Serviço de Armazenamento | Ponto de Extremidade Público |
|-------------------------|------------------------------|
|Armazenamento de Blobs | `https://<storage-account-name>.blob.core.windows.net` |
|Data Lake Storage Gen2 | `https://<storage-account-name>.dfs.core.windows.net` |
|Arquivos do Azure | `https://<storage-account-name>.file.core.windows.net` |
|Armazenamento de filas | `https://<storage-account-name>.queue.core.windows.net` |
|Armazenamento de Tabelas | `https://<storage-account-name>.table.core.windows.net` |

*Via de regra, o primeiro nome é sempre o nome do recurso.*

**Camadas de Acesso de Armazenamento do Azure**
|Frequente | Esporádico | Frio | Arquivo Morto |
|----------|------------|------|---------------|
|Otimizada para armazenamento de dados acessados com frequência. | Otimizada para armazenamento de dados acessados com pouca frequência e armazenados por pelo menos 30 dias. | Otimizado para o armazenamento de dados acessados com pouca frequência e armazenados por pelo menos 90 dias. | Otimizada para armazenamento de dados acessados raramente e armazenados por pelo menos 180 dias com requisitos de latência flexíveis. |

## Migrações para o Azure
  - Plataforma de migração unificada
  - Intervalo de ferramentas integradas e autônomas
  - Avaliação e migração
  - **Azure Data Box:** Até 80 Terabytes de dados de uma só vez.
    1. Armazenar até 80 terabytes de dados.
    2. Mova os backups de recuperação de desastre para o Azure
    3. Proteja seus dados em uma caixa robusta durante o trânsito
    4. Migre dados do Azure para conformidade ou necessidades regulatórias
    5. Migre dados para o Azure de locais remotos com conectividade limitada ou sem conectividade

## Opções de Gerenciamento de Arquivos
### AzCopy
  - Utilitário de linha de comando
  - Copiar blobs ou arquivos de/para sua conta de armazenamento
  - Sincronização em uma direção

### Gerenciador de Armazenamento do Azure
  - Interface gráfica do usuário (de modo semelhante ao Windows Explorer)
  - Compatível com o Windows, MacOS e Linux

### Sincronização de Arquivos do Azure
  - Sincroniza os arquivos do Azure e locais de forma bidirecional
  - A camada de nuvem mantém os arquivos acessados com frequência no local, enquanto libera espaço

## Laboratório
Contas de Armazenamento:
  - Criação
    1. Assinatura: Automático
    2. Grupo de Recursos
    3. Nome exclusivo na Terra: 3 a 24 caracteres minusculos e números
    4. Região
    5. Desempenho: Standard (Uso Geral) ou Premium (Mais caro, para cenários que exigem baixa latência)
    6. Redundância: LRS / GRS / ZRS / GZRS
    7. Armazenamento de Blobs: Quente / Frio
  - Novo compartilhamento de Arquivos:
    1. Nome
    2. Camada: Transação Otimizada / Quente / Frio
    3. Backup
  - Conectar:
    1. Letra de Unidade
    2. Método de autenticação: Active Directoru ou Microsoft Entra / Chave de conta de armazenamento
    3. Script: Pode ser gerado para Windows / Linux / MacOS
    4. Conexão: Porta TCP 445, Protocolo SMB
  - Migração para o Azure:
    1. Explorar mais cenários
    2. Criar projeto
    3. Detalhes do projeto: Nome
    4. Detalhes do projeto: Geografia
    5. Avançado: Método de conectividade: Ponto de extremidade público
    6. Criar
  - AzCopy (Unidirecional):
    1. Funciona para outros sistemas operacionais
    2. Necessita ter um Storage Account
    3. Criar um contêiner
    4. Tokens de acesso compartilhado: Permissões (Todos)
    5. Gerar tokens SAS: Copiar URL SAS do blob
    6. Pelo Prompt de Comando: Dentro da pasta do AzCopy `azcopy copy "/path/to/dir" https://[account].blob.core.windows.net/[container]/[path/to/directory]?[SAS]" --recursive=true`
    7. Arquivos serão copiados para dentro do contêiner do Azure
  - Gerenciador de Armazenamento do Microsoft (Storage Explorer):
    1. Funciona para outros sistemas operacionais
    2. Baixar e instalar
    3. Selecionar um Ambiente do Azure
    4. Assinatura: Selecionar Azure
    5. Autenticar no navegador

-------------

## Identidade, Acesso e Segurança

### Identidade, Acesso e Segurança
#### Roteiro de Aprendizagem
  - Serviços de diretório
  - Métodos de autenticação
  - Modelos de segurança

#### Identidade, acesso e segurança: Domínio de Objetivo
  - Descrever os serviços de diretório no Azure, incluindo o Microsoft Entra ID e o Microsoft Entra Domain Services
  - Descrever métodos de autenticação no Azure, incluindo SSO (logon único), MFA (autenticação multifator) e sem senha
  - Descrever as identidades externas e o acesso de convidado no Azure
  - Descrever o Acesso Condicional do Entra
  - Descrever o controle de acesso baseado em função (RBAC)
  - Descrever o conceito de Confiança Zero (Confiar Desconfiando)
  - Descrever a finalidade do modelo de defesa em profundidade (Modelo Cebola - proteção em camadas)
  - Descrever a finalidade do Microsoft Defender para Nuvem (Cloud Native - Totalmente personalizável)

### Microsoft Entra ID e Domain Services
#### ID do Microsoft Entra
O Microsoft Entra ID é o serviço de gerenciamento de identidades e acesso baseado em nuvem do Microsoft Azure.
  - Autenticação (os funcionários entram para acessar os recursos)
  - Login único (SSO)
  - Gerenciamento de aplicativos
  - Negócios para Negócios (B2B)
  - Gerenciamento de dispositivos

**Microsoft Entra Domain Services**
  - Obtenha os benefícios dos serviços de domínio baseados em nuvem sem gerenciar os controladores de domínio
  - Execute aplicativos herdados (que não podem utilizar os padrões de autenticação modernos) na nuvem
  - Sincronizar automaticamente a partir do Microsoft Entra ID

### Autenticação e Autorização
#### Comparar a Autenticação e a Autorização
**Autenticação:**
  - Identifica a pessoa ou serviço buscando acesso a um recurso
  - Solicita credenciais de acesso legítimo
  - Base para criar princípios de identidade e controle de acesso seguros

**Autorização:**
  - Determina o nível de acesso de uma pessoa ou serviço autenticado
  - Define quais dados eles podem acessar e o que podem fazer com eles

**Autenticação multifator:**
Fornece segurança adicional para as identidades, exigindo dois ou mais elementos para autenticação completa.

Algo que você sabe <-> Algo que você possui <-> Algo que você é

#### B2B do Microsoft Entra External ID
(Parceiros, fornecedores, outros colaboradores) -> Convite ou inscrição para autoatendimento -> ID externa do Microsoft Entra

#### B2C do Identidades Externas do Azure AD
Azure AD B2C
(Consumidores do seu aplicativo publicado) -> Fluxos dos usuários de inscrição e entrada, políticas personalizadas -> Azure AD B2C (Seu locatário do Azure AD B2C)

### Acesso Condicional
  - Associação de usuário ou grupo
  - Local do IP
  - Dispositivo
  - Aplicativo
  - Detecção de risco

#### Controle de aceso baseado em função (Role Based Access Control - RBAC)
  - Gerenciamento de acesso de granularidade fina (Acesso de acordo com a necessidade)
  - Divida as tarefas dentro da equipe e conceda somente a quantidade de acesso de que os usuários precisam para trabalhar (Somente naquilo que faz sentido)
  - Habilite o acesso ao portal do Azure e o controle de acesso aos recursos

#### Confiança Zero
  - Modelo que pressupõe sempre o pior cenário
  - Proteja os ativos onde eles estiverem com a Confiança Zero
  - Proteção completa:
    1. Segurança física: Proteger o datacenter
    2. Identidade e acesso: Acessos e Usuários
    3. Perímetro: Por exemplo: Ataque de DDOS
    4. Rede: Garantir a segmentação e a limitação de comunicações entre as redes reais
    5. Computação: Máquinas Virtuais
    6. Aplicativo: Tanto aplicações quanto da cloud, se elas estão livres de vulnerabilidades
    7. Dados: Controla todo o acesso dos dados corporativos e dos clientes, se for o caso
  - Uma abordagem em camadas para proteger sistemas de computador
  - Fornece vários níveis de proteção
  - Ataques contra uma camada são isolados das camadas subsequentes

#### Microsoft Defender para Nuvem
  - O Microsoft Defender para Nuvem é um serviço de monitoramento que fornece proteção contra ameaças nos datacenters do Azure e locais.
  - Também faz a comunicação para o ambiente da AWS e do GCP.
  - Tráz estratégias de remediação e correção dos problemas que ele identifica.
  - Trial - 30 dias de versão para validação
  - É possível ativar determinadas camadas apenas, para o que faz sentido para o sistema

#### Recursos do Azure
  - Fornece recomendações de segurança
  - Detectar e bloquear malware
  - Analisar e identificar ataques potenciais
  - Controle de acesso just-in-time para portas

### Laboratório
  - Microsoft Entra ID (Antigo Microsoft Active Directory): (Para as mesmas autenticações na Cloud e no On-Premise: Sincronização de contas do on-Premise -> Cloud. O processo inverso não ocorre.)
    1. Roles and administrators: Este permissionamento está relacionado com a conta de outra pessoa. Se atentar com as diferenças com o RBAC.
    2. Users: Users are permanently deleted automatically 30 days after they are deleted.
    3. Self-service Password Reset
    4. Possibilidade de criar um usuário novo ou convidar um externo
    5. Opções de convites em grande escala (bulk invite)
    6. Permissionamento é herdável
    7. É possível dar permissão direto no serviço
  - Microsoft Defender for Cloud:
    1. "Termômetro"
    2. Análise de postura de segurança dizendo o quão bom ou ruim estamos.
    3. Cloud Native
    4. Algumas funcionalidades chave liberadas
    5. Funciona para outras Cloud Providers
    6. DevOps Security: É possível conectar a conta do AzureDevOps, GitHub e GitLab. E realiza a validação das ações.
