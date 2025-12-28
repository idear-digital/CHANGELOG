# 🧠 Ativos de Inteligência: Workflows & MCP (GHL Elite)

Esta base consolida os conhecimentos técnicos mais críticos para que o Superagente opere o GHL com precisão cirúrgica.

---

## 🛠️ Módulo: Workflows & Automações

### 1. Configurações Globais de Workflow (Workflow Settings)
*   **O que é:** Painel de controle de comportamento do fluxo (Allow Multiple, Stop on Response).
*   **Benefício:** Evita spam e garante que o lead receba a automação correta no momento certo.
*   **Regra de Ouro:** Sempre ative "Allow Multiple" para fluxos de agendamento, mas use com cautela em fluxos de boas-vindas.
*   **Ação IA:** "Manus, verifique se o fluxo de Onboarding permite múltiplas entradas para o mesmo contato."

### 2. Gatilho: Agendamento de Consulta (Customer Booked Appointment)
*   **O que é:** Disparador ativado quando um lead marca um horário no calendário.
*   **Benefício:** Automação total de lembretes e preparação para a reunião.
*   **Configuração:** Pode ser filtrado por Calendário específico ou Status da Consulta.
*   **Ação IA:** "Crie um lembrete de 24h e 1h para todas as consultas marcadas no calendário 'Vendas'."

### 3. Gatilho: Detalhes da Chamada (Call Details)
*   **O que é:** Disparador baseado no resultado de uma ligação (Duração, Status, Direção).
*   **Benefício:** Essencial para o *WhatsApp Back* e auditoria de SDRs.
*   **Filtro Crítico:** Status "No Answer" ou "Busy" para disparar recuperação imediata.
*   **Ação IA:** "Se a chamada da Vaicci não for atendida, envie o script de recuperação via WhatsApp."

### 4. Ação: Lógica Condicional (If/Else Advanced)
*   **O que é:** O "cérebro" dentro do fluxo que decide caminhos baseados em dados.
*   **Benefício:** Permite criar jornadas personalizadas (ex: Cliente VIP vs Lead Frio).
*   **Novidade:** Comparação de datas e horários agora é nativa.
*   **Ação IA:** "Se o lead já tiver a tag 'Cliente', pule a etapa de oferta e vá direto para o Onboarding."

### 5. Ação: Formatador de Data/Hora (Date/Time Formatter)
*   **O que é:** Ferramenta para manipular datas dentro do fluxo.
*   **Benefício:** Cálculo de prazos de vencimento de boletos ou contratos.
*   **Aplicação:** Adicionar 2 dias à data atual para definir o vencimento no Asaas.
*   **Ação IA:** "Calcule a data de vencimento para 48h a partir de agora e salve no campo personalizado."

### 6. Ação: Google Sheets Premium
*   **O que é:** Integração direta para ler/escrever em planilhas sem Zapier.
*   **Benefício:** Relatórios em tempo real e backup de dados externo.
*   **Uso:** Enviar dados de faturamento para uma planilha de controle financeiro.
*   **Ação IA:** "Registre cada venda confirmada na planilha 'Faturamento Idear 2025'."

---

## 🤖 Módulo: MCP (Model Context Protocol)

### 7. Configuração do Servidor MCP
*   **O que é:** Ponte de comunicação entre IAs externas e o banco de dados do GHL.
*   **Benefício:** Permite que o Claude ou GPT-4o "atuem" como um funcionário dentro do seu CRM.
*   **Requisito:** Private Integration Token (PIT) com escopos de leitura e escrita.
*   **Ação IA:** "Conecte meu agente de suporte ao servidor MCP para que ele possa consultar o status dos contatos."

### 8. Gestão Unificada de Tarefas (Unified Task Management)
*   **O que é:** Visão centralizada de tarefas entre Contatos e Oportunidades.
*   **Benefício:** O agente de IA pode organizar a agenda do dono da agência via MCP.
*   **Aplicação:** Listar todas as tarefas pendentes de "Follow-up" para o dia de hoje.
*   **Ação IA:** "Manus, quais são minhas 5 tarefas mais urgentes no CRM hoje?"

### 9. Integração de Pagamentos Customizados
*   **O que é:** Capacidade de conectar gateways externos (como Asaas) via API/MCP.
*   **Benefício:** Recebimento rápido (2 dias) mantendo o status de "Pago" dentro do GHL.
*   **Fluxo:** Webhook Asaas -> n8n -> MCP GHL (Update Opportunity).
*   **Ação IA:** "Quando o Asaas confirmar o Pix, use o MCP para marcar a oportunidade como 'Ganha'."

### 10. Busca Semântica e Knowledge Base
*   **O que é:** Uso de IA para ler a Central de Ajuda e responder dúvidas técnicas.
*   **Benefício:** Suporte 24/7 para os clientes da sua subconta Whitelabel.
*   **Diferencial:** O agente entende a intenção, não apenas palavras-chave.
*   **Ação IA:** "Explique para o cliente como ele pode integrar o domínio dele no nosso criador de sites."
