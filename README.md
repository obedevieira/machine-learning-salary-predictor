Projeto de Previsão de Salário com Machine Learning

Este projeto demonstra a construção de um modelo de machine learning para prever o salário de um profissional com base em seus anos de experiência. O notebook abrange todo o ciclo de vida de um projeto de ciência de dados, desde a análise exploratória dos dados até a implantação de um modelo preditivo.

Visão Geral e Metodologia
O objetivo principal deste estudo é resolver um problema de regressão: prever o salário de um indivíduo a partir de sua experiência profissional. Para isso, foi utilizado um conjunto de dados que estabelece a relação entre anos de experiência e o salário. O projeto seguiu uma metodologia estruturada em etapas para garantir um fluxo de trabalho robusto e uma análise completa:

Análise Exploratória de Dados (EDA): A análise inicial incluiu a verificação de dados nulos, a dimensão do conjunto de dados e a análise estatística descritiva. Foram criados gráficos como kdeplot e boxplot para entender a distribuição das variáveis 'Renda' e 'Xp' (anos de experiência). A correlação entre as variáveis foi visualizada com scatterplot, regplot e heatmap. A análise revelou uma forte correlação positiva entre os anos de experiência e o salário, indicando que a regressão linear seria um bom ponto de partida. Além disso, a análise de boxplots foi fundamental para identificar a ausência de outliers significativos, garantindo a qualidade do dataset.

Pré-processamento e Modelagem: Foi utilizado um pipeline da biblioteca scikit-learn para padronizar os dados com StandardScaler e treinar os modelos de regressão de forma sequencial. Esta abordagem garante um fluxo de trabalho organizado e robusto, facilitando a reprodutibilidade e a aplicação das transformações de forma consistente.

Comparação de Modelos: O desempenho de três modelos de regressão — Regressão Linear, Ridge e Lasso — foi comparado. As previsões foram avaliadas usando as métricas Mean Squared Error (MSE) e o coeficiente de determinação (R 
2
 ). O fato de todos os modelos apresentarem resultados semelhantes, com um R 
2
  de aproximadamente 0.90, sugere que a relação entre as variáveis é majoritariamente linear, e que modelos mais simples já são altamente eficazes para este conjunto de dados.

Ajuste de Hiperparâmetros: Para otimizar os modelos de Ridge e Lasso, foi utilizado o GridSearchCV para encontrar o melhor valor para o hiperparâmetro alpha. Embora não tenha resultado em uma melhoria significativa no desempenho final neste caso, a demonstração desta técnica é uma habilidade valiosa e crítica para aprimorar o desempenho em datasets mais complexos e com maior dimensionalidade.

Implantação e Demonstração: O modelo de Regressão Linear, que apresentou o melhor desempenho, foi salvo em um arquivo .pkl usando a biblioteca joblib. Para demonstrar a aplicação prática do modelo, foi criada uma interface interativa com ipywidgets que permite aos usuários inserir anos de experiência e obter uma previsão de salário em tempo real. Esta etapa é crucial, pois valida o modelo na prática e mostra como um protótipo pode ser facilmente transformado em uma ferramenta útil.

Insights Chave
Relação Linear Robusta: A forte correlação positiva entre anos de experiência e salário, visualizada na EDA, indica que um modelo de regressão linear simples é altamente eficaz para capturar a tendência dos dados.

Modelos de Regularização: O uso de Ridge e Lasso demonstrou que, mesmo em um conjunto de dados simples, a metodologia de teste de múltiplos modelos é a melhor prática para garantir a escolha da solução mais adequada. Neste caso, a simplicidade da Regressão Linear foi a vencedora.

Fluxo de Trabalho Reproduzível: A utilização de pipelines e o salvamento do modelo em um arquivo .pkl garantem que o processo seja totalmente reproduzível, o que é fundamental para a transição de um projeto de pesquisa para um ambiente de produção.

Valor de Negócio: O projeto culmina em uma ferramenta interativa que pode servir de base para um aplicativo de RH, ajudando na definição de faixas salariais e na negociação de remunerações.

Conclusão e Próximos Passos
Este projeto demonstra a aplicação de ponta a ponta de técnicas de machine learning para resolver um problema de regressão. As habilidades demonstradas, como a criação de pipelines, a comparação de modelos, o ajuste de hiperparâmetros e a implantação de modelos, são fundamentais para um cientista de dados. O modelo desenvolvido pode ser uma ferramenta útil para profissionais de RH e para indivíduos que desejam ter uma ideia de sua faixa salarial com base em sua experiência.

Para futuros aprimoramentos, o projeto pode ser expandido com a exploração de mais variáveis (como área de atuação, nível de educação ou certificações) ou com a aplicação de modelos mais complexos, como Redes Neurais, para verificar se o desempenho pode ser aprimorado em cenários com mais complexidade e não-linearidade.

Autor: Obede Vieira dos Santos

LinkedIn: www.linkedin.com/in/obede-vieira-dos-santos-981303324

Email: obedefactor@gmail.com

Tecnologias: Python, pandas, numpy, scikit-learn, matplotlib, seaborn, ipywidgets, joblib.