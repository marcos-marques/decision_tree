## Decision Tree Classifier

Árvore de decisão é um modelo de aprendizado de máquina utilizado para classificação e regressão. Ele funciona dividindo recursivamente os dados em subconjuntos menores com base nos valores das features de entrada, até que seja atingido um critério de parada. 

Cada divisão resulta em um novo **nó de decisão**, e os nós finais no final da árvore são chamados de **folhas**. O modelo faz previsões para novos dados ao percorrer a árvore da raiz até uma folha, e o valor associado àquela folha é a previsão. As divisões são escolhidas de tal forma que resultem no maior ganho de informação, que mede a redução de incerteza da variável-alvo após a divisão. 
Este processo é repetido até que todas as folhas contenham amostras de apenas uma classe ou seja atingido um critério de parada, como um número mínimo de amostras em uma folha ou profundidade máxima da árvore.

O algoritmo de árvore de decisão usa a ideia de ganho de informação para selecionar as melhores divisões dos dados em cada nó. O ganho de informação é uma medida da incerteza da variável-alvo antes e após uma divisão específica.

### Matemática por trás do algoritmos Desicion Tree


A medida de incerteza comumente usada é a entropia, que é definida como:

```E = -∑ p_i * log2(p_i)```

onde p_i é a proporção de amostras da classe i na divisão.

O ganho de informação é então calculado como a diferença entre a entropia antes da divisão e a média ponderada da entropia após a divisão, onde cada peso é dado pela proporção de amostras em cada sub-divisão:

```G = E_antes - ∑ w_i * E_depois_i```

A divisão que resulta no maior ganho de informação é escolhida como a melhor divisão para o nó atual, e o processo é repetido para cada nó filho até que um critério de parada seja atingido.

O algoritmo de árvore de decisão é baseado na teoria da informação e é amplamente utilizado por ser uma ferramenta poderosa e fácil de usar para a seleção de features e a construção de modelos de classificação ou regressão.
