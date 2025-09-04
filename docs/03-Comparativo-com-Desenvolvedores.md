# 03 - Qual o comparativo de funções entre Dev, DevOps e SRE?

No desenvolvimento de software moderno, três papéis são fundamentais: o Desenvolvedor de Software, o Engenheiro DevOps e o Engenheiro de Confiabilidade (SRE). Embora trabalhem juntos com o mesmo objetivo final (entregar um ótimo produto), cada um possui um foco, responsabilidades e uma "missão" primária diferente.

---

## Tabela Comparativa de Foco

| Aspecto | Desenvolvedor de Software (Dev) | Engenheiro DevOps | Engenheiro SRE |
| :--- | :--- | :--- | :--- |
| **Foco Principal** | **O Produto.** Construir e melhorar as funcionalidades da aplicação. | **O Processo.** Construir e otimizar o fluxo automatizado que leva a aplicação até o usuário. | **A Produção.** Garantir a confiabilidade, performance e estabilidade da aplicação para o usuário final. |
| **Principal "Inimigo"** | Bugs, complexidade acidental no código, requisitos mal definidos. | Processos manuais, lentidão na entrega, falta de feedback, instabilidade no pipeline. | **Downtime**, latência, erros em produção, trabalho manual repetitivo (`toil`). |
| **Escopo de Atuação**| Do requisito à feature codificada (`commit`). | Do `commit` ao `deploy` bem-sucedido. | Do `deploy` à experiência do usuário final, e de volta como feedback. |
| **Relação com Produção**| "Meu código funciona na minha máquina e passou nos testes." | "Consigo implantar o novo código em produção de forma rápida e segura." | "O novo código **continua** funcionando em produção sob estresse, dentro das metas de confiabilidade (SLOs)." |
| **Métricas Chave** | Qualidade do código, velocidade de desenvolvimento de features. | Frequência de deploy, lead time for changes, taxa de falha. | Uptime, latência, saturação, taxa de erros, cumprimento de SLOs/Error Budgets. |

---

## Uma Analogia: A Equipe de Fórmula 1

Para solidificar a ideia, vamos usar uma analogia com uma equipe de corrida:

* **O Desenvolvedor é o ENGENHEIRO QUE PROJETA O CARRO.**
    Ele projeta o motor, a aerodinâmica e os sistemas eletrônicos. Sua missão é criar o carro mais rápido e inovador possível, com as melhores features para o piloto.

* **O Engenheiro DevOps é a EQUIPE DE PIT STOP E LOGÍSTICA.**
    Ele projeta e otimiza o processo para trocar pneus, reabastecer e fazer reparos em segundos. Ele garante que qualquer melhoria feita no carro (um `commit`) chegue à pista (`produção`) da forma mais rápida e eficiente possível durante a corrida.

* **O Engenheiro SRE é o ENGENHEIRO DE TELEMETRIA E CONFIABILIDADE.**
    Ele fica na sala de controle, monitorando todos os dados do carro em tempo real durante a corrida (temperatura do motor, desgaste dos pneus, consumo). Sua missão é garantir que o carro não apenas seja rápido, mas que ele **termine a corrida**, prevendo falhas, gerenciando o risco e orquestrando a resposta quando algo dá errado.

Cada função é vital. Um carro rápido que quebra não vence. Um pit stop perfeito não salva um carro lento. E uma equipe de telemetria genial não pode fazer nada sem um carro na pista. Eles precisam trabalhar em perfeita harmonia.