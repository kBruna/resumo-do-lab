# Notas do Módulo 1

## Benefícios da Nuvem Azure
### Domínio de Objetivo
 - Descrever os benefícios da segurança e da governança na nuvem
 - Descrever os benefícios da capacidade de gerenciamento na nuvem

### Benefícios
  - Alta disponibilidade:
    1. Está sempre disponível, recursos disponíveis sempre que necessário.
    2. Muito associado com a questão de SLA.
    3. Tempos de downtime tabelados, Azure lida com 99%, 99.9%, 99.95% e 99,99% de uptime. Cada faixa possui um valor. Caso esse tempo não seja fornecido, a Microsoft dá créditos para a conta/empresa.
    4. Serviço degradado: Serviço indisponível.
    5. A alta disponibilidade se concentra em garantir a disponibilidade máxima, independentemente de interrupções ou eventos que possam ocorrer.

## Benefícios da Nuvem: Escalabilidade e Elasticidade
Escalabilidade:
  - A escalabilidade refere-se á capacidade de ajustar recursos para atender á demanda.
  - A capacidade de escalar significa que você poderá adicionar mais recursos para lidar melhor com a demanda.
  - O outro benefício da escalabilidade é que você não está pagando além do necessário pelos serviços.
  - Como a nuvem é um modelo baseado em consumo, você paga apenas pelo que usa.
  - Se a demanda cair, você poderá reduzir seus recursos e, assim, reduzir seus custos.
  - Com a escala vertical, se você estivesse desenvolvendo um aplicativo e precisasse de mais capacidade de processamento, poderia escalar verticalmente para adicionar mais CPUs ou RAM á máquina virtual.

Elasticidade:
  - Com a elasticidade, se você experimentasse um salto repentino acentuado na demanda, seus recursos implantados poderiam ser expandidos (automaticamente ou manualmente).
  - Por exemplo, você pode adicionar máquinas virtuais ou containers por meio da expansão.
  - Da mesma forma, se houver uma queda significativa na demanda, os recursos implantados poderão ser reduzidos horizontalmente (de maneira automática ou manual).

## Benefícios da Nuvem: Confiabilidade, Previsibilidade e Segurança
Confiabiliade:
 - Resiliência - Um sistema que se recupera de falhas e continua funcionando
 - Devido ao design descentralizado, a nuvem naturalmente dá suporte a uma infraestrutura confiável e resiliente
 - Com um design descentralizado, a nuvem permite que você tenha recursos implantados em várias regiões do mundo
 - Com essa escala global, mesmo que ocorra um evento catastrófico em uma região, as outras regiões ainda estarão em funcionamento

Previsibilidade:
  - Confiança
  - A previsibilidade na nuvem permite que você avance com confiança, seja no desempenho ou no custo. Ambas são influenciadas pelo Microsoft Azure Well-Architected Framework

Segurança:
  - A nuvem oferece ferramentas de segurança que atendem ás necessidades dos clientes mas, é importante lembrar que a implementação de muitas delas devem ser realizadas pelo cliente
  - A segurança não é responsabilidade da Microsoft
  - Se você quiser o controle máximo da segurança, a infraestrutura como serviço fornecerá recursos físicos, mas permitirá que você gerencie os sistemas operacionais e o software instalado, incluindo aplicação de patches e manutenção
  - Se você quiser que a aplicação de patches e a manutenção sejam tratadas automaticamente, as implantações de plataforma como serviço ou softwares como serviço podem ser as melhores estratégias de nuvem para você

## Benefícios da Nuvem: Governança e Gerenciabilidade
Governança:
  - A auditoria baseada em nuvem ajuda a sinalizar qualquer recurso que esteja fora de conformidade com seus padrões corporativos e fornece estratégias de mitigação
  - Dependendo do seu modelo operacional, patches de software e atualizações também podem ser aplicados automaticamente, o que ajuda na governança e na segurança
  - Ao estabelecer uma presença de governança o mais cedo possível, você poderá manter sua presença de nuvem atualizada, protegida e bem gerenciada

Gerenciabilidade:
  - Um dos principais benefícios da computação em nuvem são as opções de capacidade de gerenciamento. Há dois tipos de capacidade de gerenciamento para computação em nuvem que você aprenderá nesta série e ambos trazem excelentes benefícios
  - O gerenciamento da nuvem diz respeito a gerenciar seus recursos de nuvem. Por exemplo: Escalar automaticamente a implantação de recursos com base na necessidade
  - Implantar recursos com base em um modelo pré-configurado, removendo a necessidade de configuração manual
  - O gerenciamento na nuvem diz respeito á maneira de gerenciar seus ambiente de nuvem e seus recursos. Por exemplo:
    1. Por meio de um portal da Web
    2. Usando uma interface de linha de comando
    3. Usando APIs
    4. Usando o PowerShell

## Tipos de Serviço de Nuvem na Azure
 - IaaS, PaaS e SaaS

### IaaS, PaaS e SaaS na Azure
 - IaaS - Infraestrutura como Serviço
   1. Recursos/Serviços que nós como clientes temos mais acesso.
   2. Manutenção é geralmente feita por nós(como cliente).
   3. Crie uma infraestrutura de TI de pagamento conforme o uso alugando servidores, máquinas virtuais, armazenamento, redes e sistemas operacionais de um provedor de nuvem.

 - PaaS - Plataforma como Serviço
   1. Um nível acima de IaaS
   2. Fornece um ambiente para a criação, o teste e a implantação de aplicativos de software, sem focar no gerenciamento da infraestrutura subjacente.

 - SaaS - Software as a Service
   1. Um nível acima de PaaS
   2. Os usuários se conectam e usam aplicativos com base em nuvem pela Internet: ex.: Microsoft Office 365, email e calendários
   3. Os níveis anteriores não é de responsabilidade do cliente
   
### Modelo de Responsabilidade Compartilhada

| Tipo de Responsabilidade | Responsabilidade | SaaS | PaaS | IaaS | No local |
|---|------------------|------|------|------|----------|
|A responsabilidade é sempre retida pelo cliente | Informações e dados | Cliente | Cliente | Cliente | Cliente |
| # | Dispositivos (móveis e PCs) | Cliente | Cliente | Cliente | Cliente |
| # | Contas e identidades | Cliente | Cliente | Cliente | Cliente |
|A responsabilidade varia conforme o tipo | Infraestrutura de identidade e diretório | Ambos | Ambos | Cliente | Cliente |
| # | Aplicativos | Microsoft | Ambos | Cliente | Cliente |
| # | Controles de Rede | Microsoft | Ambos | Cliente | Cliente |
| # | Sistema Operacional | Microsoft | Microsoft | Cliente | Cliente |
| Transferências de responsabilidade para provedores de nuvem | Hosts físicos | Microsoft | Microsoft | Microsoft | Cliente
| # | Rede Física | Microsoft | Microsoft | Microsoft | Cliente |
| # | Datacenter Físico |  Microsoft | Microsoft | Microsoft | Cliente |

### IaaS
 - O Serviço de nuvem mais flexível
 - Você configura e gerencia o hardware para seu aplicativo
 - Maior Gestão

### PaaS
 - Focado no desenvolvimento de aplicativos
 - O gerenciamento de plataforma é realizado pelo provedor de nuvem
 - Intermediário em termos de gestão

### SaaS
 - Modelo de preço de pagamento conforme o uso
 - Os usuários pagam pelo software que utilizam em um modelo de assinatura
 - Menor Gestão
