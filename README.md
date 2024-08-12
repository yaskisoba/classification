# Classificação
Esse desafio foi realizado no google colab disponível [aqui](https://colab.research.google.com/drive/1H_xhxiYjqpIMUC0GfZ1EUOCQz758BXQ3?usp=sharing).

## Questão 1

Realize uma análise exploratória dos dados.

- Existe alguma cidade com taxa de churn significativamente maior? <br>
Sim, Los Angeles com 57 pessoas que deixaram a empresa neste trimestre.

- O churn é mais prevalente entre clientes recentes ou antigos?
Mais recentes, inclusive entre é bem frequente no primeiro mês.

- Quais serviços são menos utilizados? Online Security, seguido de Multiple Lines.

## Questão 2

Árvore de Decisão
- F1 Score: 0.47191011235955055
- Precisão: 0.4681528662420382
- Recall: 0.47572815533980584
- Acurácia: 0.7253756260434057

Floresta Aleatória
- F1 Score: 0.5642857142857143
- Precisão: 0.6294820717131474
- Recall: 0.511326860841424
- Acurácia: 0.7963272120200334

Observando esses resultados, a floresta aleatória superou o modelo de árvore de decisão em todas as métricas.

## Questao 3

Temos dois tipos principais de validação cruzada (cross-validation) chamada de K-Fold Cross-Validation e Leave-One-Out Cross-Validation.
A primeira, que é a que eu decidi usar, divide o dataset em K partes e treina ele K vezes, cada vez que ele usa o conjunto pra teste e o restante para treino.
A segunda é quando cada AMOSTRA do conjunto de dados é usada para teste e o restante pra treino.

No caso desses dois modelos, Árvore de Decisão e Floresta Aleatória, usei a K-Fold Cross-Validation com o K igual a 4, ou seja o dataset foi divido em 4 partes e em cada iteração um subconjunto foi escolhido para ser o de teste.
Em média a floresta aleatória se saiu melhor que a árvore de decisão.

## Questão 4

Ajuda a diminuir o ruído quando ele foca em padrões mais importantes pro modelo, diminui a complexidade computacional quando diminui a densidade do dados (quando o dataset é bem grande fica bem evidente).
