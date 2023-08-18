# Atividade - Processo de Mineração - Sprint 2

O arquivo “repairExample.csv” possui as seguintes colunas:

- Case ID;
- Activity;
- Resource;
- Start Timestamp;
- Complete Timestamp;
- Variant;
- Variant index;
- (case) description;
- defectFixed;
- defectType;
- lifecycle:transition;
- numberRepairs;
- phoneType.

As utilizadas para montagem da modelagem do processo na ferramenta disco, foram:

- Case ID;
- Activity;
- Resource;
- Start Timestamp;
- Complete Timestamp;

A seguir, é exibido a representação visual do Mapa de Processos gerado a partir do carregamento dos registros do arquivo "repairExample.csv" na plataforma DISCO. As cores atribuídas às etapas refletem a frequência de ocorrência entre os diferentes casos analisados.

<img src="https://github.com/furlan2803/AtividadesPRM2023.2/assets/99223562/4542e4d5-2350-463e-b948-1c0a3f1f2a71" alt="Descrição da Imagem" width="400"/> 

### 1. Explique o processo com suas palavras com base no Mapa de Processo.

O arquivo contém um total de 16 casos e 12 variações possíveis. As fases compreendidas no fluxo geral do processo incluem as etapas: 1) Registro; 2) Análise de Defeitos; 3) Reparo (Complexo); 4) Teste de Reparo; 5) Informações do Usuário; 6) Arquivar Reparo; 7) Reiniciar Reparo; e 8) Reparo (Simples). Duas etapas compartilham a mesma ordem lógica nos 16 casos: o registro (executado pelo sistema) e a análise de defeitos (efetuada pelo “tester”+ respectivo ID). 

<img src="https://github.com/furlan2803/AtividadesPRM2023.2/assets/99223562/b4cedf91-48d7-48c8-bc6b-15882aecd227" alt="Descrição da Imagem" width="300"/> 

Com base no mapa do processo, é possível deduzir que ele se relaciona a um procedimento de reparo e manutenção de algum produto ou sistema. As etapas desse processo são as seguintes:

1. **Registrar:** O caso é registrado no sistema automaticamente. (Colocar próximos passos)
2. **Analisar Defeito:** O defeito é analisado por um “Tester” específico.
3. **Reparo Complexo:** Se o defeito requer um reparo mais complexo, é  tratado por um dos “Solvers” disponíveis. Esta é a etapa mais demorada, como indicado pelas médias de duração das atividades na plataforma Disco.
4. **Testar Reparo:** Após o reparo, o produto é testado para verificar se o defeito foi solucionado.
5. **Informar Usuário:** O usuário é informado sobre o resultado do reparo.
6. **Arquivar Reparo:** Os detalhes do reparo e seus resultados do teste são arquivados para registro.
7. **Reiniciar Reparo:** Se o teste não passar, o caso pode ser reiniciado para revisão.
8. **Reparo Simples:** Se o defeito for simples, ele pode ser encaminhado para um reparo mais simples e rápido.

Texto de conclusão

### 2. Quantos casos necessitaram um reparo complexo?

Com base nos dados apresentados, foi-se identificado 7 casos que exigem a execução da etapa de reparos complexos: caso 1, caso 100, caso 1001, caso 1006, caso 1009, caso 101 e caso 1011. Cada um destes casos representa uma ocorrência única no processo de reparo complexo.
 
<img src="https://github.com/furlan2803/AtividadesPRM2023.2/assets/99223562/fdd0ad53-6daa-46c4-9277-fd268fc7a48c" alt="Descrição da Imagem" width="300"/> 

### 3. Quantos casos foram arquivados?

Com base nos dados apresentados, foi-se identificado 5 casos que exigem a execução da etapa de arquivar reparo: caso 1, caso 10, caso 100, caso 1000 e caso 101. Cada um destes casos representa uma ocorrência única no processo de arquivar reparo.

<img src="https://github.com/furlan2803/AtividadesPRM2023.2/assets/99223562/c040e0a6-11b0-4071-942a-b7ef81e42105" alt="Descrição da Imagem" width="300"/> 

### 4. Qual recurso teve a menor atuação média em termos de tempo?

O recurso "System" apresenta a menor média de atuação em termos de tempo, com um valor de 0 milissegundos. Sua frequência é observada em 42 instâncias, com uma duração mediana de 0 milissegundos e um intervalo de duração de 0 milissegundos.

![Untitled](https://github.com/furlan2803/AtividadesPRM2023.2/assets/99223562/1be4c94d-603b-4307-846e-977cb8adba59)


### 5. Qual é a atividade mais frequente?

A atividade mais recorrente é o teste reparo, ocorrendo em 21 instâncias. Com uma duração mediana é de 7 minutos, com uma duração média de 7 minutos e 25 segundos, e uma variação de duração de 5 minutos.

![Untitled (1)](https://github.com/furlan2803/AtividadesPRM2023.2/assets/99223562/f98f13a4-93f4-4444-99ac-9425ba8fed65)


### 6. Pense e descreva uma pergunta que um gestor poderia querer responder com base nas informações que essa ferramenta forneceu nesse cenário.

1. Dada a discrepância nas médias de duração de execução das atividades pelos solvers utilizados na etapa reparo complexo, como abordar as diferenças de desempenho entre os solvers c2 (12 minutos), c1 (17 minutos e 30 segundos) e c3 (44 minutos e 30 segundos)? 
2. Quais são os principais fatores que estão contribuindo para o solver c3 ter uma média de duração maior em comparação com os outros solvers? 
3. Que medidas devem ser tomadas para nivelar o desempenho dos solvers, reduzindo a variação nas durações médias e melhorando a eficiência da etapa de reparo complexo?

