# # Fazendo o monitoramento das condições das máquinas

## Visão Geral

Neste projeto, vamos analisar os dados disponíveis, o conjunto de dados foi adquirido por meio de medições em um demonstrador de monitoramento de condição que consiste em um motor de indução CA alimentado por CA monofásico de 230 V 50 Hz usando um capacitor de motor para dar partida e operar o motor. O motor possui carcaça de ventoinha removível e sua ventoinha original é substituída por diferentes ventoinhas impressas em 3D, ambas semelhantes à ventoinha original e com modificações, como pás faltantes. O motor é conectado a um compressor de ar por meio de um eixo de metal com um acessório impresso em 3D que permite fixar um parafuso sem cabeça para criar um desequilíbrio. Cada condição é rotulada com um ID e um rótulo abreviado e uma breve descrição é fornecida.

Você pode conferir o dataset e o projeto na íntegra clicando abaixo:

Link dataset: https://www.kaggle.com/datasets/stephanmatzka/condition-monitoring-dataset-ai4i-2021

Link do código do projeto: https://github.com/gustavoptavares/Monitoramento-AI4I/blob/main/Monitoramento_AI4I.ipynb

## Problema e Solução

Vamos analisar os dados o conjunto de dados adquirido por meio de medições em um demonstrador de monitoramento de condição que consiste em um motor de indução CA alimentado por CA monofásico de 230 V 50 Hz usando um capacitor de motor para dar partida e operar o motor. Contém dados de operação, que cada condição é rotulada com um ID e um rótulo abreviado e uma breve descrição é fornecida, vamos entender, no detalhe, os dados são úteis para monitoramento da máquina, como:

• Enteder o conjunto de dados para entender cada condição de monitoramento da máquina.

• Montar o modelo preditivo de classificação para monitorar cada condição da máquina. 

## O Processo

O primeiro passo do projeto foi adquirir os dados. Utilizamos os dados do portal Kaagle, carregando-o no Google Colab, para a exploração e análise dos dados utilizando a linguagem de programação Python e suas bibliotecas, como Pandas, Matplotlib, Seaborn e Scikit-Learn. Foi feita análise exploratória, visualização dos dados, e foi aplicado o modelo preditivo de classificação, utilizando o algortimo de árvore de decisão, para monitoramento de cada condição.

## Resultados

Os valores das métricas calculadas:

Precisão Geral (Accuracy): 81%

Relatório de Classificação: Inclui precisão, recall e pontuação F1 para cada classe. Este relatório mostra variações no desempenho do modelo entre as diferentes classes.

Matriz de Confusão: Fornece uma visão detalhada das previsões corretas e incorretas para cada classe.

ROC-AUC para Cada Classe:

Classe 0: 0.909

Classe 1: 0.926

Classe 2: 0.968

Classe 3: 1.000

Classe 4: 0.989

Classe 5: 0.936

Classe 6: 0.952

Classe 7: 1.000

ROC-AUC Média Ponderada: 0.960

No relatório de classificação e na matriz de confusão que geramos, as classes foram representadas por rótulos como "c25", "c75", "cap", "off", "on", "out", "unb", "vnt". Cada um destes rótulos corresponde a uma condição ou estado específico.

Estas métricas mostram um desempenho sólido do modelo em várias frentes. O ROC-AUC, em particular, é bastante alto, indicando que o modelo tem uma boa capacidade de diferenciar entre as classes. No entanto, é importante lembrar que a eficácia de um modelo não depende apenas de suas métricas de desempenho, mas também de como ele se encaixa no contexto específico em que será aplicado.

## Conclusões

Para concluir, este modelo de árvore de decisão, com ajuste de hiperparâmetros e validação cruzada, demonstrou ser eficaz para a classificação com base nos dados fornecidos. A análise das métricas de desempenho e da matriz de confusão revelou um bom desempenho geral, mas também destacou áreas onde o modelo poderia ser potencialmente melhorado, especialmente em termos de equilíbrio de desempenho entre as diferentes classes.

Este tipo de modelo e análise pode ser extremamente útil em aplicações de monitoramento de condição, onde a precisão na classificação de diferentes estados ou condições é crucial. A importância dos componentes do PCA também fornece insights valiosos sobre quais características dos dados são mais relevantes para tais previsões.

O modelo mostrou desempenho variado entre diferentes classes, como evidenciado pelo relatório de classificação e pela matriz de confusão. Isso sugere que algumas condições são mais fáceis de prever do que outras, o que pode ser devido à natureza dos dados ou à representatividade das classes. Por exemplo, classes com uma clara distinção nos padrões de frequência de aceleração e som podem ser mais facilmente identificadas pelo modelo.

A alta precisão e valores de ROC-AUC em algumas classes indicam que o modelo é eficaz na detecção de certos padrões que podem representar condições anormais ou estados operacionais específicos. Isso é crucial para sistemas de alerta precoce e manutenção preditiva.

O modelo pode ser adaptado e melhorado continuamente à medida que novos dados são coletados, especialmente em ambientes industriais dinâmicos onde as condições operacionais e os modos de falha podem evoluir.
