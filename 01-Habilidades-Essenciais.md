# 01 - Quais habilidades são necessárias para se tornar um Engenheiro DevOps?

Esta página detalha as competências técnicas (hard skills) и comportamentais (soft skills) fundamentais para um Engenheiro DevOps. O objetivo não é ser um especialista em tudo, mas ter uma base sólida em cada uma dessas áreas e se aprofundar nas que forem mais relevantes para o dia a dia.

---

## 🚀 Habilidades Fundamentais (A Base de Tudo)

Estes são os conhecimentos essenciais que sustentam todas as outras práticas de DevOps.

### 1. Linux e Scripting
* **Por quê é importante?** A grande maioria dos servidores na nuvem e em ambientes corporativos roda Linux. É o "chão de fábrica" do DevOps. A habilidade de criar scripts para automatizar tarefas repetitivas é, talvez, a habilidade mais fundamental de todas.
* **Principais Ferramentas/Conceitos:**
    * **Linux:** Navegação no terminal, gerenciamento de processos, permissões de arquivos, usuários e redes.
    * **Scripting:** **Bash/Shell Script** (para automações diretas no sistema operacional) e pelo menos uma linguagem de alto nível como **Python** (extremamente popular para automação, APIs e SDKs de cloud) ou Go.

### 2. Controle de Versão com Git
* **Por quê é importante?** Tudo em DevOps é tratado como código, inclusive a infraestrutura e os pipelines. O Git é a ferramenta universal para versionar, controlar e colaborar em todo esse código.
* **Principais Ferramentas/Conceitos:**
    * **Git:** Comandos essenciais (`clone`, `add`, `commit`, `push`, `pull`, `branch`, `merge`).
    * **Plataformas:** GitHub, GitLab, Bitbucket.
    * **Workflows:** Entender fluxos como GitFlow ou Feature Branch.

### 3. Redes e Sistemas
* **Por quê é importante?** Um Engenheiro DevOps precisa entender como os componentes de um sistema se comunicam. Sem uma base de redes, é impossível configurar firewalls, balanceadores de carga ou resolver problemas de conectividade.
* **Principais Ferramentas/Conceitos:**
    * **Protocolos:** TCP/IP, HTTP/HTTPS, DNS.
    * **Segurança:** Firewalls, Security Groups, VPNs.
    * **Serviços:** Load Balancers, Proxies.

---

## ⚙️ Os Pilares do DevOps

Estas são as práticas centrais que definem o trabalho de DevOps no dia a dia.

### 4. CI/CD (Integração e Entrega Contínua)
* **Por quê é importante?** É o coração do DevOps. O CI/CD automatiza o processo de build, teste e implantação do código, permitindo entregas rápidas e seguras.
* **Principais Ferramentas/Conceitos:**
    * Jenkins, GitLab CI, GitHub Actions, CircleCI.

### 5. Infraestrutura como Código (IaC)
* **Por quê é importante?** Permite que a infraestrutura (servidores, bancos de dados, redes) seja definida, versionada e provisionada através de código, garantindo ambientes consistentes, reprodutíveis e escaláveis.
* **Principais Ferramentas/Conceitos:**
    * **Terraform** (padrão de mercado para provisionamento), Ansible (ótimo para gerenciamento de configuração), AWS CloudFormation.

### 6. Contêineres e Orquestração
* **Por quê é importante?** Contêineres empacotam a aplicação e suas dependências, garantindo que ela rode da mesma forma em qualquer ambiente. Orquestradores gerenciam esses contêineres em escala.
* **Principais Ferramentas/Conceitos:**
    * **Docker** (para criar e rodar contêineres).
    * **Kubernetes (K8s)** (padrão de mercado para orquestração).

---

## ☁️ Ecossistema e Ferramentas Modernas

### 7. Computação em Nuvem (Cloud)
* **Por quê é importante?** A maioria das infraestruturas modernas está na nuvem. Conhecer os principais serviços de um provedor é essencial para construir soluções escaláveis e resilientes.
* **Principais Ferramentas/Conceitos:**
    * **Provedores:** AWS, Azure, Google Cloud (GCP).
    * **Serviços Essenciais:** Máquinas Virtuais (EC2, VM), Armazenamento de Objetos (S3, Blob Storage), Bancos de Dados Gerenciados (RDS, SQL Azure), Redes Virtuais (VPC, VNet).

### 8. Monitoramento e Observabilidade
* **Por quê é importante?** Não basta apenas implantar o software, é preciso saber se ele está funcionando bem em produção. Monitoramento (coletar dados) e Observabilidade (conseguir fazer perguntas a partir dos dados) são cruciais para a estabilidade.
* **Principais Ferramentas/Conceitos:**
    * **Métricas:** Prometheus.
    * **Logs:** ELK Stack (Elasticsearch, Logstash, Kibana), Loki.
    * **Dashboards:** Grafana.

### 9. Segurança (DevSecOps)
* **Por quê é importante?** A segurança é uma responsabilidade de todos e deve ser integrada desde o início do ciclo de vida ("Shift-Left").
* **Principais Ferramentas/Conceitos:**
    * Análise de vulnerabilidades em código e dependências (SAST, DAST, SCA).
    * Ferramentas como Snyk, Trivy.
    * Gerenciamento de segredos com HashiCorp Vault.

---

## 🤝 Habilidades Humanas (Soft Skills)

Tão ou mais importante que as ferramentas, a cultura DevOps depende de como as pessoas interagem.

* **Comunicação e Colaboração:** Você será a ponte entre equipes. Saber ouvir e comunicar ideias de forma clara é fundamental.
* **Resolução de Problemas:** Você será o "detetive" que investiga por que um deploy falhou ou por que o sistema está lento.
* **Adaptabilidade e Vontade de Aprender:** O mundo DevOps muda muito rápido. A ferramenta popular hoje pode não ser a de amanhã. Estar aberto a aprender constantemente é obrigatório.

---
**Dica de Ouro:** Não tente ser um especialista em todas as 200 ferramentas que existem. Foque em entender profundamente os **conceitos** (o que é CI/CD, por que usar IaC). Com uma base conceitual forte, aprender uma nova ferramenta se torna muito mais fácil.