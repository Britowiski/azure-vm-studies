
# 📘 Guia Completo: Máquinas Virtuais e Logs no Microsoft Azure

Este repositório contém informações essenciais e técnicas sobre o uso de Máquinas Virtuais (VMs) no Azure e os serviços de monitoramento e logs associados. É um material de apoio para iniciantes e profissionais que desejam entender a fundo a operação, gestão e análise de dados em ambientes de nuvem.

---

## ☁️ Máquinas Virtuais (VMs) - Fundamentos

### O que é uma Máquina Virtual?
Uma Máquina Virtual (VM) é um ambiente de computação simulado que funciona como um computador físico dentro da nuvem. Ela permite executar sistemas operacionais, aplicativos e serviços de maneira isolada e escalável.

### Imagens de Sistemas Operacionais
As VMs no Azure são criadas com base em imagens de sistemas operacionais pré-configuradas. Essas imagens podem ser do Windows, Linux, Red Hat, Ubuntu, entre outras, garantindo flexibilidade para diferentes cenários.

### Tamanhos e Tipos de VMs
O Azure oferece diversos tamanhos de VMs (como B1s, D2s_v3, E4as_v4) que variam em CPU, memória, armazenamento e taxa de IOPS. A escolha do tamanho influencia diretamente no custo e no desempenho da aplicação.

### Discos Gerenciados
As VMs utilizam discos gerenciados que são oferecidos em diferentes níveis de performance: Standard HDD, Standard SSD e Premium SSD. Eles são altamente disponíveis e replicados automaticamente para garantir durabilidade.

### Grupos de Recursos
Um grupo de recursos é um container lógico no Azure que agrupa todos os recursos relacionados, como VMs, discos e redes. Ele facilita a organização e o gerenciamento do ciclo de vida dos recursos.

### Rede Virtual e Subnet
Cada VM é conectada a uma Rede Virtual (VNet) que fornece isolamento e comunicação privada. Dentro da VNet, é possível criar sub-redes para segmentar e controlar o tráfego de rede.

### Endereçamento IP e DNS
As VMs recebem endereços IP públicos e privados, e podem ser configuradas com registros DNS personalizados. O IP público permite o acesso externo, enquanto o privado é usado para comunicação interna.

### Segurança e NSG (Network Security Group)
Os NSGs permitem criar regras de segurança para controlar o tráfego de entrada e saída das VMs. É uma prática essencial para garantir que somente portas e protocolos necessários estejam abertos.

### Escalabilidade
Com Azure Virtual Machine Scale Sets, é possível escalar automaticamente o número de VMs com base na demanda de uso. Isso é ideal para cenários de alta disponibilidade e cargas variáveis.

### Backup e Recuperação
As VMs podem ser protegidas com o Azure Backup, que oferece recuperação automática de dados em caso de falhas, exclusões acidentais ou ataques maliciosos. É uma etapa crítica na gestão de infraestrutura.

---

## 🛠️ Monitoramento e Logs

### Azure Monitor
Azure Monitor é um serviço centralizado que coleta, analisa e age com base em métricas e logs de recursos do Azure. Ele permite rastrear o desempenho, identificar falhas e reagir rapidamente a incidentes.

### Log Analytics
Parte do Azure Monitor, o Log Analytics permite executar consultas personalizadas em grandes volumes de logs. Ele utiliza a linguagem Kusto Query Language (KQL) para extrair insights poderosos dos dados.

### Diagnóstico de Boot
O diagnóstico de boot oferece uma captura de tela da VM durante o processo de inicialização. Ele é útil para identificar problemas de SO, drivers ou arquivos corrompidos logo no boot da máquina.

### Métricas Importantes
Entre as principais métricas monitoradas estão: uso de CPU, utilização de memória, IOPS de disco, tempo de resposta da rede, pacotes de entrada e saída e latência de disco. Essas métricas ajudam a detectar gargalos.

### Alertas Inteligentes
Os alertas no Azure Monitor podem ser configurados para enviar notificações por e-mail, SMS ou webhook quando uma métrica cruza um limiar crítico. Isso possibilita respostas rápidas a falhas ou ameaças.

### Diagnóstico de Recursos
É possível habilitar diagnósticos em VMs para coletar logs de eventos do sistema, logs de aplicativos e métricas de desempenho. Essas informações são armazenadas em uma conta de armazenamento ou enviados ao Log Analytics.

### Acompanhamento em Tempo Real
Com ferramentas como o Azure Monitor Live Metrics, é possível observar dados em tempo real, permitindo ações imediatas em aplicações críticas ou ambientes de produção.

### Dashboard Personalizado
Você pode criar dashboards no portal do Azure para visualizar graficamente as métricas e logs mais relevantes. Isso facilita o acompanhamento do estado de saúde da infraestrutura.

### Integração com Grafana e Power BI
Os dados coletados pelo Azure Monitor podem ser integrados com ferramentas de visualização como Grafana e Power BI. Isso amplia a capacidade de análise e comunicação dos dados com outras equipes.

### Custo de Logs e Métricas
O uso de logs e métricas pode gerar custos adicionais, principalmente em ambientes com alta coleta de dados. É importante planejar a retenção de logs e filtros para otimizar o custo-benefício do monitoramento.

---

## 📚 Referências

- [Documentação oficial do Azure - VMs](https://learn.microsoft.com/pt-br/azure/virtual-machines/)
- [Azure Monitor](https://learn.microsoft.com/pt-br/azure/azure-monitor/overview)
- [Kusto Query Language (KQL)](https://learn.microsoft.com/pt-br/azure/data-explorer/kusto/query/)
- [Segurança em Máquinas Virtuais](https://learn.microsoft.com/pt-br/azure/security/fundamentals/virtual-machines-overview)
