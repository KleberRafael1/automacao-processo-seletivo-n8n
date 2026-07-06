# Automação de Processo Seletivo e Comunicação Dinâmica com n8n

Este projeto apresenta uma solução completa de automação de ponta a ponta (End-to-End) voltada para a otimização de processos de Recursos Humanos e triagem de candidatos. Utilizando a ferramenta de orquestração de workflows **n8n**, o fluxo integra planilhas em nuvem ao serviço de disparo de e-mails de forma 100% automatizada, segura e escalável.

A solução elimina o trabalho operacional de preenchimento manual de mensagens e malas diretas, garantindo eficiência, personalização e governança na comunicação.

---

## 📊 Arquitetura do Workflow

Abaixo está a representação visual do fluxo estruturado dentro do n8n, mostrando a jornada dos dados desde a captura na planilha até o tratamento de tempo e envio do e-mail:

![Workflow do n8n](fluxo-n8n.png)
![Workflow do n8n](fluxo-n8n-2.png)

---

## 🚀 Funcionalidades e Diferenciais Técnicos

*   **Integração Nativa com Google Sheets API:** Consumo de dados estruturados diretamente da nuvem, permitindo que a automação trabalhe sempre com a versão mais recente dos dados sem necessidade de download de arquivos locais.
*   **Comunicação Dinâmica e Personalizada:** Utilização de expressões e manipulação de objetos JSON no n8n para injetar variáveis (como nome do candidato, status e dados exclusivos) diretamente no escopo do e-mail.
*   **Infraestrutura de Segurança (SMTP dedicado):** Implementação de arquitetura segura de disparo utilizando protocolo SMTP autenticado via senhas de aplicativo (App Passwords) criptografadas, garantindo isolamento de poder e integridade da conta principal.
*   **Gerenciamento de Fila e Proteção Anti-Spam:** Inclusão estratégica de um nó de retenção temporal (*Wait Node* de 5 segundos) entre os disparos. Essa prática controla o ritmo de requisições enviadas ao servidor de e-mail, mitigando riscos de bloqueio e garantindo alta entregabilidade (Score de Spam reduzido).

---

## 🛠️ Tecnologias e Ferramentas Utilizadas

*   **n8n** (Orquestrador de Workflows e Integrações API)
*   **Google Sheets** (Banco de dados em nuvem para armazenamento de candidatos)
*   **SMTP / Gmail** (Protocolo de transporte e infraestrutura de e-mail)
*   **JSON** (Estruturação e tráfego de dados entre os nós)
