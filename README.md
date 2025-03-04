# resumo-do-lab
Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO

### Benefícios da Nuvem Azure

- **Alta Disponibilidade**: Garantia de máxima disponibilidade, mesmo durante interrupções ou eventos inesperados.

- **Escalabilidade**: Capacidade de ajustar recursos conforme a demanda. Você paga apenas pelo que usa, podendo aumentar ou diminuir recursos conforme necessário, evitando custos excessivos.

- **Elasticidade**: Permite expandir ou reduzir recursos rapidamente (automaticamente ou manualmente) conforme variações na demanda.

- **Confiabilidade**: Infraestrutura resiliente e descentralizada, com recursos distribuídos globalmente, garantindo continuidade mesmo durante eventos catastróficos.

- **Previsibilidade**: Fornece confiança quanto ao desempenho e custos, com base no Microsoft Azure Well-Architected Framework.

- **Segurança**: Ferramentas de segurança para atender às necessidades dos clientes, com algumas implementações a cargo do cliente.

- **Governança**: Auditoria baseada em nuvem para garantir conformidade com padrões corporativos, com a possibilidade de automação de patches e atualizações.

- **Gerenciabilidade**: Facilita o gerenciamento de recursos, como a escalabilidade automática e implantação simplificada, através de APIs ou PowerShell.


# Modelo de Responsabilidade Compartilhada na Nuvem  

O **Modelo de Responsabilidade Compartilhada** define quais partes da segurança e do gerenciamento da infraestrutura são de responsabilidade do cliente e quais são do provedor de nuvem. Esse modelo varia conforme o tipo de serviço adotado:  

- **Sempre retida pelo cliente**: Algumas responsabilidades, como o gerenciamento de dados e o controle de acesso, sempre permanecem sob o controle do cliente, independentemente do serviço escolhido.  
- **Varia conforme o tipo**: O nível de responsabilidade do cliente e do provedor muda dependendo do modelo de serviço utilizado.  
- **Transferências de responsabilidade**: À medida que se utiliza serviços gerenciados, mais tarefas são delegadas ao provedor de nuvem.  

## Modelos de Serviço na Nuvem  

### IaaS (Infraestrutura como Serviço)  
- Serviço de nuvem mais flexível, permitindo que o cliente tenha maior controle.  
- O cliente gerencia a infraestrutura virtual, como servidores, redes e armazenamento.  
- **Exemplo**: Máquinas virtuais hospedadas na nuvem.  

### PaaS (Plataforma como Serviço)  
- Focado no desenvolvimento e implantação de aplicativos.  
- O provedor gerencia a infraestrutura e a plataforma, enquanto o cliente gerencia apenas os aplicativos e os dados.  
- **Exemplo**: Serviços de hospedagem de aplicativos e bancos de dados gerenciados.  

### SaaS (Software como Serviço)  
- Modelo baseado em pagamento conforme o uso ou assinatura.  
- O provedor gerencia toda a infraestrutura, plataforma e software, enquanto o cliente apenas utiliza o serviço.  
- **Exemplo**: Microsoft 365, Google Workspace, Dropbox.  

Esse modelo permite que as empresas escolham o nível de controle e gerenciamento que desejam manter, equilibrando flexibilidade, facilidade de uso e segurança.  


# Componentes de Arquitetura do Azure  

## Regiões  
- Compostas por um ou mais datacenters muito próximos.  
- Fornecem flexibilidade e escala para reduzir a latência do cliente.  
- Preservam a residência dos dados com uma ampla oferta de conformidade.  

## Zonas de Disponibilidade  
- Protegem contra tempo de inatividade devido a falha de datacenter.  
- Datacenters fisicamente separados dentro da mesma região.  
- Cada datacenter possui alimentação, resfriamento e redes independentes.  

## Pares de Regiões  
- Mínimo de **300 milhas** de separação entre pares de regiões.  
- Replicação automática para alguns serviços.  
- Prioridade na recuperação em caso de interrupção.  
- Atualizações distribuídas sequencialmente para minimizar tempo de inatividade.  

## Regiões Soberanas do Azure  

### Serviços Governamentais dos EUA  
- Atendem às exigências de segurança e conformidade de agências federais, governos estaduais e locais dos EUA, além de seus provedores de soluções.  

### Azure Governamental  
- Instância separada do Azure.  
- Fisicamente isolado de implantações que não sejam do governo dos EUA.  
- Acessível apenas a pessoal verificado e autorizado.  

### Azure China  
- A Microsoft é o primeiro provedor estrangeiro de serviços de nuvem pública da China, em conformidade com regulamentações governamentais.  
- Instância fisicamente separada dos serviços do Azure, operada pela **21Vianet**.  
- Todos os dados permanecem dentro da China para garantir conformidade.  

## Recursos do Azure  
Os recursos do Azure são componentes essenciais para a criação de soluções na nuvem, como:  
- **Máquinas Virtuais**  
- **Contas de Armazenamento**  
- **Redes Virtuais**  
- **Serviços de Aplicativos**  
- **Banco de Dados SQL**  
- **Funções (Azure Functions)**  

