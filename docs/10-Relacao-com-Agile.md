# 10 - Como Agile se Relaciona com DevOps e SRE?

Agile, DevOps e SRE não são concorrentes; são peças complementares e evolutivas de um quebra-cabeça maior: como entregar software de alta qualidade de forma rápida e sustentável. Eles operam em diferentes partes do ciclo de vida, mas com princípios compartilhados.

De forma simples:
* **Agile** revolucionou o **desenvolvimento**.
* **DevOps** estendeu essa revolução para a **entrega e operações**.
* **SRE** garante que essa nova velocidade seja **confiável e sustentável**.

---

### 1. O Que o Agile Trouxe para a Mesa? (A Origem)

Antes do Agile, o modelo predominante era o "Waterfall" (Cascata), onde cada fase (planejamento, desenvolvimento, teste) levava meses ou anos e era feita de forma isolada. O resultado era lento, arriscado e muitas vezes não atendia às necessidades do cliente.

O **Agile** quebrou esse paradigma com foco em:
* **Ciclos Curtos e Iterativos (Sprints):** Construir e entregar pequenas partes funcionais do software em ciclos de poucas semanas.
* **Colaboração:** Unir desenvolvedores e stakeholders do negócio (Product Owners, etc.) para garantir que o produto certo estivesse sendo construído.
* **Feedback Rápido:** Obter feedback do cliente em cada ciclo para adaptar e melhorar o produto continuamente.

**O novo gargalo:** O Agile tornou as equipes de desenvolvimento extremamente rápidas e eficientes. Elas conseguiam produzir novas versões do software a cada duas semanas. No entanto, a equipe de **Operações** ainda era lenta e manual, levando semanas ou meses para implantar esse software. Isso criou um enorme gargalo e conflito entre "Dev" (que queria velocidade) e "Ops" (que queria estabilidade).

---

### 2. DevOps: Estendendo a Agilidade Além do Código

O **DevOps** surgiu como uma resposta direta a esse gargalo. Ele pega os princípios do Agile (velocidade, automação, feedback, pequenos lotes) e os aplica ao processo de **entrega e operações**.

* Se o **Agile** se pergunta "Como podemos desenvolver features mais rápido?", o **DevOps** se pergunta "Como podemos *entregar* essas features mais rápido e com mais segurança?".

**Como eles se conectam:**
* **Ciclos Curtos (Agile) → Deploys Frequentes (DevOps):** O pipeline de CI/CD do DevOps é o que torna possível implantar em produção as pequenas entregas geradas a cada Sprint do Agile.
* **Colaboração (Agile) → Quebra de Silos (DevOps):** O DevOps estende a colaboração do Agile para incluir também as equipes de Operações, Segurança e Qualidade.
* **Feedback do Cliente (Agile) → Feedback do Sistema (DevOps):** O DevOps adiciona o monitoramento e a observabilidade como uma forma de "feedback" técnico contínuo sobre a saúde da aplicação.

Se o Agile ensinou a equipe a construir um motor de carro em duas semanas, o DevOps construiu a linha de montagem automatizada para colocar esse motor no chassi e na estrada em minutos.

---

### 3. SRE: A Garantia de que a Velocidade é Sustentável

A combinação de Agile e DevOps cria uma pressão imensa por **velocidade**. Mas como saber se não estamos indo rápido demais a ponto de comprometer a estabilidade do serviço?

O **SRE** entra como o "freio de segurança" baseado em dados. Ele responde à pergunta: **"Quão rápido é rápido demais?"**.

* O SRE estabelece os **SLOs (Objetivos de Nível de Serviço)**, que são metas claras de confiabilidade.
* A partir dos SLOs, ele calcula o **Error Budget (Orçamento de Erros)**.
* O Error Budget se torna a métrica que guia a velocidade do time Agile/DevOps. O SRE diz: "Vocês podem entregar novas features na velocidade que o Agile e o DevOps permitem, **desde que não esgotem o nosso orçamento de erros**".

Se o orçamento se esgota devido a muitas falhas, a prioridade nº 1 de todos (incluindo o time Agile) passa a ser a estabilidade, não as novas features do próximo Sprint. Isso cria um sistema de auto-regulação que equilibra perfeitamente a inovação (Agile) com a confiabilidade (SRE).

### Conclusão

| Metodologia | Foco Principal | Pergunta que Responde |
| :--- | :--- | :--- |
| **Agile** | O Processo de **Desenvolvimento** | "Estamos construindo o **produto certo** e da forma certa?" |
| **DevOps** | O Processo de **Entrega** | "Conseguimos entregar este produto de forma **rápida e automatizada**?" |
| **SRE** | A **Operação** do Produto | "O produto continua funcionando de forma **confiável** para o usuário?" |

Eles não são excludentes; são camadas de uma mesma estratégia. Uma equipe de alta performance moderna é ágil em seu desenvolvimento, usa práticas DevOps para a entrega e é guiada por princípios SRE para garantir a sustentabilidade.