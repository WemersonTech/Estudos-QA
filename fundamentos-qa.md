\# Módulo 1 — Fundamentos de QA



\## O que é Qualidade de Software

Qualidade de software = atende requisitos + é confiável + tem usabilidade aceitável + é mantível. QA (Quality Assurance) é o conjunto de processos e práticas para \*\*prevenir\*\* problemas e garantir que o produto entregue cumpra esses requisitos.



\*\*Resumo prático:\*\* QA não é só testar no final; é criar processos que reduzam a chance de defeitos chegarem ao usuário.



---



\## Diferença entre QA, QC e Testes de Software

\- \*\*QA (Quality Assurance)\*\*: foco no processo (prevenção). Ex.: definir padrões, políticas, revisões e integração de testes no processo.

\- \*\*QC (Quality Control)\*\*: foco no produto (inspeção). Ex.: revisão de deliverables, checkpoints de qualidade.

\- \*\*Testes de Software\*\*: atividades práticas que buscam defeitos (execução, verificação, relatórios).



\*\*Relação:\*\* QA define o processo; QC verifica produtos; testes executam casos e reportam defeitos.



---



\## Custos da Qualidade

Categorias:

\- \*\*Prevenção:\*\* treinamento, revisões de requisitos, automação de build. (mais barato)

\- \*\*Avaliação:\*\* testes, auditorias, avaliações. (custo médio)

\- \*\*Falhas internas:\*\* defeitos encontrados antes do release. (mais caro)

\- \*\*Falhas externas:\*\* defeitos encontrados em produção pelos usuários. (muito caro — perda de cliente, reputação)



\*\*Prática:\*\* priorize prevenção (revisão de requisitos, critérios de aceite, automação básica).



---



\## Importância de prevenir defeitos

\- Corrigir cedo é muito mais barato.

\- Encontrar defeitos em produção causa retrabalho, custo de interrupção e perda de confiança.

\- Cultura: ensinar time a escrever requisitos claros e revisões de pares.



---



\## Ciclo de vida do defeito (Defect / Bug Lifecycle)

Estados comuns (exemplo realista):

1\. \*\*Novo\*\* (registrado)

2\. \*\*Triagem\*\* (avaliado por QA/PO)

3\. \*\*Atribuído\*\* (para dev)

4\. \*\*Em progresso / Em correção\*\*

5\. \*\*Resolvido / Em revisão\*\* (dev marca como resolvido)

6\. \*\*Em teste\*\* (QA verifica correção)

7\. \*\*Reaberto\*\* (se não corrigido)

8\. \*\*Fechado\*\* (confirmado por QA)

9\. \*\*Duplicado / Não é bug / Won't fix\*\* (ocasional)



\*\*Dica prática:\*\* sempre tenha evidências (logs, screenshots, steps). Sem evidência, bug não é confiável.



---



\## Diferença entre Erro, Defeito e Falha

\- \*\*Erro (Error)\*\*: ação humana incorreta (ex.: dev cometeu erro lógico).

\- \*\*Defeito (Bug)\*\*: o resultado do erro no artefato (código, requisito).

\- \*\*Falha (Failure)\*\*: quando o usuário experimenta o problema — comportamento errado em execução.



---



\## Introdução à comunicação de bugs e documentação de teste



\### Princípios ao reportar um bug

\- \*\*Seja objetivo e claro.\*\*

\- \*\*Reproduzível\*\*: passos claros, ambiente, versão, dados.

\- \*\*Impacto\*\*: descreva impacto no negócio/usuário.

\- \*\*Prioridade vs Severidade\*\*: explique por que acha prioridade X e severidade Y.

\- \*\*Evidências\*\*: screenshots, logs, vídeo curto, request/response (API).

\- \*\*Sugestão\*\*: quando possível, dê sugestão de local provável do problema (ex.: validação no front, endpoint X).



\### Modelo mínimo (campo obrigatório)

\- Título sucinto (o que acontece)  

\- Ambiente (ex.: prod/stage, browser e versão, OS)  

\- Versão/build (se aplicável)  

\- Passos para reproduzir (1., 2., 3.)  

\- Resultado esperado  

\- Resultado atual (o que aconteceu)  

\- Evidências (screenshots, logs, request/response)  

\- Severidade (baixa/média/alta/crítica)  

\- Prioridade sugerida (baixa/média/alta)  

\- Quem reportou e data



---



\## Exercícios práticos (faça e registre no repositório)

1\. Abra um site simples (qualquer). Faça um checklist rápido e registre 3 passos para reproduzir um bug hipotético e escreva o bug usando o template do repositório.

2\. Escreva 2 casos de teste manuais para a funcionalidade de login: um positivo e um negativo.

3\. Registre uma breve nota (2–3 linhas) sobre como prevenir o bug hipotético (onde no processo preveniria).



---



\## Referências e leitura (prioridade)

\- \*The Art of Software Testing\* — Glenford Myers (fundamentos de teste)

\- \*Foundations of Software Testing\* — Dorothy Graham et al. (modelos, técnicas)

\- Capítulos relacionados: comece por esses livros para as seções acima.  

\- Nota: as práticas citadas aqui também são práticas de times reais (triagem em Jira, evidências, CI com testes básicos).





