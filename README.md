# Plano de Garantia da Qualidade

Repositório de apoio ao planejamento, à execução e à comprovação das atividades de garantia da qualidade de um sistema web.

O conteúdo está organizado para acompanhar o ciclo de qualidade desde a definição do que será verificado até o registro dos resultados, das não conformidades e das recomendações de melhoria.

## Objetivos

- Padronizar a autoria e a revisão dos casos de teste.
- Registrar os resultados da avaliação de usabilidade do sistema web.
- Manter evidências verificáveis para cada problema identificado.
- Apoiar a comunicação, o acompanhamento e o encerramento de não conformidades.
- Preservar a rastreabilidade entre requisito, teste, resultado, evidência e ação corretiva.

## Visão geral do processo

```text
Especificação do sistema
        |
        v
Autoria dos casos de teste
        |
        v
Auditoria e revisão dos casos
        |
        v
Execução dos testes e avaliação de usabilidade
        |
        v
Registro de resultados e não conformidades
        |
        v
Evidências, comunicação, correção e reteste
        |
        v
Relatório final e recomendações
```

## Processo ponta a ponta

### 1. Preparar a base de avaliação

Antes da execução, reunir a especificação funcional e de design, a versão do sistema, o ambiente de teste, os requisitos aplicáveis e o roteiro de avaliação. Essa etapa define o que será verificado e evita que o resultado fique sem contexto.

**Entrada:** requisitos, especificação de design, versão/build e ambiente.

**Saída:** escopo de avaliação, cenários e critérios de verificação.

### 2. Elaborar os casos de teste

Transformar os requisitos e os cenários de uso em casos de teste reproduzíveis. Cada caso deve permitir que outra pessoa entenda o objetivo, prepare o ambiente, execute os passos e compare o resultado esperado com o resultado obtido.

Sempre que aplicável, registrar:

- identificador e título do caso;
- requisito ou funcionalidade coberta;
- pré-condições e dados de entrada;
- passos de execução;
- resultado esperado;
- resultado obtido;
- situação do teste: aprovado, reprovado, bloqueado ou não executado;
- referência para a evidência e para a não conformidade relacionada.

### 3. Auditar a autoria

Submeter os casos ao checklist de auditoria antes da execução. A revisão deve verificar clareza, completude, consistência, rastreabilidade, ausência de ambiguidade e possibilidade de repetição do teste.

O checklist preenchido deve registrar os itens avaliados, os apontamentos encontrados, o responsável pela revisão, a data e a decisão de aprovação ou devolução para correção.

### 4. Executar os testes e a avaliação de usabilidade

Executar os casos aprovados em um ambiente identificado e registrar o resultado real. Para a avaliação de usabilidade, registrar também as tarefas avaliadas, o perfil dos participantes, as observações, as dificuldades encontradas e as conclusões.

O relatório de usabilidade deve consolidar os achados de forma objetiva, relacionando cada problema à tarefa, ao impacto para o usuário e à recomendação correspondente.

### 5. Registrar não conformidades

Para cada desvio, criar um registro com descrição objetiva do problema, condição observada, comportamento esperado, comportamento atual, impacto, prioridade ou severidade, ambiente, responsável e estado de tratamento.

Uma não conformidade deve ser suficientemente detalhada para permitir reprodução e correção sem depender de explicações informais.

### 6. Preservar e comunicar as evidências

Associar ao registro as evidências pertinentes, como capturas de tela, mensagens de e-mail, logs, resultados de execução ou trechos do relatório. As evidências devem conter contexto suficiente e usar nomes que permitam localizar rapidamente a não conformidade relacionada.

Após a comunicação, acompanhar a correção até o reteste. O encerramento só deve ocorrer quando o resultado corrigido estiver verificado e a evidência final estiver anexada.

### 7. Consolidar os resultados

Ao final do ciclo, consolidar os casos executados, os resultados, as não conformidades abertas e encerradas, os riscos remanescentes e as recomendações. O relatório final deve informar claramente o escopo avaliado, as limitações e a decisão de aceite, quando houver.

## Estrutura do repositório

