# Projeto Final Data Science Awari - Bank Marketing Data Set

I - Exposição do problema:
  Os dados estão relacionados com campanhas de marketing direto de uma instituição bancária portuguesa. As campanhas de marketing foram baseadas em telefonemas para seus clientes. Muitas vezes, era necessário mais de um contato com o mesmo cliente, para acessar se o produto (depósito a prazo bancário) seria - ou não - subscrito.

II - Coleta ou importação dos dados:
  Os dados foram coletados do repositório de dados da UCI - https://archive.ics.uci.edu/ml/index.php.
  
III - Preparação dos dados:
  Foram utilizados métodos de verificação dos dados obtidos:
    * Números de linhas x colunas.
    * Verificação de valores missing.
    * Verificaçao dos tipos de dados.
  Não foram encontrados valores ausentes e nem foram necessárias transformações no dataset nessa fase.

IV - Análise exploratória dos dados:
  Nessa dase foram utilizados métodos estatísticos para obtenção de insights referentes as variáveis independentes quanto a correlação com a variável target.
  Os gráficos criados evidenciam que os dados não seguem uma curva normal e em alguns casos, como as variáveis 'age' e 'day', apresentam mais de uma moda.
  Além disso, as variáveis apresentam uma fraca correlação, sendo as variáveis 'pdays' e 'previous' que tem uma correção mais significativa, com o valor de 0,45.
  
V - Modelagem:
  Para a realização da modelagem, os variáveis independentes categóricas foram transformadas através do método OneHotEncoder e a váriavel independente (por ser categórica também) foi modificada pelo método LabelEncoder, portanto, a saída ficou como um número inteiro - 0 = 'no' e 1 = 'yes'.
  Posteriormente, foi realizada a divisão do dataset em treino e teste na proporção de 80%-20%, respectivamente.
  Os números apresentados possuem escalas diferentes, para a uniformização foi utilizado o StandScaler (proveniente do sklearn.preprocessing).
  Como o problema apresentado se refere à uma variável target com valores "sim" ou "não", ou seja, um problema envolvendo classificação, foi escolhido o modelo de machine learning conhecido como Regressão Logística, por ser um algoritmo "simples" e que atende perfeitamente os requisitos necessários para a realização das futuras predições.
  Primeiramente, foi feito o treinamento do modelo através do dataset de treino:
    from sklearn.linear_model import LogisticRegression
      classifier = LogisticRegression(random_state = 0)
      classifier.fit(X_train, y_train)
  E, posteriormente, a predição com o dataset de teste:
    y_pred_logistic = classifier.predict(X_test)
  Para a avaliação do modelo, foi utiliza a matriz de confusão e a pontuação de acurácia. O valor obtido foi de 89,92%, evidenciando que o modelo utilizado possui boa precisão. Portanto, o modelo de Regressão Logística se mostra confiável para a determinação da subscrição do produto ofertado.
  Ainda assim, para a melhoria do modelo em questão, há a necessidade de testar outros algoritmos de machine learning de classificação, assim como testar o modelo com a combinação das variáveis independentes de formas diversas, com o intuito de observar se o modelo apresentará resultados mais satisfatórios. 
  
