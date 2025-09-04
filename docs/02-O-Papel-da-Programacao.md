# 02 - Como DevOps e SRE Utilizam a Programação?

A resposta curta é: **Sim, ambos programam, e a programação é ainda mais fundamental para o SRE.**

Embora tanto o Engenheiro DevOps quanto o SRE usem a programação extensivamente, a natureza e a profundidade dessa habilidade podem variar. O SRE, por definição, é um papel de engenharia de software aplicado às operações, o que intensifica a necessidade de codificação.

---

### A Perspectiva do Engenheiro DevOps

Um **Engenheiro DevOps** usa a programação como uma **ferramenta para construir, automatizar e manter a infraestrutura e os processos** do ciclo de vida de software. O foco principal é a **automação do fluxo**.

**Onde o DevOps usa programação:**
* **Scripts de Automação:** Usando **Python**, **Bash/Shell Script** ou **Go** для automatizar tarefas repetitivas (backups, verificações, etc.).
* **Infraestrutura como Código (IaC):** Escrevendo código declarativo com ferramentas como **Terraform (HCL)** ou **CloudFormation (YAML/JSON)** para provisionar infraestrutura.
* **Pipelines de CI/CD:** Definindo os estágios do pipeline com **YAML** (GitLab CI, GitHub Actions) ou **Groovy** (Jenkins).
* **Gerenciamento de Configuração:** Usando **YAML** (Ansible) ou **Ruby** (Chef) para configurar sistemas.

Para o Engenheiro DevOps, a programação é o meio para um fim: **a eficiência e a velocidade da entrega**.

---

### A Perspectiva do SRE (Site Reliability Engineer)

Para um **SRE**, a programação não é apenas uma ferramenta de automação; é a **principal abordagem para resolver problemas de operações**. O lema do Google SRE é "tratar as operações como um problema de software". Isso significa que o SRE tem uma expectativa de habilidade de programação mais profunda.

**Onde o SRE usa programação (além de tudo o que o DevOps faz):**

* **Ferramentas Internas:** Um SRE frequentemente constrói, do zero, ferramentas internas para automação de larga escala, análise de causa raiz ou para gerenciar a confiabilidade do sistema. Se uma ferramenta de mercado não resolve o problema, o SRE a constrói.
* **Análise de Dados e Depuração Profunda:** SREs escrevem código para analisar grandes volumes de métricas e logs, identificar padrões complexos e depurar problemas de performance no nível do sistema operacional ou até mesmo no código da aplicação.
* **Automação de Resposta a Incidentes (Auto-remediação):** Em vez de apenas alertar, um SRE escreve código que **reage automaticamente** a um problema. Por exemplo, um script que, ao detectar uma falha, automaticamente coleta dados de diagnóstico, reinicia o serviço e abre um ticket para os desenvolvedores com as informações.
* **Implementação de `Error Budgets`:** SREs escrevem automações que controlam a taxa de deploys com base no "orçamento de erros" (Error Budget). Se o serviço já falhou muito em um período, o pipeline pode ser automaticamente bloqueado.

Para o SRE, a programação é a forma de **codificar a confiabilidade** e **eliminar o trabalho manual repetitivo (toil)** de forma sistemática.

### Conclusão em Tabela

| Aspecto | Engenheiro DevOps | Engenheiro SRE |
| :--- | :--- | :--- |
| **Foco da Programação** | **Automação de processos** e pipelines. | **Resolução de problemas de operações** através de engenharia de software. |
| **Profundidade** | Proficiente, focado em scripts e linguagens de configuração. | Avançado, similar a um desenvolvedor de software, com foco em sistemas distribuídos. |
| **"Produto" do Código** | Um pipeline de CI/CD eficiente, uma infraestrutura consistente. | Ferramentas de auto-remediação, sistemas de monitoramento avançados, uma plataforma confiável. |
| **Principal Objetivo** | Acelerar a **entrega** de software. | Garantir a **confiabilidade** do software em produção. |

Em resumo, ambos programam, mas enquanto o DevOps usa código para **construir a ponte**, o SRE usa código para **tornar a ponte indestrutível e inteligente**.