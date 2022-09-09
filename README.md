# Redes-Neurais
## A Matemática das Redes Neurais Artificiais

Construindo a Rede Neural com Programação e Matemática

Teremos 2 Partes:

- Parte 1 - Vamos construir uma rede neural artificial somente com operações matemáticas
- Parte 2 - Vamos treinar a rede para Prever a Ocorrência de Câncer

## A Arquitetura de Redes Neurais Artificiais

Uma rede neural típica é constituída por um conjunto de neurônios interligados, infuenciando uns aos outros formando um sistema maior, capaz de armazenar conhecimento adquirido por meio de exemplos apresentados e, assim, podendo realizar inferências sobre novos conjuntos de dados. Vejamos a arquitetura de redes neurais artificiais.

As redes neurais são comumente apresentadas como um grafo orientado, onde os vértices são os neurônios e as arestas as sinapses. A direção das arestas informa o tipo de alimentação, ou seja, como os neurônios são alimentados (recebem sinais de entrada). As redes neurais derivam seu poder devido a sua estrutura massiva e paralela e a habilidade de aprender por experiência. Essa experiência é transmitida por meio de exemplos obtidos do mundo real, definidos como um conjunto de características formados por dados de entrada e de saída. Se apresentamos esses dados de entrada e saída à rede, estamos diante de aprendizagem supervsionada e caso apresentemos apenas os dados de entrada, estamos diante de aprendizagem não supervisionada!

O conhecimento obtido pela rede através dos exemplos é armazenado na forma de pesos das conexões, os quais serão ajustados a fim de tomar decisões corretas a partir de novas entradas, ou seja, novas situações do mundo real não conhecidas pela rede. O processo de ajuste dos pesos sinapticos é realizado pelo algoritmo de aprendizagem, responsável em armazenar na rede o conhecimento do mundo real obtido atraves de exemplos. Existem vários algoritmos de aprendizagem, dentre eles o backpropagation que é o algoritmo mais utilizado.

