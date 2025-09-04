# 01 - Quais as habilidades essenciais para DevOps e SRE?

Este documento detalha as competências fundamentais para Engenheiros DevOps e Engenheiros de Confiabilidade (SREs). Muitas habilidades são compartilhadas, mas o foco e a profundidade exigida podem variar significativamente.

Enquanto o **DevOps** foca no **fluxo e velocidade da entrega**, o **SRE** foca na **confiabilidade e estabilidade da produção**. Isso se reflete nas habilidades de cada um.

---

## Tabela Comparativa de Habilidades

| Habilidade Chave | Foco do Engenheiro DevOps | Foco do Engenheiro SRE (ênfase adicional) |
| :--- | :--- | :--- |
| **Programação e Scripting** | Usa código para **automatizar pipelines e processos**. Proficiência em Python, Bash, Go e linguagens de configuração (YAML, HCL) é essencial. | Usa código para **resolver problemas operacionais em escala**. Exige profundidade similar à de um engenheiro de software, focado em sistemas, performance e automação complexa (auto-remediação). |
| **Sistemas Operacionais (Linux)** | Conhecimento sólido para gerenciar e configurar servidores, permissões e serviços. | Conhecimento **profundo** do Kernel, performance de I/O, `system calls` e depuração em baixo nível para otimizar a performance do sistema. |
| **Redes** | Configurar a infraestrutura de rede (VPCs, Firewalls, Load Balancers) para que as aplicações funcionem. | **Analisar e depurar** o tráfego de rede, entender protocolos a fundo para resolver problemas de latência e conectividade em sistemas distribuídos. |
| **Monitoramento e Observabilidade** | Implementar e manter ferramentas de monitoramento (Prometheus, Grafana, ELK) para coletar dados. | **Projetar a estratégia de observabilidade**. Definir **SLOs e SLIs**, gerenciar **Error Budgets** e criar sistemas que permitam fazer perguntas complexas sobre o estado do sistema. |
| **Infraestrutura como Código (IaC)** | Usar ferramentas como **Terraform** e **Ansible** para provisionar e configurar a infraestrutura de forma consistente. | Usar as mesmas ferramentas, mas com foco em criar uma infraestrutura altamente resiliente, escalável e com mecanismos de recuperação automática. |
| **Contêineres e Orquestração** | Saber usar **Docker** e **Kubernetes** para empacotar e implantar aplicações. | Ter um conhecimento profundo do funcionamento interno do Kubernetes para otimizar o scheduling, a rede e a segurança de clusters em larga escala. |
| **Nuvem (AWS, Azure, GCP)** | Saber usar os serviços da nuvem para construir e implantar a infraestrutura necessária. | Ser um especialista em otimizar o **custo, a performance e a resiliência** dos serviços em nuvem, muitas vezes em escala massiva. |

---

### Habilidades com Ênfase Especial para SREs

Além da profundidade extra nas áreas acima, um SRE geralmente precisa de uma base mais forte em:

* **Sistemas Distribuídos:** Entender os desafios de consistência, disponibilidade e tolerância a falhas (Teorema CAP) é o dia a dia de um SRE.
* **Estrutura de Dados e Algoritmos:** Como SREs frequentemente constroem ferramentas e precisam otimizar sistemas complexos, uma base sólida de ciência da computação é mais exigida do que em muitas funções de DevOps.
* **Ciência de Dados e Estatística (Básico):** Habilidade para analisar tendências em dados de monitoramento, entender distribuições estatísticas (percentis) e tomar decisões baseadas em dados para definir SLOs.

### As Soft Skills Continuam Sendo as Mesmas

Para ambos os papéis, as habilidades humanas de **comunicação, colaboração, resolução de problemas e adaptabilidade** são absolutamente essenciais.

---

**Conclusão:** Um SRE pode ser considerado um tipo de Engenheiro DevOps altamente especializado, com um foco obsessivo em métricas de confiabilidade e uma abordagem de engenharia de software para todos os problemas de operações.