# Plano de Garantia da Qualidade

Este repositório reúne o trabalho de garantia da qualidade que fizemos sobre um sistema web: a auditoria dos artefatos, o teste de usabilidade, as não conformidades que encontramos e as evidências de como cada uma foi tratada até o encerramento.

A ideia aqui não é guardar documento por guardar. É conseguir mostrar, para qualquer pessoa que chegue depois, **o que foi avaliado, o que deu errado, quem foi avisado e como aquilo terminou**.

## O que foi feito

Trabalhamos em cima de um sistema web já existente e seguimos um ciclo bem simples:

1. **Auditamos os artefatos** usando um checklist padrão, item por item.
2. **Registramos as não conformidades** encontradas direto no checklist, com data e hora.
3. **Comunicamos cada NC por e-mail** ao responsável pela correção.
4. **Acompanhamos o retorno.** Quando a resposta não veio ou não resolveu, escalonamos.
5. **Fechamos a NC** só depois da correção confirmada — e guardamos o e-mail de conclusão como prova.
6. **Consolidamos a experiência de uso** no relatório de teste de usabilidade.

O ponto que mais tomou tempo (e o mais interessante) foi o passo 4. Nem toda NC morre no primeiro e-mail: uma delas precisou ser escalonada para outra pessoa até ser efetivamente resolvida, e os checklists nesta pasta mostram exatamente essa progressão.

## A trilha das não conformidades

Os arquivos em `CheckLists de autoria/Checklists/` não são versões alternativas do mesmo documento — eles são a **linha do tempo** do tratamento das NCs. Lendo na ordem, dá para acompanhar a história inteira:

| Momento | Arquivo | O que aconteceu |
| --- | --- | --- |
| 1 | `Checklist com NCs identificadas e enviadas para o email...` | NCs identificadas na auditoria e comunicadas por e-mail, com data e hora do envio registradas. |
| 2 | `Checklist primeira NC resolvida Segunda em espera` | A primeira NC foi corrigida. A segunda seguiu sem resposta. |
| 3 | `Checklist primeira NC resolvida Segunda Escalonada` | Sem retorno, a segunda NC foi escalonada. |
| 4 | `Checklist primeira NC resolvida Segunda Escalonada resolvida` | Escalonamento funcionou: a segunda NC foi resolvida e o ciclo fechou. |

O `Checklist_Auditoria_Vazio.xlsx` é o modelo em branco, para quem quiser repetir a auditoria em outro sistema.

## As evidências

Em `Capturas de Tela - Emails NC/` estão os e-mails que comprovam cada etapa acima. Sem eles, os checklists seriam só afirmação nossa:

- **Envio da NC** — André Gritten comunica a não conformidade a Pedro Brecher.
- **Conclusão da NC** — Pedro Brecher confirma a correção.
- **NC escalonada** — a NC levantada por Eduardo Blasczak é escalonada e resolvida por Gabriela Sartor.

Cada PDF fecha o par "problema comunicado → problema resolvido". É essa amarração que dá rastreabilidade ao processo.

## O relatório de usabilidade

Em `Relatório de Teste de Usabilidade/` está o relatório do teste com usuários, nas versões editável (`.docx`) e final (`.pdf`). Ele consolida as tarefas avaliadas, as dificuldades observadas durante o uso e as recomendações de melhoria.

A cópia em `Documentacao referencia auditoria/` é o mesmo relatório usado como **documento de referência da auditoria** — foi sobre ele que o checklist foi aplicado.

## Estrutura do repositório

```text
PlanoGarantiaQualidade/
├── CheckLists de autoria/
│   ├── Checklist_Auditoria_Vazio.xlsx      # modelo em branco
│   └── Checklists/                         # a evolução do tratamento das NCs
├── Capturas de Tela - Emails NC/           # e-mails: envio, conclusão e escalonamento
├── Documentacao referencia auditoria/      # documento que foi auditado
└── Relatório de Teste de Usabilidade/      # relatório final (.docx e .pdf)
```

## Como ler isso em ordem

Se você está abrindo o repositório pela primeira vez, sugerimos este caminho:

1. Comece pelo **relatório de usabilidade** — é o objeto da avaliação.
2. Abra o **checklist vazio** para entender quais critérios foram aplicados.
3. Percorra os **quatro checklists preenchidos** na ordem da tabela acima.
4. Confira os **e-mails** para ver a comprovação de cada passo.

## O que aprendemos

- **Checklist sem evidência não prova nada.** Marcar "resolvido" na planilha só tem valor com o e-mail correspondente ao lado.
- **Escalonar não é conflito, é processo.** A segunda NC só andou porque foi escalonada — e isso ficou documentado em vez de virar conversa informal.
- **Data e hora importam.** Registrar quando a NC foi enviada é o que permite dizer, depois, se o retorno demorou.

## O que ainda dá para melhorar

- Padronizar os nomes dos arquivos (hoje há espaços, parênteses e um PDF com caracteres quebrados no nome).
- Definir formalmente os critérios de severidade e prioridade das NCs.
- Registrar sistema, versão e ambiente avaliados de forma explícita no relatório.
