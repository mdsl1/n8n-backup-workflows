# 📦 n8n-backup-workflows

Este repositório armazena o backup automatizado e versionado de todos os meus workflows ativos do n8n. O processo de extração, triagem, organização por pastas e commit é executado de forma 100% autônoma por um agente orquestrador interno.

---

## 🗺️ Estrutura de Diretórios (Organização por Tags)

O repositório adota uma arquitetura dinâmica de pastas. O agente de backup lê a **primeira tag** configurada nas propriedades de cada workflow no n8n e a utiliza como o nome do diretório correspondente. 

Caso um fluxo seja salvo sem nenhuma etiqueta, ele é automaticamente alocado na pasta `Gerais/`.

```text
📦 n8n-backup-workflows/
 ┣ 📂 Project T.A.C.O./           # Automações do ecossistema de agentes de IA
 ┃ ┗ 📜 [T.A.C.O.] Agent Orchestrator.json
 ┃ ┗ 📜 [T.A.C.O.] O Conselho.json
 ┃ ┗ ...
 ┣ 📂 Monitoramento & Backup/           # Automações de monitoramento e notificações/ Agente de Backup 
 ┃ ┗ 📜 Notificar_Mensagens_Contato.json
 ┃ ┗ 📜 Backup Workflows.json
 ┃ ┗ ...
 ┗ 📂 Gerais/                  # Workflows ativos pendentes de categorização
   ┗ 📜 Fluxo-Provisorio.json
