# 08 - Quais são as métricas de sucesso para DevOps e SRE?

Tanto DevOps quanto SRE são disciplinas orientadas a dados. "Não se pode melhorar o que não se pode medir" é um lema que se aplica a ambos. No entanto, eles medem o sucesso através de lentes diferentes: DevOps foca na saúde e eficiência do **processo de entrega**, enquanto SRE foca na saúde e confiabilidade do **serviço em produção**.

---

### A Perspectiva DevOps: As Métricas DORA (Accelerate)

As métricas mais respeitadas e adotadas pela indústria para medir a performance de um time DevOps vêm da pesquisa do grupo DORA (DevOps Research and Assessment), popularizadas no livro "Accelerate". Elas são conhecidas como as 4 métricas DORA e se dividem em duas categorias:

#### 🚀 Métricas de Velocidade (Throughput)

1.  **Deployment Frequency (Frequência de Implantação):**
    * **O que mede:** Com que frequência a organização implanta código em produção.
    * **Por que importa:** Uma alta frequência indica um processo de entrega automatizado, estável e com baixo risco.

2.  **Lead Time for Changes (Tempo de Ciclo para Mudanças):**
    * **O que mede:** O tempo que leva desde o `commit` de um código até ele estar rodando em produção.
    * **Por que importa:** Tempos curtos indicam um processo eficiente, sem gargalos, e que a empresa consegue entregar valor rapidamente.

#### 🛡️ Métricas de Estabilidade

3.  **Change Failure Rate (Taxa de Falha em Mudanças):**
    * **O que mede:** A porcentagem de deploys em produção que resultam em uma falha (ex: causam um incidente, precisam de `rollback`).
    * **Por que importa:** Uma taxa baixa indica que o processo de entrega é de alta qualidade e confiável.

4.  **Mean Time to Recovery (MTTR - Tempo Médio de Recuperação):**
    * **O que mede:** O tempo médio que a equipe leva para restaurar o serviço após um incidente ou falha em produção.
    * **Por que importa:** Um MTTR baixo indica que a equipe é resiliente e capaz de se recuperar rapidamente de problemas, minimizando o impacto no usuário.

O objetivo de um time DevOps é melhorar continuamente essas quatro métricas.

---

### A Perspectiva SRE: SLOs e Error Budgets

A medição de sucesso para um SRE é mais focada na experiência do usuário e na confiabilidade do serviço. O framework para isso é matemático e bem definido:

1.  **SLI (Service Level Indicator - Indicador de Nível de Serviço):**
    * **O que é:** Uma medida quantitativa direta de um aspecto do seu serviço. É a "coisa" que você mede.
    * **Exemplo:** A porcentagem de requisições HTTP que retornaram com sucesso (código 200) em menos de 200ms.

2.  **SLO (Service Level Objective - Objetivo de Nível de Serviço):**
    * **O que é:** A meta que você define para um SLI durante um período. É o "quanto" de sucesso você almeja.
    * **Exemplo:** 99.9% das requisições devem ser bem-sucedidas (SLI) ao longo dos últimos 28 dias.
    * **Importante:** SLOs são metas internas, não contratos com o cliente (isso é um SLA - Service Level Agreement). Um SLO de 100% é irreal e indesejável, pois significa que você não pode inovar ou correr riscos.

3.  **Error Budget (Orçamento de Erros):**
    * **O que é:** A consequência direta do SLO. É `100% - SLO`. É a quantidade de falha que é **aceitável** para o serviço.
    * **Exemplo:** Para um SLO de 99.9%, seu Error Budget é de 0.1%. Isso significa que 0.1% das requisições *podem* falhar naquele período sem que o time seja penalizado.
    * **Por que importa:** O Error Budget é a métrica que une SRE e Desenvolvimento. Se o time está com o orçamento cheio, ele tem "permissão" para correr riscos (lançar novas features). Se o orçamento se esgotou (devido a muitas falhas), **todos os lançamentos de novas features são congelados** e o foco total da equipe se volta para a confiabilidade.

### Como as Métricas se Conectam?

As métricas DevOps e SRE não são concorrentes; elas se alimentam.

* O **Error Budget (SRE)** dá ao time DevOps um guia claro sobre **quando** eles podem aumentar a **Frequência de Deploy (DevOps)**.
* Uma baixa **Taxa de Falha em Mudanças (DevOps)** ajuda a preservar o **Error Budget (SRE)**.
* Um baixo **MTTR (DevOps)** é crucial para se recuperar rapidamente quando um **SLO (SRE)** é violado.

Em resumo, as métricas DORA medem a saúde da "fábrica" (o processo de entrega), enquanto as métricas SRE medem a qualidade e a confiabilidade do "carro" que sai da fábrica (o serviço em produção).