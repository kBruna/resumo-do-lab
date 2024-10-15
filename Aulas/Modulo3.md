# Módulo 3 - Gerenciamento e Governança
## Roteiro de Aprendizagem
Gerenciamento de Custos
  - Calculadora de custos e preços
  - Gerenciamento de custos e marcas (Tags)

# Gerenciamento de Custos no Azure
## Fatores que afetam os Custos
Computação em nuvem: Domínio do objetivo
  - Descrever fatores que podem afetar os custos no Azure
  - Compare a calculadora de preços e a calculadora de custo total de propriedade (TCO)
  - Descreva a Ferramenta de Gerenciamento de Custos do Azure
  - Descrever a finalidade das marcas (Tags)

**Fatores que afetam os custos:**
Estes são fatores que afetam os custos:
  **1. Tipo de recurso:** Os custos são específicos do recurso, portanto, o uso que um medidor rastreia e o número de medidores associados a um recurso, dependendo do tipo de recurso.
  
  **2. Consumo:** Com um modelo pago conforme o uso, o consumo é um dos maiores geradores de custos.
  
  **3. Manutenção:** Monitorar seu volume do Azure e manter seu ambiente pode ajudá-lo a identificar e reduzir os custos que não são necessários, como ao desligar máquinas virtuais subutilizadas.

  **4. Área Geográfica:** O mesmo tipo de recurso pode custar valores diferentes dependendo da área geográfica, o que afeta os custos do Azure.

  **5. Tráfego de Rede:** Embora algumas transferências de dados de entrada sejam gratuitas, o custo de dados de saída ou dados entre recursos do Azure é afetado por zonas de cobrança.

  **6. Assinatura:** O tipo e a configuração da assinatura também podem afetar o custo. Por exemplo, a avaliação gratuita permite explorar alguns recursos do Azure gratuitamente.

**Explorar o Azure Marketplace:**
  O **Azure Marketplace** permite que os clientes encontrem, experimentem, comprem e provisionem aplicativos e serviços de centenas de provedores de serviços líderes, que são todos certificados para execução no Azure.
      - Software de compilação e implantação de aplicativos;
      - Ferramentas para Desenvolvedores;
      - E muito mais, com mais de 10.000 itens listados.
      - Recursos criados a partir deste marketplace, que não é nativo do Microsoft, necessita que você entre em contato com o fabricante, em caso de problemas técnicos.

## Calculadora de Preços:
  - Sempre trás uma estimativa de preço, não o valor real.
  A **calculadora de preços** é uma ferramenta que ajuda a estimar o custo dos produtos do Azure.
  As opcões que você pode configurar na calculadora de preços variam entre os produtos, mas as opções básicas de configuração incluem:
  - Região;
  - Camada;
  - Opções de cobrança;
  - Opções de suporte;
  - Programas e ofertas;
  - Preço de Desenvolvimento/Teste do Azure.

**Calculadora de Custo Total de Propriedade (TCO)**
  - Uma ferramenta para estimar a economia de custos possível ao migrar para o Azure.
  - Um relatório compara os custos das infraestruturas locais com os custos de uso de produtos e serviços do Azure na nuvem.

**Gerenciamento de Custos do Azure**
  - Relatório: Relatórios de cobrança
  - Enriquecimento de dados
  - Orçamentos: Definir orçamento de gastos
  - Alertas: Quando o custo excede os limites
  - Recomendação: Recomendações de custo

## Marcas (Tags) no Azure
  - Fornecem metadados aos recursos do Azure
  - **Não são obrigatórias e não são herdáveis**
  - Organizam os recursos em uma taxonomia de maneira lógica
  - Consistem em um par nome-valor
  - Muito úteis para reunir informações de cobrança
  - Ajuda a filtrar o custo na fatura

Video 5 - Gerenciamento de Custos - Revisão -> Vídeo duplicado de Marcas (Tags)

## Laboratório
**Gerenciamento de custos:**
  - Calculadora do TCO (Custo Total de Propriedade)
    1. Definir Suas Cargas de Trabalho:
       - Servidores;
       - Banco de Dados;
       - Armazenamento;
       - Redes.
    2. Ajustar Suposições:
       - Cobertura do Software Assurance (fornece Benefício Híbrido do Azure)
    3. Exibir relatório:
       - Exibe um gráfico comparativo da configuração on-premisse e cloud Azure.
  - Calculadora Microsoft:
    1. Portal Oficial para Orçamentos;
    2. Acesso para Empresas, possibilita a visualização de descontos específicos;
    3. Produtos -> Possibilita fazer simulações
  - Azure: Cost Management + Billing:
    1. Permite a visualização de custos e gerenciamento de alertas;
    2. Possui um Advisor que recomenda sugestões de melhorias relacionada a custos;
  - Azure: Marcas (Tags):
    1. Dupla Chave:Valor;
    2. Não é um pré-requisito pra nada;
    3. A Tag não é herdável;
    4. Policy: Permite criar políticas para padronizar e "forçar" o uso das Tags.
   
-------------------







