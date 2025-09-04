# 05 - O que é o Ciclo de Vida da Entrega de Software?

O Ciclo de Vida da Entrega de Software (Software Delivery Lifecycle - SDLC) é a sequência de estágios pelos quais uma ideia passa até se tornar uma funcionalidade em produção, nas mãos do usuário. Tanto DevOps quanto SRE atuam em todo este ciclo, mas com objetivos e focos primários diferentes.

---

### A Perspectiva DevOps: O Foco no Fluxo Contínuo

Para o Engenheiro DevOps, o ciclo de vida é um **fluxo** a ser otimizado. O principal objetivo é fazer com que o código passe por todas as etapas da forma mais rápida, automatizada e eficiente possível, eliminando gargalos e promovendo a colaboração.

Os estágios clássicos sob a ótica de DevOps são:

1.  **Plan (Planejar):** Definição de requisitos e planejamento das tarefas (usando metodologias Agile).
2.  **Code (Codificar):** Desenvolvimento da funcionalidade e versionamento do código (com Git).
3.  **Build (Construir):** Compilação do código-fonte e criação dos artefatos (ex: uma imagem Docker).
4.  **Test (Testar):** Execução de testes automatizados (unitários, de integração) para garantir a qualidade.
5.  **Release (Lançar):** Versionamento do artefato e preparação para o deploy.
6.  **Deploy (Implantar):** Instalação do artefato no ambiente de produção.
7.  **Operate (Operar):** Manutenção e gerenciamento da infraestrutura onde a aplicação roda.
8.  **Monitor (Monitorar):** Coleta de métricas e logs para observar o comportamento da aplicação.

O foco do DevOps é garantir que a "esteira" que move o código através desses estágios seja robusta e veloz.

---

### A Perspectiva SRE: O Foco na Confiabilidade em Cada Estágio

Um SRE participa do mesmo ciclo, mas sua principal preocupação é injetar e garantir a **confiabilidade** em cada uma das etapas. O SRE age como um "consultor de confiabilidade" para as equipes de desenvolvimento.

Veja como a atuação do SRE se manifesta em cada estágio:

1.  **Planejamento:** O SRE pergunta: **"Qual o SLO (Objetivo de Nível de Serviço) para esta nova feature?"**. Ele ajuda o time a definir metas de confiabilidade antes mesmo de uma linha de código ser escrita.
2.  **Codificação:** O SRE pode aconselhar sobre as melhores práticas de design para sistemas resilientes (ex: uso de `retries`, `circuit breakers`) e sobre como a aplicação deve expor suas métricas.
3.  **Build/Teste:** O SRE se preocupa com testes de performance, carga e caos (`chaos engineering`), para descobrir os limites da aplicação antes que ela chegue em produção.
4.  **Release/Deploy:** O SRE defende e ajuda a implementar estratégias de implantação seguras, como **Canary Releases** ou **Blue-Green Deployments**, que minimizam o impacto de uma falha. Ele também garante que os `rollbacks` sejam rápidos e automáticos.
5.  **Operação/Monitoramento:** Este é o "habitat natural" do SRE. Ele não apenas consome os dados do monitoramento, mas os utiliza para garantir que os SLOs estão sendo cumpridos. Se o **Error Budget** (orçamento de erros) se esgota, ele tem autoridade para **bloquear novos deploys** até que a estabilidade seja restaurada.

### Conclusão em Tabela

| Estágio do Ciclo | Foco Principal do DevOps | Pergunta Principal do SRE |
| :--- | :--- | :--- |
| **Planejamento** | O que vamos construir e como vamos organizar o trabalho? | Qual é a meta de confiabilidade (SLO) para o que vamos construir? |
| **Codificação/Build** | O código está sendo integrado e construído de forma contínua? | O código está sendo construído de forma resiliente e observável? |
| **Teste** | Os testes funcionais estão passando e a qualidade está garantida? | O sistema sobrevive a testes de carga e cenários de falha? |
| **Deploy** | Conseguimos implantar a nova versão de forma rápida e automatizada? | Conseguimos implantar a nova versão com o mínimo de risco para o usuário? |
| **Operação** | A infraestrutura está funcionando como esperado? | O serviço está cumprindo seu SLO e dentro do Error Budget? |

Em resumo, DevOps constrói a estrada, enquanto o SRE instala os radares, as placas de sinalização e a equipe de resgate para garantir que a viagem pela estrada seja segura e previsível.