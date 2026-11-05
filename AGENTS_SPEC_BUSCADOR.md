# ESPECIFICAÇÃO DA ARQUITETURA MULTI-AGENTES — BUSCADOR & PROSPECTOR DE AUTOESCOLAS

Este documento define a divisão de responsabilidades dos **4 Agentes Especializados** que compõem o sistema de prospecção e fechamento de sites para autoescolas, integrado aos nossos playbooks:
- [PLAYBOOK_DIRECAO_DE_ARTE_AUTOESCOLAS.md](file:///c:/Users/akreu/Downloads/variados/sites/autoescola/PLAYBOOK_DIRECAO_DE_ARTE_AUTOESCOLAS.md)
- [PLAYBOOK_NEGOCIACAO_E_FECHAMENTO.md](file:///c:/Users/akreu/Downloads/variados/sites/autoescola/PLAYBOOK_NEGOCIACAO_E_FECHAMENTO.md)

---

## 1. OS 4 AGENTES DO SISTEMA

```
┌────────────────────────────────────────────────────────────────────────┐
│                   SISTEMA PROSPECTOR DE AUTOESCOLAS                    │
└────────────────────────────────────────────────────────────────────────┘
                                    │
    ┌───────────────────────────────┼───────────────────────────────┐
    ▼                               ▼                               ▼
[AGENTE 1: SCOUT]           [AGENTE 2: AUDITOR]           [AGENTE 3: PITCH]
Rastreador de Leads         Diagnóstico & Raio-X          Copywriter Tático WhatsApp
• Localização & Bairro      • Tem site? ➔ Acha falhas     • Aplica Chris Voss / Hormozi
• Telefone fixo / Móvel     • NÃO tem site? ➔ Raio-X Maps • Mensagem personalizada 1 clique
• WhatsApp detectado        • Status de prioridade        • Link wa.me pronto para envio
    │                               │                               │
    └───────────────────────────────┼───────────────────────────────┘
                                    ▼
                        [AGENTE 4: ART DIRECTOR]
                        Briefing para o Playbook de Design
                        • Define Território Visual (Cockpit, Bairro, Street...)
                        • Gera o prompt exato para a IA criar o index.html
```

---

### AGENTE 1: SCOUT (Rastreador & Coletor de Leads)
- **Função:** Buscar e organizar autoescolas por país, cidade ou bairro (ex: València - Patraix, Ruzafa, Benimaclet, Campanar, etc.).
- **Dados Coletados:**
  - Nome oficial da autoescola.
  - Endereço físico completo e bairro.
  - Telefone fixo (`96X XXX XXX` na Espanha) e Celular/WhatsApp (`6XX XXX XXX` ou `7XX XXX XXX`).
  - **Perfil do Instagram (detectado ou botão de busca direta de perfil).**
  - Presença de site oficial (URL existente ou Ausente).
  - Nota e volume de avaliações do Google Maps.

---

### AGENTE 2: AUDITOR (Diagnóstico de Vulnerabilidade)
- **Função:** Classificar o lead em duas rotas estratégicas:
  1. **ROTA A — COM SITE EXISTENTE (Oportunidade de Renovação):**
     - Identifica vulnerabilidades técnicas: falta de botão de WhatsApp direto, ausência de calculadora DGT, site não responsivo no mobile, textos antigos em inglês ou desatualizados.
     - Ângulo de ataque: *"O site de vocês está perdendo alunos no mobile e tem erros visíveis."*
  2. **ROTA B — SEM SITE (Oportunidade de Criação do Zero — Prioridade Máxima):**
     - A autoescola depende 100% do Google Maps e perde todas as buscas orgânicas da região para concorrentes.
     - Compila os dados do Maps (endereço, notas, horários, categorias prováveis) para servir de insumo de criação imediata.
     - Ângulo de ataque: *"Todo jovem de 17-18 anos em [Bairro] pesquisa no Google e vai direto para a autoescola que tem site moderno com WhatsApp."*

---

### AGENTE 3: PITCH (Copywriter Tático de WhatsApp)
- **Função:** Gerar em tempo real a mensagem persuasiva para o WhatsApp da autoescola seguindo rigorosamente o [PLAYBOOK_NEGOCIACAO_E_FECHAMENTO.md](file:///c:/Users/akreu/Downloads/variados/sites/autoescola/PLAYBOOK_NEGOCIACAO_E_FECHAMENTO.md).
- **Mecânica:**
  - Diferencia o tom caso a autoescola tenha site (cita a falha do site atual + link da prévia) ou não tenha site (cita a falta de presença online + prévia exclusiva pronta).
  - Inclui o link `wa.me` com o número da autoescola já codificado para abrir em 1 clique no celular ou web.
  - **Gera pitch específico para Instagram Direct (DM):** Mensagem curta e magnética adaptada para envio via direct do Instagram quando o WhatsApp não responder.

---

### AGENTE 4: ART DIRECTOR (Alimentador do Playbook de Design)
- **Função:** Gerar com 1 clique o comando/prompt completo estruturado para o [PLAYBOOK_DIRECAO_DE_ARTE_AUTOESCOLAS.md](file:///c:/Users/akreu/Downloads/variados/sites/autoescola/PLAYBOOK_DIRECAO_DE_ARTE_AUTOESCOLAS.md).
- **Saída:**
  - O usuário clica em "Copiar Briefing de Design" e cola no chat para a IA gerar o novo `index.html` sob medida para aquele cliente específico.

---

## 2. INTERFACE UNIFICADA DO SISTEMA
O sistema é disponibilizado como uma aplicação web standalone em `buscador.html`, acessível em qualquer computador ou celular sem necessidade de instalação de servidores complexos.
