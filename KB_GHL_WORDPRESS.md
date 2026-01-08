# 🧠 Guia de Integração: GoHighLevel + WordPress (Elite)

Este guia detalha as melhores formas de conectar o ecossistema GHL ao WordPress, garantindo captura de leads, rastreamento e automação sem depender da hospedagem interna da GHL.

---

## 🚀 Método 1: Sem Plugin LeadConnector (Via Webhooks)
*Ideal para quem usa Elementor, Divi ou outros construtores e quer máxima performance e controle.*

### Passo a Passo (Exemplo Elementor):
1.  **No GoHighLevel:**
    *   Crie um novo **Workflow**.
    *   Defina o gatilho como **Inbound Webhook**.
    *   Copie a **Webhook URL** gerada.
2.  **No WordPress (Elementor):**
    *   Edite o formulário desejado.
    *   Em **Actions After Submit**, adicione a opção **Webhook**.
    *   No novo campo "Webhook" que aparecer, cole a URL do GHL.
3.  **Mapeamento de Dados:**
    *   Envie um formulário de teste no seu site.
    *   No GHL, clique em **Fetch Sample Requests** para ver os dados chegando.
    *   Mapeie os campos (ex: `form_fields[name]` -> `Full Name`).
4.  **Automação:**
    *   Adicione a ação **Create/Update Contact**.
    *   Adicione a ação **Add to Pipeline** para criar a oportunidade automaticamente.

---

## 🔌 Método 2: Com Plugin LeadConnector
*Ideal para integração rápida de Chat Widgets, Funis e Calendários nativos.*

### Passo a Passo:
1.  **Instalação:**
    *   No WordPress, vá em **Plugins > Adicionar Novo** e busque por "LeadConnector".
    *   Instale e ative o plugin.
2.  **Conexão via API:**
    *   No GHL, vá em **Settings > API Keys** e copie a chave da subconta.
    *   No WordPress, vá nas configurações do LeadConnector e cole a API Key.
3.  **Funcionalidades Disponíveis:**
    *   **Chat Widget:** Ative o widget de chat do GHL em todo o site com um clique.
    *   **Funnels/Pages:** Importe páginas criadas no GHL para dentro do seu domínio WordPress (ex: `seusite.com.br/promocao`).
    *   **Shortcodes:** Use shortcodes para embutir formulários e calendários nativos do GHL em qualquer página ou post.

---

## 💡 Comparativo Estratégico

| Recurso | Sem Plugin (Webhook) | Com Plugin (LeadConnector) |
| :--- | :--- | :--- |
| **Performance** | Mais leve (sem scripts extras) | Adiciona scripts do plugin |
| **Design** | Usa o design do seu tema/Elementor | Usa o design nativo do GHL |
| **Facilidade** | Requer configuração de mapeamento | Plug-and-play para widgets |
| **Rastreamento** | Requer GTM ou script manual | Rastreamento nativo simplificado |

---

## 🛡️ Ativos de Inteligência para o Superagente
*   **Ação IA (Sem Plugin):** "Manus, configure o webhook do formulário de 'Contato' do WordPress para criar uma oportunidade no funil de 'Vendas Diretas'."
*   **Ação IA (Com Plugin):** "Manus, ative o Chat Widget da GHL no meu WordPress e importe a página de 'Obrigado' do funil X."
*   **Ação IA (Rastreamento):** "Verifique se o script de rastreamento da GHL está instalado corretamente no cabeçalho do WordPress para capturar a origem dos leads."
