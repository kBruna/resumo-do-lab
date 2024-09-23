# resumo-do-lab
Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO.

# Introdução

## Objetivo Geral
Este curso oferece um nível de conhecimento básico sobre:
  - Conceito do Azure
  - Principais serviços do Azure
  - Principais soluções e ferramentas de gerenciamento, segurança geral e segurança de rede
  - Governança, privacidade e recursos de conformidade e gerenciamento de custo do Azure

## Roteiro de Aprendizagem
Computação em nuvem:
  - O que é computação em nuvem
  - Responsabilidade compartilhada
  - Modos de nuvem
  - Custos de capital versos custo operacional

## Computação em nuvem: Domínio do objetivo
O que é computação em nuvem?

Computação em nuvem é o fornecimento de serviços de computação pela internet, habilitando inovações mais rápidas, recursos flexíveis e economias de escala.

### Nuvem privada
  - 100% on premisse. Local e exclusivo da empresa.
  - As organizações criam um ambiente em nuvem em seu datacenter.
  - As organizações são responsáveis por operar os serviços que oferecem.
  - Não fornecem acesso aos usuários fora da organização.

### Nuvem pública
  - Pertencente a serviços de nuvem ou provedor de hosting.
  - Fornece recursos e serviços a várias organizações e usuários.
  - Acessada via conexão de rede segura (geralmente pela Internet).

### Nuvem híbrida
  - "Melhor dos dois mundos"
  - Combina nuvens públicas e privadas para permitir que os aplicativos sejam executados no local mais adequado.

### Modelo Multi-Cloud
  - Trabalhar em paralelo com múltiplos domínios de cloud (On-Premisse, Azure, AWS, etc)

## Comparação
### Nuvem pública:
  - Nenhuma despesa de capital para escalar verticalmente.
  - Os aplicativos podem ser provisionados e desprovidos rapidamente.
  - As organizações pagam apenas pelo que utilizam (Pay-as-you-go).

### Nuvem privada:
  - As organizações têm controle total sobre os recursos e a segurança.
  - As organizações são responsáveis pela manutenção e pelas atualizações de software.

### Nuvem híbrida:
  - As organizações têm controle total sobre os recursos e a segurança.
  - As organizações controlam a segurança, a conformidade e os requesitos legais.
  - Fornece maior flexibilidade.

## Comparar CapEx e OpEx
### Despesas de capital (CapEx)
  - O gasto inicial de dinheiro  em infraestrutura física
  - As despesas de CapEx têm um valor que se reduz com o tempo

### Despesas Operacionais (OpEx)
  - Gastar com produtos e serviços conforme necessário, pagamento conforme o uso.
  - Seja cobrado imediatamente.

## Modelo baseado no consumo
  Os provedores de serviços em nuvem operam em um modelo baseado no consumo, o que significa que os usuários finais pagam somente pelos recursos que usam.
  - Melhor previsão de custos
  - São fornecidos preços para recursos e serviços individuais
  - A cobrança é feita com base no seu uso real.

# Aula 1 - Localizando serviços por Categoria

### Resumo dos recursos disponíveis
  - Poucas diferenças de ferramentas disponíveis na conta Trial
  - Limitação de ferramentas em algumas regiões
  - Limitação de ferramentas mais custosas

### Overview sobre a interface do Microsoft Azure
  - Opções para mudar a barra lateral
  - Opções de cores/modo noturno
  - Opções de troca de região e idioma

### Categorias
  - Lista de todos os serviços por categorias:
  - Bastions: Rede segura para fazer o acesso as suas máquinas, funciona como um Jumpserver.
  - Jumpserver: Um servidor que é usado como ponte para conectar outras máquinas.
  - Lembrete: Quando estamos falando de nuvem, é seu ambiente On-Premisse meio virtualizado.
  - Peering: Emparelhamento de rede.
  - Versão Prévia: Início da disponibilização de um serviço. Pode ser descontinuado a qualquer momento. Não tem SLA. Se usa por sua conta e risco.
  - SLA - Service Level Agreement: Acordo de nível de serviço, ou garantia.
