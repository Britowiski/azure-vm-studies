# Gerenciamento de Máquinas Virtuais no Microsoft Azure

Repositório de estudo e aplicação prática dos principais conceitos para criação, configuração, monitoramento e segurança de Máquinas Virtuais (VMs) no Microsoft Azure.

---

## Objetivos

- Compreender a arquitetura e componentes das VMs no Azure.
- Executar operações via Azure Portal, Azure CLI e ARM templates.
- Aplicar configurações de rede, segurança e armazenamento.
- Documentar práticas de gerenciamento, backup e monitoramento.


---

## Conceitos Técnicos Fundamentais

### Máquina Virtual (VM)

Uma VM no Azure é um recurso computacional em nuvem, que emula um computador físico, permitindo executar sistemas operacionais e aplicações.

### Componentes Principais

- **Imagem:** Base do sistema operacional (Windows, Linux).
- **Tamanho (SKU):** Define CPU, memória, IOPS e rede (ex: Standard_D2s_v3).
- **Disco:** Discos gerenciados (Premium SSD, Standard HDD).
- **Rede Virtual (VNet):** Ambiente isolado de rede.
- **Sub-rede:** Segmento dentro da VNet.
- **NSG (Network Security Group):** Firewall para regras de acesso.
- **IP Público:** Para acesso externo via RDP/SSH.
- **Extensões:** Scripts e agentes instalados na VM.

---

## Exemplos Práticos via Azure CLI

### 1. Criar Resource Group

```bash
az group create --name MeuGrupo --location eastus


az vm create \
  --resource-group GrupoCriado \
  --name MinhaVM01 \
  --image UbuntuLTS \
  --size Standard_B1s \
  --admin-username azureuser \
  --generate-ssh-keys \
  --subnet default \
  --public-ip-address "" \
  --no-wait


az network nsg rule create \
  --resource-group GrupoCriado \
  --nsg-name MinhaNSG \
  --name AllowSSH \
  --priority 1000 \
  --protocol Tcp \
  --direction Inbound \
  --source-address-prefixes '*' \
  --source-port-ranges '*' \
  --destination-port-ranges 22 \
  --access Allow
