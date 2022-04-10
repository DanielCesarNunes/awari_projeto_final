# Projeto Final Data Science Awari - Bank Marketing Data Set

I - Exposição do problema:
  Os dados estão relacionados com campanhas de marketing direto de uma instituição bancária portuguesa. As campanhas de marketing foram baseadas em telefonemas para seus clientes. Muitas vezes, era necessário mais de um contato com o mesmo cliente, para acessar se o produto (depósito a prazo bancário) seria - ou não - subscrito.\n

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
  
  
