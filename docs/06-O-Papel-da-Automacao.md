# 06 - Qual o papel da automação em DevOps e SRE?

A automação é, sem dúvida, o motor que impulsiona tanto o DevOps quanto o SRE. Sem ela, a entrega rápida e a confiabilidade em escala seriam impossíveis. No entanto, o **propósito** e a **profundidade** da automação podem ser vistos de maneiras ligeiramente diferentes em cada disciplina.

---

### A Perspectiva DevOps: Automação como Acelerador de Fluxo

Para o Engenheiro DevOps, a automação é a principal ferramenta para **aumentar a velocidade, a consistência e a segurança do ciclo de vida de entrega**. O objetivo é remover o máximo possível de intervenção manual para que o código possa fluir do desenvolvedor para a produção com o mínimo de atrito.

**Onde a automação DevOps brilha:**

* **CI/CD Pipelines:** O exemplo máximo. Automatiza a integração, o build, os testes e o deploy, formando a "esteira de produção" do software.
* **Infraestrutura como Código (IaC):** Automatiza a criação e configuração de toda a infraestrutura, garantindo que os ambientes sejam idênticos e reprodutíveis.
* **Testes Automatizados:** Automatiza a verificação da qualidade do código em cada etapa do pipeline.
* **Gerenciamento de Configuração:** Automatiza a instalação e atualização de softwares e dependências nos servidores.

O foco da automação em DevOps é **orquestrar o processo de entrega**. A principal métrica de sucesso de uma boa automação é a **redução do `lead time`** (tempo do commit ao deploy) e da **taxa de falhas nas mudanças**.

---

### A Perspectiva SRE: Automação como Eliminador de `Toil`

Para um SRE, a automação tem um objetivo muito específico e bem definido: **eliminar o `toil`**.

> **O que é `Toil`?**
> `Toil` é o termo cunhado pelo Google para descrever o tipo de trabalho operacional que é **manual, repetitivo, automatizável, reativo e que não agrega valor duradouro**. É o trabalho que tende a crescer linearmente com o tamanho do serviço. Exemplos: reiniciar um servidor manualmente, aplicar um patch de segurança, provisionar uma conta de usuário.

O SRE vê a automação não apenas como um acelerador, mas como uma **estratégia de engenharia para garantir que o sistema possa escalar sem que a equipe precise crescer na mesma proporção**. O objetivo é que o sistema se gerencie sozinho o máximo possível.

**Onde a automação SRE vai além:**

* **Auto-remediação:** Em vez de apenas alertar um humano sobre um problema (ex: um disco está quase cheio), a automação SRE **resolve o problema sozinha** (ex: executa um script que limpa arquivos temporários antigos).
* **Provisionamento de Capacidade Automático:** Escrever automações que analisam tendências de uso e provisionam novos recursos **antes** que o sistema fique sobrecarregado.
* **Execução de Testes de Caos:** Automatizar a injeção de falhas controladas no ambiente de produção (`chaos engineering`) para descobrir proativamente as fraquezas do sistema.
* **Gerenciamento de `Error Budgets`:** Automatizar o bloqueio ou a desaceleração de novos deploys quando o `error budget` de um serviço se esgota.

O foco da automação em SRE é **construir um sistema que se cura e se opera sozinho**. A principal métrica de sucesso é a **redução do `toil`** e a **manutenção dos SLOs** com o mínimo de intervenção humana.

### Conclusão em Tabela

| Aspecto | Automação em DevOps | Automação em SRE |
| :--- | :--- | :--- |
| **Objetivo Primário** | Acelerar o **fluxo de entrega** de software. | Eliminar o **trabalho manual repetitivo (`toil`)**. |
| **Foco** | Orquestrar e automatizar o **processo de CI/CD**. | Construir sistemas **auto-operáveis e auto-remediáveis**. |
| **O que se Automatiza?** | Tarefas do ciclo de vida: build, teste, deploy, provisionamento. | Respostas a incidentes, gerenciamento de capacidade, testes de resiliência. |
| **Resultado Esperado** | Entregas mais rápidas, consistentes e seguras. | Um sistema mais confiável que escala sem precisar de mais operadores humanos. |

Em resumo, DevOps automatiza o **caminho para a produção**, enquanto o SRE automatiza a **própria produção**.