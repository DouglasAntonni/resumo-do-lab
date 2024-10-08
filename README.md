# Resumo do Lab - Azure

Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO sobre introdução ao Azure.

## Tópicos abordados:

### 1. Criação de Máquinas Virtuais no Azure
- Aprendi a criar e configurar uma máquina virtual (VM) no Azure, incluindo a seleção do sistema operacional (Windows), tamanho da VM, e configurações de rede.
- Configurei regras de porta de entrada para permitir o acesso via Remote Desktop Protocol (RDP) na porta 3389.

### 2. Armazenamento de Dados em Máquinas Virtuais
- Compreendi a importância de usar discos de dados anexados para o armazenamento persistente de arquivos, em vez do disco do sistema operacional ou do disco temporário.

### 3. Grupos de Segurança de Rede (NSG)
- Descobri que a última regra aplicada em um Grupo de Segurança de Rede é a regra "Negar Tudo" (Deny All), o que garante que qualquer tráfego não explicitamente permitido seja bloqueado.

### 4. Boas Práticas no Azure
- Refleti sobre as melhores práticas de segurança e armazenamento ao trabalhar com recursos de nuvem, como limitar o acesso às VMs e configurar backup adequado para os dados.

### 5. Integração com o GitHub
- Durante o lab, aprendi a criar e gerenciar repositórios no GitHub para armazenar e compartilhar o resumo do trabalho desenvolvido.

- # SLA no Azure (Service Level Agreement)

Os **SLAs** (Acordos de Nível de Serviço) no Azure definem os compromissos da Microsoft em termos de **disponibilidade, desempenho e conectividade** dos serviços em nuvem. Eles garantem níveis mínimos de serviço para clientes e, em caso de falha, podem resultar em compensações.

## Principais Tópicos:

### 1. Definição de SLA
- Compromissos em relação à **disponibilidade**, **confiabilidade** e **conectividade** dos serviços.
- Especifica o tempo de atividade garantido e o nível de desempenho esperado.

### 2. Exemplos de Níveis de SLA
- **Máquinas Virtuais (VMs)**: 99,9% de disponibilidade com discos gerenciados.
- **SQL Azure**: 99,99% de disponibilidade.
- **Azure App Services**: 99,95% de tempo de atividade.
- **Armazenamento Azure**: Durabilidade de até 99,999999999% para armazenamento com redundância geográfica.

### 3. Alta Disponibilidade
- Configurações como **Availability Sets** podem aumentar o SLA, garantindo até **99,95%** de tempo de atividade para VMs.

### 4. Compensações
- Se o Azure não cumprir o SLA, o cliente pode receber **créditos de serviço** como compensação.

### 5. Monitoramento
- Ferramentas como o **Azure Monitor** e o **Azure Service Health** permitem que os clientes acompanhem o desempenho dos serviços e verifiquem o cumprimento do SLA.

### Exemplo:
- Um SLA de 99,9% de disponibilidade permite até **43,2 minutos de inatividade** por mês (em 30 dias).

### 6. Combinação de SLAs
- Quando serviços são combinados, o SLA geral é o **produto dos SLAs individuais**. Isso pode reduzir ligeiramente o nível de disponibilidade combinado.

---

Os SLAs no Azure fornecem previsibilidade e garantias aos clientes, permitindo que eles planejem a confiabilidade e a resiliência de suas soluções em nuvem.

# Tipos de Serviço de Nuvem na Azure

A Azure oferece diferentes **modelos de serviço em nuvem**, cada um projetado para atender a diferentes necessidades de negócios e níveis de gerenciamento de recursos. Esses serviços são classificados em três principais categorias:

## 1. **IaaS (Infrastructure as a Service)**
- **Descrição**: Oferece infraestrutura de TI sob demanda, como servidores virtuais, redes, e armazenamento. O cliente gerencia o sistema operacional, aplicativos e dados.
- **Exemplos de uso**: Criação de máquinas virtuais, armazenamento de dados em discos gerenciados, redes virtuais.
- **Responsabilidade do cliente**: Gerenciamento de SO, aplicativos, tempo de execução e middleware.
- **Exemplos de serviços Azure**: Azure Virtual Machines, Azure Storage.

## 2. **PaaS (Platform as a Service)**
- **Descrição**: Fornece uma plataforma completa para desenvolvimento e implantação de aplicativos, sem a necessidade de gerenciar a infraestrutura subjacente.
- **Exemplos de uso**: Desenvolvimento de aplicativos web, APIs, e serviços móveis.
- **Responsabilidade do cliente**: Desenvolvimento e gerenciamento de aplicativos, enquanto o provedor gerencia a infraestrutura, o SO e as atualizações.
- **Exemplos de serviços Azure**: Azure App Service, Azure Functions.

## 3. **SaaS (Software as a Service)**
- **Descrição**: Oferece aplicativos prontos para uso que são gerenciados pelo provedor de nuvem, acessíveis via navegador ou APIs.
- **Exemplos de uso**: Aplicativos como e-mail, CRM, e ferramentas de colaboração.
- **Responsabilidade do cliente**: Somente o uso do software, sem precisar se preocupar com a infraestrutura ou manutenção.
- **Exemplos de serviços Azure**: Microsoft 365, Dynamics 365.

## Comparação entre os Modelos:
| Modelo   | Gerenciado pelo Cliente                   | Gerenciado pela Azure                         |
|----------|-------------------------------------------|-----------------------------------------------|
| **IaaS** | Aplicações, SO, dados, tempo de execução   | Infraestrutura, rede, hardware                |
| **PaaS** | Aplicações, dados                         | Sistema operacional, rede, infraestrutura     |
| **SaaS** | Apenas o uso da aplicação                 | Todo o resto (aplicação, infraestrutura, etc) |

---

A escolha do tipo de serviço depende das necessidades do projeto e do nível de controle que o cliente deseja ter sobre o ambiente. IaaS oferece mais controle, enquanto SaaS fornece soluções prontas e gerenciadas.


