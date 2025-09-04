# 04 - Como me Preparar para Entrevistas de DevOps e SRE?

A preparação para uma entrevista, seja para DevOps ou SRE, vai além de simplesmente decorar conceitos. O objetivo é demonstrar mentalidade, experiência prática e a capacidade de resolver problemas. A preparação pode ser dividida em três pilares: Estudo Teórico, Projetos Práticos e Soft Skills.

---

### 1. Estudo Teórico: O Que Revisar?

Ambas as entrevistas exigirão uma base sólida, mas o foco das perguntas pode variar.

| Tópico | Foco na Entrevista de DevOps | Foco na Entrevista de SRE |
| :--- | :--- | :--- |
| **CI/CD** | **Como você constrói um pipeline?** Descreva os estágios, as ferramentas que usou e como garante a velocidade do feedback para os desenvolvedores. | **Como você torna um pipeline confiável?** Descreva como implementaria checagens de qualidade, `rollbacks` automáticos e como o pipeline reage a falhas. |
| **IaC (Terraform)** | **Como você provisiona a infraestrutura?** Mostre seu conhecimento em escrever código para criar recursos, usar módulos e gerenciar o estado. | **Como você gerencia o `drift`?** E como você projeta uma infraestrutura resiliente a falhas de zona или região? Foco em alta disponibilidade. |
| **Kubernetes** | **Como você faz o deploy de uma aplicação?** Fale sobre `Deployments`, `Services`, `Ingress` e como o pipeline interage com o cluster. | **O que você faz quando um `Pod` está em `CrashLoopBackOff`?** Prepare-se para depurar problemas no cluster, otimizar o uso de recursos e entender o funcionamento interno. |
| **Monitoramento** | **Quais ferramentas você usou?** Fale sobre como configurou Prometheus, Grafana ou o ELK Stack para coletar métricas e logs. | **O que é um SLO?** Prepare-se para definir SLIs, SLOs e gerenciar um `Error Budget`. A conversa será menos sobre a ferramenta e mais sobre a **estratégia de confiabilidade**. |
| **Programação** | **Mostre um script que você criou.** O foco será em automação de tarefas. | **Resolva um problema de codificação.** Prepare-se para um desafio de algoritmo/estrutura de dados, similar a uma entrevista de desenvolvedor, mas com foco em sistemas. |

---

### 2. Projetos Práticos (O Portfólio é o seu Melhor Amigo)

A melhor maneira de provar seu conhecimento é mostrando o que você construiu. Este repositório do GitHub é o seu maior trunfo.

* **Para DevOps:**
    * **Crie um pipeline completo:** Pegue uma aplicação simples (ex: um site em Python/Node.js), crie um `Dockerfile` para ela e construa um pipeline no GitHub Actions que faz o build, testa e a implanta em um serviço de nuvem (ex: AWS EC2, Azure App Service).
    * **Automatize com IaC:** Use o Terraform para criar toda a infraestrutura que seu pipeline precisa.

* **Para SRE:**
    * **Adicione Observabilidade:** Pegue o projeto acima e adicione monitoramento com Prometheus e Grafana. Crie um dashboard que mostre métricas importantes (SLIs) como latência e taxa de erros.
    * **Simule uma Falha:** Crie um script ou um cenário que cause uma falha na sua aplicação (ex: um `endpoint` que comece a dar erro 500) e mostre como seu sistema de alertas detectaria isso.
    * **Implemente Auto-remediação (Avançado):** Crie um script que, ao detectar a falha, tente reiniciar a aplicação automaticamente.

---

### 3. Soft Skills: Como Demonstrá-las

Em qualquer entrevista, você será avaliado pela sua capacidade de colaborar e resolver problemas.

* **Use a Metodologia STAR:** Ao responder perguntas sobre sua experiência, use o método **Situação, Tarefa, Ação, Resultado**.
    * **Situação:** "Em um projeto anterior, os deploys eram manuais e demorados."
    * **Tarefa:** "Minha tarefa era automatizar esse processo."
    * **Ação:** "Eu implementei um pipeline de CI/CD usando GitHub Actions que..."
    * **Resultado:** "Como resultado, reduzimos o tempo de deploy de 2 horas para 10 minutos e eliminamos os erros humanos."
* **Seja Curioso:** Faça perguntas inteligentes sobre os desafios da empresa. Isso mostra que você está pensando como um solucionador de problemas, e não apenas como alguém que sabe usar ferramentas.
* **Demonstre Propriedade (Ownership):** Fale sobre os problemas como "nós" (o time), mas sobre as soluções como "eu" (o que você fez).

**Conclusão:** A melhor preparação é a **prática**. Construa projetos, quebre coisas, conserte-as e, o mais importante, **documente tudo** no seu GitHub. Este repositório é a prova viva da sua jornada.