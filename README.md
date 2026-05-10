[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/ARkoM8Jo)

# Diagnóstico de retomada - Aprendizado de Máquina

Esta atividade serve para mapear o que você já domina em Aprendizado de Máquina depois das atividades anteriores da disciplina.

Responda individualmente. Use suas palavras. Rode o código quando possível. Se usar IA depois da primeira tentativa, registre o uso na seção 8.

Prazo: 11/05/2026 às 23:59, horário de Fortaleza.

## 1. Mapa do que eu lembro

Marque cada tópico como: lembro bem, lembro parcialmente, não lembro, nunca vi ou não tenho certeza.

- vetores, matrizes e produto escalar: lembro bem
- média, desvio padrão e correlação: lembro parcialmente
- probabilidade condicional e Teorema de Bayes: não lembro
- regressão linear: lembro bem
- classificação supervisionada: não lembro
- treino, teste e validação: lembro bem
- normalização ou padronização de dados: lembro parcialmente
- KNN: não lembro
- árvore de decisão: não lembro
- matriz de confusão: não lembro
- acurácia, precisão, recall e F1-score: lembro parcialmente
- overfitting e underfitting: não lembro
- validação cruzada: não lembro
- Random Forest: não lembro
- XGBoost ou boosting: lembro parcialmente
- `predict_proba()`: lembro parcialmente
- SQL/ETL aplicado a dados: lembro parcialmente
- simulação de Monte Carlo: lembro bem

## 2. O que foi trabalhado antes

Explique, em 8 a 12 linhas:

1. quais desses tópicos você lembra de ter trabalhado na disciplina;
2. quais atividades ou exemplos você lembra;
3. o que você conseguiu fazer com autonomia;
4. o que você só conseguiu fazer seguindo roteiro;
5. qual assunto precisa ser retomado com mais urgência.

Resposta: Lembro de ter trabalhado todos os tópicos, porém uns mais do que outros. KNN, teorema de Bayes, correlação, arvores de decisão, matriz de confusão e XGBoost trabalhamos pouco ou quase nada. Das atividades sobre esses tópicos, Lembro de uma sobre regressão linear que consistia em criar um modelo que prevê o preço do aluguel de um imóvel com base nas características do local, como por exemplo a distancia até o metrô, além de outra atividade que consistia em criar um modelo que previa os resultados de partidas de futebol com base em Random Forest ou XGBoost por meio de uma database SQLite, e utilizá-lo para prever o vencedor de um campeonato com base na simulação de Monte Carlo. De forma autonoma consegui fazer a classificação dos dados para treino e testes e também a normalização, as outras partes das implementações só consegui fazer com ajuda de exemplos que o professor passou e utilizando IA. De forma geral acho que deveriamos fazer uma revisão dos assuntos mais básicos, rever sobre indicadores e reforçar os assuntos de classificação, pois nos aprofundamos poucos neles.

## 3. Conceitos essenciais

Responda com suas palavras e dê um exemplo simples.

1. O que é aprendizado supervisionado?
2. O que é uma tarefa de classificação?
3. O que são features e target?
4. Para que serve separar treino e teste?
5. O que é overfitting?
6. Por que acurácia pode ser uma métrica enganosa?

## 4. Diagnóstico prático com Scikit-Learn

No arquivo `diagnostico_ml.py`, use o dataset `load_breast_cancer` do Scikit-Learn e faça:

1. carregue os dados;
2. separe `X` e `y`;
3. divida em treino e teste;
4. treine uma regressão logística;
5. treine uma árvore de decisão;
6. mostre matriz de confusão, acurácia, precisão, recall e F1-score para cada modelo;
7. compare o desempenho em treino e teste;
8. escreva aqui qual modelo generalizou melhor e por quê.

Se não conseguir terminar tudo, registre até onde chegou e qual erro apareceu.

### Resultados

Cole aqui os principais resultados do seu código.

```text

```

### Interpretação

Qual modelo generalizou melhor? Explique usando as métricas e a comparação entre treino e teste.

Resposta:

## 5. Probabilidade e interpretação

Escolha um dos modelos treinados e responda:

1. O modelo produz probabilidade com `predict_proba()`?
2. O que significa uma probabilidade alta para uma classe?
3. Probabilidade alta garante que a previsão está correta? Explique.
4. Em um problema real, qual seria o risco de confiar cegamente nessa previsão?

Resposta:

## 6. Generalização

Compare treino e teste:

1. Há sinal de overfitting?
2. Há sinal de underfitting?
3. O que você tentaria mudar para melhorar o resultado?
4. O que você precisaria estudar melhor para responder com mais segurança?

Resposta:

## 7. Ponto de dificuldade

Escolha um tópico da lista inicial e escreva:

1. o que você entende dele;
2. onde você se confunde;
3. que tipo de explicação ajudaria: exemplo no quadro, notebook guiado, exercício curto, revisão matemática, visualização ou projeto pequeno.

Resposta:

## 8. Uso de IA, se houver

Se você usou IA depois da primeira tentativa, registre:

```text
Pergunta feita:
Resumo da resposta:
Como eu verifiquei:
O que eu alterei na minha resposta:
O que ainda não entendi:
```

## Submissão no Moodle

Depois de finalizar, copie no Moodle:

```text
Repositório:
Commit final:
Autoavaliação: nível atual, maior dificuldade e tópico que precisa ser retomado.
```
