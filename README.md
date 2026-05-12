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

> Resposta: Lembro de ter trabalhado todos os tópicos, porém uns mais do que outros. KNN, teorema de Bayes, correlação, arvores de decisão, matriz de confusão e XGBoost trabalhamos pouco ou quase nada. Das atividades sobre esses tópicos, Lembro de uma sobre regressão linear que consistia em criar um modelo que prevê o preço do aluguel de um imóvel com base nas características do local, como por exemplo a distancia até o metrô, além de outra atividade que consistia em criar um modelo que previa os resultados de partidas de futebol com base em Random Forest ou XGBoost por meio de uma database SQLite, e utilizá-lo para prever o vencedor de um campeonato com base na simulação de Monte Carlo. De forma autonoma consegui fazer a classificação dos dados para treino e testes e também a normalização, as outras partes das implementações só consegui fazer com ajuda de exemplos que o professor passou e utilizando IA. De forma geral acho que deveriamos fazer uma revisão dos assuntos mais básicos, rever sobre indicadores e reforçar os assuntos de classificação, pois nos aprofundamos poucos neles.

## 3. Conceitos essenciais

Responda com suas palavras e dê um exemplo simples.

1. O que é aprendizado supervisionado?
> é quando o modelo aprende com dados que já vêm com a resposta certa. Exemplo: mostrar ao modelo fotos de frutas com um rotulo dizendo “maçã” ou “banana”, para ele aprender a reconhecer novas fotos.
2. O que é uma tarefa de classificação?
> é quando treinamos um modelo para categorizar algo de acordo suas características. exemplo: classificar se um e-mail é spam ou não.
3. O que são features e target?
> são as características de entrada usadas para fazer a previsão. Target é o valor que queremos prever. exemplo: para prever o preço de uma casa, as features podem ser tamanho, número de quartos e bairro; o target é o preço.
4. Para que serve separar treino e teste?
> serve para avaliar o aprendizado do modelo. exemplos: treinar com 80% dos dados e testar com os 20% restantes.
5. O que é overfitting?
> é quando o modelo aprende demais os dados de treino, incluindo ruídos e detalhes irrelevantes, e acaba indo mal em dados novos. Exemplo: um aluno que decora as respostas da lista, mas erra quando a pergunta muda um pouco.
6. Por que acurácia pode ser uma métrica enganosa?
> a acurácia pode ser uma métrica enganosa por que os dados passados para o treinamento podem estar desbalanceados. Exemplo: se 95% dos e-mails são normais e 5% são spam, um modelo que sempre chuta “normal” terá 95% de acurácia, mas será ruim para detectar spam, pois foi treinado com poucos casos de spam.

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
=== Regressão logística ===
Acurácia treino: 0.958
Acurácia teste: 0.958
Precisão teste: 0.947
Recall teste: 0.989
F1-score teste: 0.967
Matriz de confusão:
[[48  5]
 [ 1 89]]
Probabilidades das 5 primeiras amostras de teste:
[[0.01851079 0.98148921]
 [0.99816902 0.00183098]
 [0.17664237 0.82335763]
 [0.23384359 0.76615641]
 [0.19969055 0.80030945]]

=== Árvore de decisão ===
Acurácia treino: 1.000
Acurácia teste: 0.923
Precisão teste: 0.954
Recall teste: 0.922
F1-score teste: 0.938
Matriz de confusão:
[[49  4]
 [ 7 83]]
Probabilidades das 5 primeiras amostras de teste:
[[0. 1.]
 [1. 0.]
 [1. 0.]
 [0. 1.]
 [0. 1.]]
```

### Interpretação

Qual modelo generalizou melhor? Explique usando as métricas e a comparação entre treino e teste.

> Resposta: segundo as métrica de acurácia, o modelo de Regressão logística obteve melhor resultado, pois os valores obtidos nos treinos e testes foram muito próximos(cerca de 95% de acurácia em ambos). isso significa que o desempenho se manteve praticamente igual em dados novos, mostrando que o modelo aprendeu os padrões reais do conjunto de dados sem “decorar” os exemplos de treino. Enquanto no modelo de Árvore de decisão houve um possível overfitting porque ele acertou perfeitamente os dados de treino, mas perdeu desempenho no teste. Além disso o F1-score da regressão logística(0.967 ou 96,7%) foi maior que o da Arvore de decisão(0.938 ou 93,8%), indicando maior equilíbrio entre encontrar os casos positivos e evitar erros nas previsões.

##

## 5. Probabilidade e interpretação

Escolha um dos modelos treinados e responda:

1. O modelo produz probabilidade com `predict_proba()`?
2. O que significa uma probabilidade alta para uma classe?
3. Probabilidade alta garante que a previsão está correta? Explique.
4. Em um problema real, qual seria o risco de confiar cegamente nessa previsão?

> Resposta: sim, tanto a regressão logística quanto a árvore de decisão produzem probabilidades com a função predict_proba(). Uma probabilidade alta para uma classe significa que o modelo tem alto grau de confiança que a amostra pertence a essa classe. Não necessariamente uma probabilidade alta garante que a previsão esteja correta, pois o modelo pode estar confiante, mas errado por várias razões, como dados de treinamento enviesados ou com ruidos, overfitting, etc. Em casos reais, confiar cegamente nessas previsões pode ocasionar sérios prejuízos, como por exemplo em uma aplicação que faz diagnóticos médicos, se um modelo prevê com 99% de certeza que um paciente não tem uma doença grave, mas a previsão está errada (um falso negativo), isso pode levar a um atraso no tratamento e consequências graves para a saúde do paciente.

## 6. Generalização

Compare treino e teste:

1. Há sinal de overfitting?
2. Há sinal de underfitting?
3. O que você tentaria mudar para melhorar o resultado?
4. O que você precisaria estudar melhor para responder com mais segurança?

> Resposta: Sim, no modelo de árvore de decisão podemos ver que a acurácia de treino atingiu 100% e a de teste atingiu 92.3%, caracterizando um possível overfitting. Já na regressão Logística, não há sinal de overfitting, pois as acurácias de treino e teste são idênticas (cerca de 96% em ambas). Apesar disso, ambos os modelos obtiveram acurácias altas, acima dos 90%, descaracterizando um underfitting, mostrando que os modelos não são tão simples a ponto de não conseguirem capturar os padrões e perfomar de forma satisfatória no treino e testes. Uma possivel melhoria para o modelo de árvore de decisão seria "podar" a árvore, limitando a profundidade para evitar que ela crie ramos muito específicos(passando o parametro max_depth). já na regressão logística poderia ser aplicado um escalonamento dos dados utilizando a função StandartScaler() para que o cálculo dos coeficientes para as features estejam na mesma ordem de grandeza.

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