![image](https://user-images.githubusercontent.com/87387315/189378464-b1ef1a84-07e1-42e4-af94-60e3727701a7.png)

Veia que temos umas setas rosas , elas indicam os dados de entrada, Para essa figura você tem 5 atributos, imagina você tem 5 atributos de uma pessoa e você quer preveer se vai pagar o emprestamo. Você alimenta o modelo para cada atributo atravez de uma operação para cada atributo , a operação executada vai ser uma operação de matrices uma que representa cada atributo e outra que representa os pesos, que são os coeficientes. Inicialmente quando empeza o treinamento a gente não sabe quais são os valores de pesose isso o que a gente quer aprender. Então crio uma matriz com os pesos inicializados de forma randomica. Depois multiplico a matriz de pesos pela matriz de valores de entrada. Cada um dessas operações (valor de cada atributo pelo peso), vai gerar uma saída , que são essas zetas intermediarias, 

Cada resultado vai alimentar os proximos circulos cada circulo vai ser chamado de neuronio matemático. Esses resultados iniciais eu passo por uma função chamada de função de ativação, a função mais usada em Deep Learning é a RELU. Essa função pega o resultado da aoperação e observa o resultado é negativo: transforma o valor em zero, o valor e maior o igual a zero e transforma em 1.

Depois de isso eu posso ter outra camada de neuronios matemáticos,Logo multiplico a saida da função de ativação e pelos novos pesos, para poder aplicar novamente a função de ativação. Mentras mais camadas mais tempo. esso processo se repite até ter a previsão do modelo.

Depois eu pego a previsão do modelo e comparo com o valor real, em este caso é um modelo supervisionado. Vamos observar que probavelmente exista erro conhecido como Loss , esse erro vai ajudar indicar a precisão do modelo, Agora eu pego esse erro e faço o caminho de volta. O caminho de ida é o que chamamos de forward propagation e o caminho de volta backward propagation, Precisamos voltar para o inicio para poder mudar os pesos adequados, voltamos n vezes de acordo a quantidade de epocas que queremos treinar o modelo. Para atualizar os pesos precisamos usar o algoritmo Backward propagation usando derivadas. a derivada (gradiente) indica a direção a que eu devo alterar o peso (aumentar o diminuir, a taxa de aprendisaje indica a maginitude se eu devo aumentar o diminuir muito ou pouco. 

## Parâmetros x Hiperparâmetros
Alguns termos  podem parecer confusos  quando  você  começa  a  aprender Machine Learning e Inteligência Artificial.

Há tantos termos a serem usados e muitos dos termos são intercambiáveis. Isto é especialmente verdadeiro se você veio de outro campo de estudo que pode usar alguns dos mesmos termos utilizados em aprendizagem de máquina, mas de forma diferente. E um bom exemplo disso são os termos "parâmetro" e “hiperparâmetro".Não ter uma definição clara para estes termos é uma dúvidacomum para iniciantes.Vamosentãocompreender as diferenças entre esses 2 termos.O que é um parâmetro do modelo?Um parâmetro domodelo é uma variável de que é interna ao modelo e cujo valor pode ser  estimado  a  partir  de  dados.

O  parâmetro  também  costuma  ser  chamado  de  peso  ou coeficiente. 
Suas principais características são:•Eles são requeridospelo modelo parafazer previsões

•Os valores dos parâmetros definem ahabilidade do modelo em resolver seu problema.

•Eles são estimados ou aprendidos a partir de dados.•Muitas vezes, eles nãoprecisam serconfigurados manualmente.

•Eles geralmente são salvos como parte do modelo aprendido.Os parâmetros são fundamentais para algoritmos de aprendizagem de máquina.

Eles são parte do modelo que é construídocom os dados históricos de treinamento.Na literatura de aprendizagem de máquina, podemos pensar no modelo como a hipótese e os parâmetroscomo a adaptação da hipótese a um conjunto específico de dados.Muitas vezes, os parâmetros do modelo são estimados usando um algoritmo de otimização, que é um tipo de pesquisa eficiente através de possíveis valores de parâmetros.Em Estatística e Programação, o termo parâmetro pode ter definições ligeiramente diferentes:Estatística: nas estatísticas, você pode assumir uma distribuição para uma variável, como uma distribuição Gaussiana.

Dois parâmetros da distribuição Gaussiana são a média e o desvio padrão. Isso é válido no aprendizado de máquina, onde esses parâmetros podem ser estimados a partir de dados e usados como parte de um modelo preditivo.Programação: na programação, você pode passar um parâmetro para uma função. Neste caso, um parâmetro é umargumento de função que poderia assumirumvalorde um intervalo de valores. Na aprendizagem demáquina, o modelo específico que você está usando é a função e requer parâmetros para fazer uma previsão sobrenovos dados.

**Estatística:** nas estatísticas, você pode assumir uma distribuição para uma variável, como uma distribuição Gaussiana. Dois parâmetros da distribuição Gaussiana são a média e o desvio padrão. Isso é válido no aprendizado de máquina, onde esses parâmetros podem ser estimados a partir de dados e usados como parte de um modelo preditivo.

**Programação:** na programação, você pode passar um parâmetro para uma função. Neste caso, um parâmetro é umargumento de função que poderia assumirumvalorde um intervalo de valores. Na aprendizagem demáquina, o modelo específico que você está usando é a função e requer parâmetros para fazer uma previsão sobrenovos dados.

Alguns exemplos de parâmetros do modelo incluem:

  •Os pesos em uma rede neural artificial.
  
  •Os vetores de suporte em uma máquina vetorial de suporte.

  •Os coeficientes em uma regressão linear ou regressão logística.

### O que é um hiperparâmetro de um modelo?

Um hiperparâmetro de um modelo é uma configuração externa ao modelo e cujo valor não pode ser estimado a partir de dados.Suas principais características são:

  •Eles são frequentemente usados em processos para ajudar a estimar os parâmetros do modelo.

  •Eles são frequentemente especificados pelo Cientista de Dados.

  •Eles geralmente podem ser configurados usando heurísticas.

  •Eles são frequentemente ajustadospara um determinado problema de modelagem preditiva.

Não temos comoconhecer o melhor valor para um hiperparâmetro em um determinado problema.  Podemos  usar  regras  básicas,  copiar  valores  usados  em  outros  problemas  ou procurar o melhor valor por tentativa e erro.Quando  um  algoritmo  de  aprendizagem  de  máquina  é ajustadopara  um  problema específico, usando por exemplogrid searchou pesquisa aleatória, você está ajustando os hiperparâmetros  do  modelo  para  descobrir  os  parâmetros  do  modelo  que  resultam nas previsões mais precisas.Os hiperparâmetros do modelo são frequentemente referidos como parâmetros do modelo o que acaba gerando confusão. 

Uma boa regra geral para superar essa confusão é a seguinte:**Se você precisa especificar um parâmetro do modelo manualmente, entãoprovavelmente, este é um hiperparâmetro.** Alguns exemplos de hiperparâmetros modelo incluem:

    •A taxa de aprendizado para treinar uma rede neural.

    •Os hiperparâmetros C e sigma para máquinas de vetor de suporte(SVMs).

    •k em k-vizinhos mais próximos.
