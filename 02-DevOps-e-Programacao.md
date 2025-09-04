# 02 - Um Engenheiro DevOps Sabe Programar?

A resposta curta é: **Sim, e muito bem.**

No entanto, o *tipo* de programação e o *foco* do código escrito por um Engenheiro DevOps são geralmente diferentes dos de um Desenvolvedor de Software. Entender essa diferença é fundamental.

---

### O Foco Não é a Aplicação, Mas Sim a Automação

Um **Desenvolvedor de Software** tradicionalmente escreve código que se torna o produto final: as funcionalidades de um site, a lógica de negócio de um aplicativo, a interface de um programa.

Um **Engenheiro DevOps**, por outro lado, usa a programação como uma **ferramenta para construir, automatizar e manter a infraestrutura e os processos** que permitem que o código do desenvolvedor seja entregue de forma rápida e confiável.

O código do Engenheiro DevOps é a "fábrica"; o código do Desenvolvedor é o "carro" que sai da fábrica.

### Onde um Engenheiro DevOps Usa Programação no Dia a Dia?

A programação é aplicada em praticamente todas as tarefas de um profissional de DevOps. Aqui estão os exemplos mais comuns:

* **1. Scripts de Automação:**
    * **O quê?** Criar scripts para automatizar tarefas repetitivas, como fazer backups, verificar a saúde de um sistema, limpar arquivos temporários ou orquestrar processos complexos.
    * **Linguagens Comuns:** **Python** (a mais popular, pela sua versatilidade e bibliotecas), **Bash/Shell Script** (essencial para interagir com o Linux) e **Go** (crescendo em popularidade pela sua performance).

* **2. Infraestrutura como Código (IaC):**
    * **O quê?** Definir toda a infraestrutura (servidores, redes, bancos de dados) em arquivos de código. Isso permite que a infraestrutura seja criada, destruída e gerenciada de forma automatizada e versionada.
    * **Linguagens/Ferramentas:** **HCL** (linguagem do Terraform), **YAML** ou **JSON** (usados no AWS CloudFormation).

* **3. Pipelines de CI/CD:**
    * **O quê?** Escrever o "código do pipeline" que define os passos para compilar, testar e implantar uma aplicação.
    * **Linguagens/Ferramentas:** **YAML** (usado no GitLab CI, GitHub Actions, Azure DevOps), **Groovy** (usado nos Jenkinsfiles).

* **4. Gerenciamento de Configuração:**
    * **O quê?** Escrever código que garante que os servidores estejam configurados da maneira correta, com os softwares e as versões necessárias instalados.
    * **Linguagens/Ferramentas:** **YAML** (usado nos playbooks do Ansible), **Ruby** (usado nos cookbooks do Chef).

* **5. Interação com APIs e SDKs:**
    * **O quê?** Criar pequenas ferramentas ou scripts para interagir com as APIs dos provedores de nuvem (AWS, Azure, GCP) ou de outras ferramentas, a fim de extrair informações ou automatizar ações.
    * **Linguagens Comuns:** **Python** é o rei aqui, graças a bibliotecas como `boto3` para a AWS.

### Conclusão

Sim, programar é uma habilidade **não negociável** para um Engenheiro DevOps. No entanto, o foco raramente é em algoritmos complexos ou na interface do usuário. A programação para um Engenheiro DevOps é uma **ferramenta para resolver problemas de infraestrutura, automação, eficiência e confiabilidade.**