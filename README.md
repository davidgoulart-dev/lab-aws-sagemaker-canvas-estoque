# 📊 Previsão de Estoque Inteligente na AWS com [SageMaker Canvas](https://aws.amazon.com/pt/sagemaker/canvas/)




## 🚀 Passo a Passo

### 1. Selecionar Dataset
-   Escolhi o dataset que usei para treinar meu modelo de previsão de estoque.
-   Fiz o upload do dataset no SageMaker Canvas.

### 2. Construir/Treinar

-   No SageMaker Canvas, importei o dataset que você selecionou.
-   Configurei as variáveis de entrada e saída de acordo com os dados.
-   Iniciei o treinamento do modelo. Isso leva algum tempo, dependendo do tamanho do dataset.

### 3. Analisar

-   Após o treinamento, examinei as métricas de performance do modelo.
-   Verifiquei as principais características que influenciam as previsões.
![sagemaker](https://github.com/davidgoulart-dev/lab-aws-sagemaker-canvas-estoque/assets/119085211/ceeac1f6-04f3-4239-a56a-1fdf644ceb74)
Ao avaliar a performance de um modelo de previsão, diversas métricas entram em jogo, cada uma com suas vantagens e desvantagens. Entre as mais comuns, encontramos Avg. wQL, MAPE, WAPE, RMSE e MASE. Mas o que elas realmente significam e como interpretá-las de forma eficaz?

1. Avg. wQL (Perda Média Ponderada por Quantil):

Imagine uma competição de tiro ao alvo. O Avg. wQL mede a distância média ponderada entre seus chutes e o centro do alvo. Ponderada? Sim, porque ele leva em conta a importância de cada erro. Erros maiores em áreas cruciais (como o centro do alvo) são penalizados mais do que aqueles na periferia.

2. MAPE (Erro Percentual Absoluto Médio):

Essa métrica calcula a diferença média entre os valores previstos e reais, expressa como uma porcentagem. É útil para comparar a precisão em diferentes magnitudes, pois normaliza os erros. Imagine prever vendas: um erro de R$10 em um item de R$100 é mais significativo do que um erro de R$10 em um item de R$1.000.

3. WAPE (Erro Percentual Absoluto Ponderado):

Similar ao MAPE, o WAPE calcula a diferença média entre valores previstos e reais, porém com uma ponderação adicional. Essa ponderação considera a importância de cada ponto de dados, tornando-o mais adequado para séries temporais com grandes picos ou flutuações sazonais.

4. RMSE (Raiz do Erro Quadrático Médio):

Essa métrica mede a distância média entre os valores previstos e reais, elevando os erros ao quadrado antes de calcular a média. Essa elevação penaliza mais os erros maiores, tornando o RMSE útil para identificar grandes discrepâncias.

5. MASE (Erro Escalado Absoluto Médio):

O MASE compara o erro médio absoluto do seu modelo com um modelo de referência simples, como a média das séries temporais. Essa comparação normaliza o erro e o torna independente da escala dos dados, facilitando a comparação entre diferentes séries temporais.

Interpretando as Métricas:

Valores baixos em todas as métricas indicam um bom desempenho do modelo.
Avg. wQL e WAPE: Foque na distribuição dos erros. Valores baixos com distribuição uniforme indicam boa performance.
MAPE: Útil para comparações entre magnitudes. Valores baixos (< 10%) geralmente indicam boa precisão.
RMSE: Ideal para identificar grandes erros. Valores baixos indicam boa performance.
MASE: Compare com um modelo de referência simples. Valores próximos a 0 indicam boa performance.
Lembre-se:

Nenhuma métrica é perfeita. Escolha as que melhor se adequam ao seu problema e objetivos.
Analise as métricas em conjunto. Uma métrica isoladamente pode não fornecer uma visão completa da performance.
Considere o contexto do problema. Interprete as métricas com base no conhecimento do seu negócio e dos dados.

### 4. Prever

-   Usei o modelo treinado para fazer previsões de um produto do estoque.
![single_prediction_results (1)](https://github.com/davidgoulart-dev/lab-aws-sagemaker-canvas-estoque/assets/119085211/14947cac-c0a1-4da1-a54f-a8741cda467c)
analise preditiva do estoque de um produto.
p50= num cenário médio
p10= num cenário ruim
p90= num cenário bom, ou seja o melhor resultado.



