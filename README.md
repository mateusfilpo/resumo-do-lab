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