| Pasta | Finalidade | Conteúdo atual |
| --- | --- | --- |
| `CheckLists de autoria/` | Apoiar a revisão da qualidade dos casos de teste e da documentação produzida. | `Checklist_Auditoria_Vazio.xlsx` |
| `Especificação Design de Software/` | Centralizar a especificação usada como base para os testes. | Pasta disponível para inclusão dos documentos de referência. |
| `Relatório de Teste de Usabilidade/` | Armazenar o relatório editável e sua versão distribuível. | `RA1 - Relatório de Teste de Usabilidade de Sistema Web.docx` e versão PDF correspondente. |
| `Capturas de Tela - Emails NC/` | Preservar evidências de comunicação e tratamento das não conformidades. | Pasta disponível para inclusão das evidências. |

## Artefatos e responsabilidades

| Artefato | Responsabilidade principal | Momento de uso | Resultado esperado |
| --- | --- | --- | --- |
| Especificação de design | Definir a referência do comportamento e da solução. | Preparação | Base de avaliação identificada. |
| Casos de teste | Descrever verificações reproduzíveis. | Autoria e execução | Testes claros, rastreáveis e executáveis. |
| Checklist de auditoria | Verificar a qualidade dos casos e documentos. | Revisão | Aprovação ou apontamentos registrados. |
| Relatório de usabilidade | Consolidar a experiência observada no sistema web. | Execução e análise | Achados, impacto e recomendações. |
| Registro de não conformidade | Controlar desvios e ações corretivas. | Após a identificação do problema | Tratamento e reteste rastreáveis. |
| Evidências | Comprovar o comportamento observado e a correção. | Durante a execução e o reteste | Evidência vinculada ao registro correto. |

## Critérios mínimos de qualidade

Um ciclo pode ser considerado documentado quando:

- o escopo, a versão e o ambiente estão identificados;
- os casos de teste possuem passos e resultados esperados claros;
- os casos foram revisados com o checklist aplicável;
- cada execução possui resultado e evidência quando necessário;
- toda não conformidade possui descrição, impacto, responsável e estado;
- correções foram submetidas a reteste;
- o relatório consolida resultados, limitações e riscos remanescentes.

Os critérios específicos de aprovação, severidade, prioridade, métricas de usabilidade e aceite do produto devem ser definidos pelo responsável pelo projeto antes do próximo ciclo formal.

## Status atual do acervo

O repositório já possui a estrutura básica e o relatório de teste de usabilidade em formatos editável e PDF. Ainda é necessário completar o checklist de auditoria, adicionar a especificação de design, registrar as execuções dos casos de teste e organizar as evidências de não conformidades.

Também é recomendável revisar a nomenclatura do arquivo PDF do relatório, que apresenta caracteres inconsistentes no nome, e adotar uma convenção única de nomes e versões.

## Convenção recomendada para novos arquivos

Use nomes curtos, descritivos e consistentes:

```text
<tipo>-<identificador>-<assunto>-v<versao>.<extensao>
```

Exemplos:

```text
casos-de-teste-CT-001-v1.xlsx
checklist-auditoria-CA-001-v1.xlsx
nao-conformidade-NC-001-evidencia-01.png
relatorio-usabilidade-RA1-v1.pdf
```

Evite espaços, caracteres especiais e nomes genéricos como `final`, `novo` ou `versao2`. Registre a versão e a data no próprio documento quando o formato permitir.

## Próximas ações

- Preencher e versionar o checklist de auditoria.
- Adicionar a especificação de design utilizada como referência.
- Formalizar os casos de teste e sua rastreabilidade aos requisitos.
- Definir critérios de severidade, prioridade, aprovação e aceite.
- Identificar sistema, versão, ambiente, participantes e tarefas no relatório de usabilidade.
- Adicionar as evidências das não conformidades e seus respectivos registros.
- Revisar nomes de arquivos e confirmar qual versão do relatório é a oficial.

## Observação

Este README documenta o fluxo de trabalho representado pela estrutura atual do repositório e explicita os pontos ainda não comprovados pelos artefatos disponíveis. Ele deve ser atualizado sempre que o processo, os responsáveis ou os critérios de qualidade forem formalmente definidos.