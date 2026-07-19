# 🛠️ Estratégias de Resposta aos Riscos

Plano de ação imediato para cada risco mapeado, contendo a estratégia adotada, plano de contingência e justificativa de gestão.

### 🚨 RSK-01: Falha Crítica ou Indisponibilidade na Integração do Prontuário
* **Estratégia Adotada:** **Mitigar** (Ações imediatas) e **Isolar** (Abordagem arquitetural).
* **Justificativa:** Como a integração é crítica para a entrega do projeto, não podemos aceitar o risco. Precisamos desacoplar o nosso desenvolvimento da instabilidade do parceiro.
* **Plano de Ação:**
  1. **Arquitetura Resiliente (Pattern Advisor/Gateway):** Implementar na camada de serviço um padrão similar ao desenvolvido no *Laboratorio TaskAPI*: um mecanismo inteligente que consome a API externa, mas possui um **fallback local** robusto (banco de dados em cache com dados mockados atualizados de forma assíncrona).
  2. **Task Force Técnica:** Agendar uma reunião de alinhamento técnico urgente com o time do sistema de prontuário externo para congelar um contrato de API (*Swagger/OpenAPI*).

### 📐 RSK-02: Desvio de Escopo (*Scope Creep*) no Fluxo de Agendamento
* **Estratégia Adotada:** **Evitar** (Estancar novos desvios).
* **Justificativa:** O acúmulo de novas regras sem critério inviabiliza o cumprimento de qualquer cronograma e sobrecarrega a equipe.
* **Plano de Ação:**
  1. **Implementação de Formal Change Control:** Instituir uma política rígida de congelamento de escopo para a versão atual (MVP). Toda nova validação solicitada entrará obrigatoriamente para o *Backlog da V2*.
  2. **Design de Soluções Simplificado:** Negociar com os stakeholders para que as novas validações críticas sejam simplificadas e tratadas em nível de *front-end* temporariamente nesta fase intermediária.

### 👥 RSK-03: Burnout e Exaustão da Equipe
* **Estratégia Adotada:** **Mitigar** (Proteger o fator humano).
* **Justificativa:** Sob o ponto de vista ético e de liderança, a integridade da equipe é inegociável. Além disso, desenvolvedores exaustos introduzem mais falhas de segurança e bugs no sistema.
* **Plano de Ação:**
  1. **Replanejamento de Capacidade (*Capacity Planning*):** Recalcular a velocidade do time retirando as horas de horas extras e reajustando as entregas com base na capacidade real (Sprints realistas de 80% de ocupação).
  2. **Foco e Blindagem:** Eliminar reuniões desnecessárias e focar o time estritamente no fluxo crítico (Cadastro + Agendamento Core + Integração Isolada).

### 🧪 RSK-04: Gargalo na Esteira de Testes
* **Estratégia Adotada:** **Mitigar** (Automação e Distribuição).
* **Justificativa:** O tester isolado não consegue absorver a demanda de 4 engenheiros de software sem suporte automatizado.
* **Plano de Ação:**
  1. **Test-Driven / Automação Compartilhada:** Os 4 desenvolvedores passarão a escrever obrigatoriamente testes integrados e unitários para as rotas e serviços (*fastapi/pytest approach*), liberando o Tester para focar exclusivamente nos testes exploratórios de comportamento do app móvel e validação de cenários de erro da API.
