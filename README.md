# ColabIntro
Repositório para a disciplina de Introdução

Texto Explicativo:

1- Importação das bibliotecas:

A biblioteca TensorFlow é importada como "tf".
Os módulos "datasets", "layers" e "models" são importados da biblioteca "tensorflow.keras".
A biblioteca Matplotlib é importada como "plt".

2- Carregamento dos dados:

O conjunto de dados CIFAR-10 é carregado usando a função "datasets.cifar10.load_data()".
As imagens de treinamento, os rótulos de treinamento, as imagens de teste e os rótulos de teste são atribuídos a variáveis correspondentes.
Os valores dos pixels das imagens são normalizados dividindo-os por 255.0.

3- Visualização das imagens:

É criada uma figura com tamanho 10x10 usando o Matplotlib.
Um loop é executado 25 vezes para preencher cada subplot da figura.
Cada subplot mostra uma imagem de treinamento usando a função "plt.imshow()" e exibe o rótulo correspondente.

4- Construção do modelo de rede neural:

Um modelo sequencial vazio é criado usando "models.Sequential()".
Camadas de convolução ("Conv2D") e pooling máximo ("MaxPooling2D") são adicionadas ao modelo.
As camadas são empilhadas usando "model.add()".
Um resumo detalhado da arquitetura do modelo é exibido usando "model.summary()".

5- Compilação e treinamento do modelo:

O modelo é compilado com um otimizador ("adam"), uma função de perda (entropia cruzada categórica esparsa) e uma métrica (acurácia).
O modelo é treinado usando os dados de treinamento e os parâmetros especificados.
O histórico do treinamento é armazenado na variável "history".

6- Visualização do desempenho do treinamento:

A acurácia do treinamento e da validação ao longo das épocas é plotada usando "plt.plot()".
Os rótulos dos eixos são definidos e uma legenda é adicionada ao gráfico.

7- Avaliação do modelo nos dados de teste:

A perda e a acurácia do modelo nos dados de teste são avaliadas usando "model.evaluate()".
A acurácia do teste é impressa na tela.

8- Previsão de uma imagem de teste:

Uma imagem de teste é selecionada e reformulada para ter a forma correta.
O modelo faz uma previsão utilizando "model.predict()".
A matriz de probabilidades resultante é impressa na tela.
