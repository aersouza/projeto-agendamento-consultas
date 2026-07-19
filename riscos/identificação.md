# 🔍 Identificação de Riscos

Nesta etapa, foram identificados e categorizados os principais riscos do projeto com base na Estrutura Analítica de Riscos (EAR), detalhando seu contexto de ocorrência no cenário atual.

| ID | Categoria | Título do Risco | Descrição Detalhada | Contexto de Ocorrência |
| :--- | :--- | :--- | :--- | :--- |
| **RSK-01** | Técnico (Integração) | Falha Crítica ou Indisponibilidade na Integração do Prontuário | A API do sistema de prontuário externo está instável, mal documentada e sofreu alterações recentes sem aviso prévio. | Ocorre na camada de sincronização de dados médicos. Sendo uma dependência crítica, impede a homologação do fluxo de agendamento fim a fim. |
| **RSK-02** | Escopo | Desvio de Escopo (*Scope Creep*) no Fluxo de Agendamento | Inclusão contínua de novas validações e regras de negócio complexas por parte dos stakeholders sem a devida análise de impacto. | Ocorre durante a fase intermediária, alterando o comportamento de funcionalidades que já estavam parcialmente codificadas pela equipe. |
| **RSK-03** | Recursos Humanos | *Burnout*, Exaustão e Perda de Produtividade da Equipe | Sobrecarga de trabalho decorrente do acúmulo de refação (devido às mudanças de escopo) e pressão por prazos subestimados. | Afeta diretamente os 4 desenvolvedores e 1 tester, gerando gargalos na esteira de Code Review e na fase de testes automatizados/manuais. |
| **RSK-04** | Qualidade | Gargalo na Esteira de Testes e Débito Técnico | Com apenas 1 tester para validar o trabalho de 4 desenvolvedores em um cenário de mudanças frequentes de escopo, a taxa de bugs tendará a subir. | Ocorre no encerramento das Sprints, onde o tester fica sobrecarregado com regressões manuais provocadas pela instabilidade da API. |
