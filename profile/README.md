# 🚀 MantecSystems1 Infrastructure

Bem-vindo à organização de gerenciamento da infraestrutura **Docker Swarm** da MantecSystems. Este perfil é atualizado automaticamente pelo nosso servidor Ubuntu via GitHub CLI.

## 📊 Dashboard de Serviços (Estado Atual)

| Serviço | Domínio / URL | Status | Stack |
| :--- | :--- | :--- | :--- |
| **Ollama AI** | `ai.portalmantec.com.br` | ✅ 1/1 | `ai` |
| **Sigma API** | `sigma.portalmantec.com.br` | ✅ 1/1 | `sigma` |
| **Site Principal** | `portalmantec.com.br` | ✅ 1/1 | `site` |
| **Nextcloud** | `cloud.portalmantec.com.br` | ❌ 0/1 | `nextcloud` |
| **n8n Automação** | `n8n.portalmantec.com.br` | ✅ 1/1 | `traefik` |
| **Vaultwarden** | `vault.portalmantec.com.br` | ✅ 1/1 | `vault` |
| **Grafana** | `grafana.portalmantec.com.br` | ✅ 1/1 | `traefik` |
| **Portainer** | `port.portalmantec.com.br` | ❌ 0/1 | `portainer` |

## 🛠️ Infraestrutura Técnica

### Cluster Docker Swarm
- **Manager**: `mantec` (v29.4.3)
- **Nodes**: 5 ativos (`mantec` + `node1` a `node4`)
- **Ingress**: Traefik v3.6.13 (Gerenciando SSL via Let's Encrypt)

### Bancos de Dados Ativos
- **MSSQL 2022**: ✅ Online (Sigma)
- **MongoDB 6**: ✅ Online (Mantec3)
- **MariaDB 11**: ❌ Offline (Nextcloud)
- **Redis 7**: ❌ Offline (Nextcloud)

## 🚨 Incidentes Ativos
Atualmente, os seguintes serviços de monitoramento e aplicação requerem intervenção técnica (réplicas em 0):
- `monitoring_mongo-exporter`
- `monitoring_mysqld-exporter`
- `nextcloud_app` / `nextcloud-db_db`
- `portainer-stack_portainer`

---
## 📖 Links Úteis
- [📄 Inventário Completo](https://github.com/mantecsystems1/infra-status/blob/main/inventory.md)
- [🌐 Mapa de Redes e Topologia](https://github.com/mantecsystems1/infra-status/blob/main/topology.md)
- [⚡ Histórico de Incidentes](https://github.com/mantecsystems1/infra-status/issues)

> *Este README é atualizado automaticamente a cada hora pelo servidor `mantec`.*
