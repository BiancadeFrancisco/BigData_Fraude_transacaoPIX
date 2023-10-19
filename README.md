# BigData_Fraude_transacaoPIX

## Descrição Projeto

**Conjunto de dados:** Dataset com informações de transações bancárias, via PIX.
O conjunto de dados inclui as seguintes informações para cada transação:

Detalhes da transação: valor, tempo, remetente e receptor CPF/CNPJ, tipo
Etiqueta de fraude: uma variável binária que indica se a transação foi fraudulenta (1) ou não (0)

**Arquivo:** .json

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

**CRISP-DM:**
1° PREPARAÇÃO DOS DADOS: 
Normalização dos dados: O dataset lido inicialmente está em formato json, realizado ajuste para colunar após, renomeado colunas e descrever estatisticamente os dados;

2° ENTENDIMENTO DO NEGÓCIO E DOS DADOS:
Etapa onde foi encontrado utilidade para os dados levantados, gerado insights para novos conhecimentos sobre o business.

Análise Exploratória de Dados, usando o PySpark para analisar padrões de uso do PIX, como:
- chaves pix mais usadas;
- os valores de transação mais comuns;
- distribuição dos valores de transação por hora e dia;
- quais bancos receberam mais transferências por dia;
- para qual tipo de pessoa (PF ou PJ) foram realizadas mais transações.

Insights:
- Para qual banco esse cliente mais transfere?
- Qual é a média de transferências por período que esse cliente faz?
- Baseando-se no valor das transferências, poderia dar um aumento de crédito?
- Para o que esse cliente mais usa as transferências?
- Executar um algoritmo de machine learning que identifique possíveis transações com fraude.
  
Engenharia de Recursos: Apresentado novas características que podem ser úteis para a detecção de fraudes, tais como o número de transações feitas pelo mesmo remetente em um período de tempo específico.

4° MODELAGEM: Usado o PySpark MLlib e, modelo de Logistic Regression, para treinar e detectar possíveis transações que contenham fraude.

6° AVALIAÇÃO: Avaliado desempenho do modelo para verificar se atingiu todas as necessidades que foram definidas inicialment.
Após treinar o modelo, o mesmo conseguiu prever quase 100% de fraudes, apenas com erro de 2 casos, que a predição indicou erroneamente que não eram fraudes.

5° DEPLOYMENT: 
Foi identificado que o cliente Jonathan Gonsalve tem uma alta taxa de transaferências pix mensal. Através de análise realizadas foi possível perceber que a maior categoria de transação é a transferência bancária.
Também foi possível notar que o segundo banco que o cliente mais transaciona é o banco BTG, porém, o mesmo possui o menor valor transacionado, o que indica que o cliente faz muitas transações de menor valor para esse banco.
Também foi possível verificar que há um alto índice de tentativas de fraude na conta desse cliente, sendo que todas as tentativas de fraude foram com valores acima de R$19.999,00 e com a categoria de transferência. Por isso, foi criado um algoritimo de machine learning que identifica esses tipos de transações que contém fraude.
Conclui-se que há uma alta tentativa de transações com fraude e uma ação possível seria diminuir o limite máximo de transferência de pix do cliente.Possivelmente o cliente esteja usando essa conta PF com propósitos de PJ, devido a alta taxa de transferências s altos valores.  

**IMPORTANTE:**
Em cenário real, é importante identificar:
- Como o dado chega até nós?
- Qual formato virá?
- Aonde o processamento será executado (AWS EMR, Cluster On-Premise)?
- De quanto em quanto tempo eu preciso gerar esse relatório (mensal, diário, near-real time)?
