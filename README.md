# BigData_Fraude_transacaoPIX

## Descrição Projeto

**Conjunto de dados:** Dataset com informações de transações bancárias, via PIX.
O conjunto de dados inclui as seguintes informações para cada transação:

Detalhes da transação: valor, tempo, remetente e receptor CPF/CNPJ, tipo
Etiqueta de fraude: uma variável binária que indica se a transação foi fraudulenta (1) ou não (0)

**Arquivo:** .json

**CRISP-DM:**
1° PREPARAÇÃO DOS DADOS: ajustado e normalizado os dados do arquivo .json, renomeado colunas e descrever estatisticamente os dados.
2° MODELAGEM: Etapa onde foi encontrado utilidade para os dados levantados, gerado insights para novos conhecimentos sobre o business.
Insights:
- Para qual banco esse cliente mais transfere?
- Qual é a média de transferências por período que esse cliente faz?
- Baseando-se no valor das transferências, poderia dar um aumento de crédito?
- Para o que esse cliente mais usa as transferências?
- Executar um algoritmo de machine learning que identifique possíveis transações com fraude.
3° AVALIAÇÃO MODELO: Avaliado desempenho do modelo para verificar se atingiu todas as necessidades que foram definidas inicialmente.

**Objetivo:**
- Limpar e pré-processar os dados das transações PIX
- Analisar padrões de uso do PIX, tais como os canais mais utilizados e os valores de transação mais comuns
- Usar o PySpark MLlib para treinar e avaliar um modelo de detecção de fraude
- Avaliar o desempenho do modelo

**IDE:** Colab

**Linguagem:** Python

**Principais bibliotecas utilizadas:**

- PySpark, para explorar e analisar big data.

**Aprendizado de Máquina**: 
- Logistic Regreesion

**Obs:**
1° Normalização dos dados: O dataset lido inicialmente está em formato json, realizado ajuste para colunar;

2° Análise Exploratória de Dados: Usado o PySpark para analisar padrões de uso do PIX, como:
- chaves pix mais usadas;
- os valores de transação mais comuns;
- distribuição dos valores de transação por hora e dia;
- quais bancos receberam mais transferências por dia;
- para qual tipo de pessoa (PF ou PJ) foram realizadas mais transações.
  
3° Engenharia de Recursos: Apresentado novas características que podem ser úteis para a detecção de fraudes, tais como o número de transações feitas pelo mesmo remetente em um período de tempo específico.

4° Modelagem: Usado o PySpark MLlib para treinar e detectar possíveis transações que contenham fraude.

**Resultado**: Após treinar o modelo, o mesmo conseguiu prever quase 100% de fraudes, apenas com erro de 2 casos, que a predição indicou erroneamente que não eram fraudes.


  