## Grupos de Recursos  
- Contêiner usado para gerenciar e agregar recursos em uma única unidade.  
- Um recurso pode existir em **apenas um grupo de recursos**.  
- Recursos podem ser distribuídos em diferentes regiões.  
- Recursos podem ser **movidos** entre grupos de recursos.  
- Aplicações podem utilizar **múltiplos grupos de recursos**.  

## Assinaturas do Azure  
- Cada conta do Azure pode ter múltiplas assinaturas.  
- Uma assinatura fornece **acesso autenticado e autorizado** aos recursos do Azure.  

### Limites das Assinaturas  
- **Limite de cobrança**: Relatórios de cobrança e faturas separados para cada assinatura.  
- **Limite de controle de acesso**: Gerencia e controla quais recursos podem ser provisionados pelos usuários.  

## Grupos de Gerenciamento  
- Permitem incluir várias assinaturas do Azure.  
- As assinaturas **herdam** as condições aplicadas ao grupo de gerenciamento.  

# Computação e Rede no Azure  

## Serviços de Computação do Azure  
A computação no Azure é um serviço sob demanda que fornece recursos como:  
- **Discos**  
- **Processadores**  
- **Memória**  
- **Rede**  
- **Sistemas Operacionais**  

## Máquinas Virtuais do Azure  
- As **Máquinas Virtuais do Azure (VMs)** são emulações de software de computadores físicos.  
- Incluem **processador virtual, memória, armazenamento e rede**.  
- Oferecem uma solução **IaaS**, permitindo **personalização e controle total**.  

## Conjuntos de Dimensionamento de VMs  
- Permitem o **balanceamento de carga** para escalar os recursos automaticamente.  

## Conjuntos de Disponibilidade de VM  
- Garantem **alta disponibilidade** distribuindo as VMs em domínios de falha e atualização.  

## Área de Trabalho Virtual do Azure  
- Serviço de **virtualização de área de trabalho e aplicativos** na nuvem.  
- Permite criar um ambiente completo de virtualização **sem necessidade de servidores adicionais**.  
- Reduz o risco de que recursos fiquem **obsoletos ou subutilizados**.  
- Suporte a **múltiplas sessões simultâneas**.  

## Serviços de Contêineres do Azure  
Os contêineres do Azure oferecem um ambiente virtualizado **leve e escalável**:  
- **Instâncias de Contêiner do Azure**: PaaS para executar um ou mais contêineres.  
- **Aplicativos de Contêiner do Azure**: PaaS semelhante às instâncias de contêineres, com balanceamento de carga e escalabilidade.  
- **Serviço de Kubernetes do Azure (AKS)**: Orquestração para arquiteturas distribuídas com grande volume de contêineres.  

## Azure Functions  
- Plataforma **PaaS** que permite computação **serverless**.  
- Código baseado em eventos que **executa apenas quando chamado**, sem necessidade de infraestrutura constante.  

## Comparação das Opções de Computação no Azure  

| Opção                | Características |
|----------------------|----------------|
| **Máquinas Virtuais** | Servidor baseado em nuvem para Windows/Linux, útil para migração *lift-and-shift*. Inclui SO do host. |
| **Área de Trabalho Virtual** | Fornece experiência de área de trabalho baseada em nuvem. Suporta múltiplos logins simultâneos. |
| **Contêineres** | Ambientes leves, ideais para microsserviços. Alta escalabilidade e resiliência com orquestração. |

## Serviços de Aplicativos do Azure  
Plataforma totalmente gerenciada para criar, implantar e escalar **aplicativos Web e APIs**.  
- Compatível com **.NET, .NET Core, Node.js, Java, Python e PHP**.  
- Solução **PaaS** com requisitos de **segurança, conformidade e alto desempenho**.  

---

# Serviços de Rede do Azure  

## Rede Virtual do Azure (VNet)  
- Permite comunicação entre recursos do Azure, Internet e redes locais.  
- **Pontos de extremidade públicos**: acessíveis pela Internet.  
- **Pontos de extremidade privados**: acessíveis apenas dentro da rede.  
- **Sub-redes virtuais**: segmentação para melhor organização.  
- **Emparelhamento de rede**: conecta redes privadas diretamente.  

## Gateway de VPN do Azure  
- Envia **tráfego criptografado** entre uma rede virtual do Azure e uma rede local pela Internet pública.  

## ExpressRoute  
- Estende redes locais ao Azure via **conexão privada**, facilitada por um provedor de conectividade.  

## DNS do Azure  
- Oferece **alta confiabilidade e desempenho**, aproveitando servidores de nomes globais com **Anycast**.  
- **Segurança** baseada no **Gerenciador de Recursos do Azure**, com controle de acesso baseado em função.  
- **Gerenciamento unificado** para recursos externos e internos.  
- **Redes virtuais personalizáveis**: uso de nomes de domínio privados personalizados.  
- **Registros de alias**: apontam diretamente para recursos do Azure.  
