# 07 - Como São Construídos os Pipelines?

Um pipeline de CI/CD é a materialização da cultura DevOps. É a "linha de montagem" automatizada que transforma o código de um desenvolvedor em um produto funcional nas mãos do usuário. A construção de um pipeline robusto envolve a visão de fluxo do DevOps e as garantias de confiabilidade do SRE.

---

### A Estrutura Fundamental do Pipeline (A Visão DevOps)

A principal responsabilidade do Engenheiro DevOps é projetar e construir o fluxo de trabalho do pipeline, garantindo que ele seja rápido, eficiente e totalmente automatizado. As etapas fundamentais são:

1.  **Commit / Trigger (Gatilho):**
    * O ciclo começa quando um desenvolvedor envia (`push`) seu código para um repositório Git. Esse evento serve como o gatilho automático que inicia o pipeline.

2.  **Build (Construção):**
    * O servidor de CI (ex: Jenkins, GitLab Runner) pega o código-fonte.
    * Ele compila o código (se necessário), instala as dependências e cria um **artefato**. Em aplicações modernas, esse artefato é geralmente uma **imagem de contêiner (Docker)**.

3.  **Test (Teste Automatizado):**
    * O pipeline executa uma bateria de testes automatizados contra o artefato recém-criado.
    * **Tipos de Teste:** Testes unitários, testes de integração, análise estática de código (`linting`).
    * Se qualquer um desses testes falhar, o pipeline para imediatamente, e o desenvolvedor é notificado. Isso garante que o feedback seja rápido.

4.  **Deploy em Ambiente de Homologação (Staging):**
    * Se os testes passaram, o artefato é implantado automaticamente em um ambiente de homologação (`staging`), que é uma cópia fiel do ambiente de produção.

5.  **Testes de Aceitação (Opcional):**
    * Neste ambiente, testes mais complexos podem ser executados, como testes end-to-end (que simulam a jornada do usuário) ou testes de carga para verificar a performance.

6.  **Deploy em Produção:**
    * Após a aprovação (que pode ser manual ou automática), o pipeline implanta o artefato no ambiente de produção, tornando-o disponível para os usuários finais.

O foco do DevOps aqui é a **fluidez e a velocidade** de todo esse processo.

---

### As Camadas de Confiabilidade (A Visão SRE)

O SRE olha para o pipeline acima e pergunta: **"Onde estão os pontos de falha? Como podemos garantir que este processo não quebre a produção?"**. O SRE adiciona "grades de proteção" e inteligência ao fluxo.

As contribuições do SRE transformam um pipeline rápido em um pipeline **seguro**:

* **"Portões de Qualidade" (Quality Gates) mais Rígidos:**
    * Além dos testes funcionais, o SRE insiste em integrar no pipeline:
        * **Análises de Segurança:** Ferramentas (como o Snyk) que escaneiam por vulnerabilidades conhecidas nas dependências.
        * **Testes de Carga:** Verificam se a nova versão aguenta a carga esperada de usuários sem degradar a performance.

* **Estratégias de Implantação Segura (Progressive Delivery):**
    * O SRE evita o "Big Bang", onde 100% dos usuários recebem a nova versão de uma vez. Em vez disso, ele implementa:
        * **Canary Release (Lançamento Canário):** O deploy é feito para um pequeno subconjunto de usuários (ex: 1% do tráfego). O sistema é monitorado de perto. Se tudo estiver estável, o deploy é gradualmente expandido para todos.
        * **Blue-Green Deployment:** O pipeline direciona o tráfego para uma infraestrutura "verde" idêntica à de produção ("azul"). Se a versão verde se mostrar estável, o tráfego é totalmente virado para ela. Se der problema, o tráfego volta instantaneamente para a azul.

* **Verificação e Rollback Automático:**
    * Esta é uma das contribuições mais importantes do SRE. Após o deploy em produção, o pipeline não "termina".
    * Ele entra em um estado de **verificação**, onde monitora as métricas chave (taxa de erros, latência) da nova versão por alguns minutos.
    * Se essas métricas piorarem e violarem os SLOs, o pipeline aciona um **`rollback` automático**, revertendo para a versão estável anterior sem intervenção humana.

### Conclusão

| | Engenharia de DevOps | Engenharia de SRE |
| :--- | :--- | :--- |
| **Metáfora** | Constrói o **motor** do pipeline. | Instala os **freios, airbags e sensores**. |
| **Foco** | Velocidade, automação e fluxo contínuo. | Segurança, gerenciamento de risco e estabilidade. |
| **Resultado** | Um pipeline que entrega código **rapidamente**. | Um pipeline que entrega código **com segurança**. |

A construção de um pipeline de elite exige ambas as perspectivas. DevOps garante a velocidade, e SRE garante que essa velocidade não resulte em acidentes.