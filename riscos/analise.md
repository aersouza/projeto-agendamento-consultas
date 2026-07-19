# 📊 Análise Qualitativa dos Riscos

Análise de probabilidade, impacto socio-técnico e os fatores condicionantes que ativam os gatilhos dos riscos levantados.

### Matriz de Probabilidade e Impacto (Escala 1 a 5)
* **Probabilidade:** 1 (Muito Baixa) a 5 (Muito Alta)
* **Impacto:** 1 (Muito Baixo) a 5 (Muito Alto)

| ID | Risco | Probabilidade | Impacto | Severidade (P x I) | Fatores Condicionantes / Gatilhos |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **RSK-01** | Falha Crítica na Integração | 5 | 5 | **25 (Crítico)** | Falta de um canal de comunicação com a equipe técnica do sistema de prontuário parceiro; ausência de ambiente de *sandbox*. |
| **RSK-02** | Desvio de Escopo (*Scope Creep*) | 4 | 4 | **16 (Alto)** | Ausência de um processo formal de Controle de Mudanças (*Change Control Board*) e validações tardias de regras de negócio. |
| **RSK-03** | Exaustão e Perda de Produtividade | 4 | 4 | **16 (Alto)** | Manutenção de prazos irreais sem readequação da capacidade produtiva (*velocity*) dos 4 desenvolvedores. |
| **RSK-04** | Gargalo na Esteira de Testes | 5 | 3 | **15 (Alto)** | Execução predominantemente manual de testes pelo único tester da equipe face a um fluxo que muda constantemente. |

---

### 💥 Impactos no Projeto

1. **Impacto Técnico (RSK-01 e RSK-04):** A instabilidade da API externa impede o funcionamento do aplicativo. Sem dados confiáveis de prontuário, as consultas agendadas perdem o valor clínico. A falta de braço em testes gera um aumento exponencial de débito técnico na TaskAPI e rotas do app móvel.
2. **Impacto de Negócio (RSK-02):** O desalinhamento das expectativas dos stakeholders estica a data de lançamento do MVP (*Time-to-Market*), gerando frustração comercial e potencial estouro orçamentário.
3. **Impacto Humano e Ético (RSK-03):** Manter a equipe operando acima de sua capacidade sustentável corrói a cultura do time, eleva a rotatividade (*turnover*) e reduz drasticamente a qualidade do código produzido, ferindo princípios éticos de gestão de pessoas.
