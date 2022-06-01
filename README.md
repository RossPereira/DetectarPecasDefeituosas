# Problema de Negócio e Solução:

**Problema de Negócio:** Lidar com uma linha de produção é algo desafiador, principalmente a questão de lidar com peças defeituosas, por mas que as linhas de montagem sejam automatizadas, na maioria do casos a verificação da qualidade das peças ainda é feita de forma manual.

**Solução proposta:** Pensando em como melhorar essa gargalo será construida uma solução que utliza 2 redes neurais a primeira para identificar se há um problema na peça submetida ao modelo e uma segunda rede para identificar a localização do defeito.

# Bibliotecas Usadas:

* Tensorflow
* Keras
* Scikit learn
* OpenCV
* Numpy
* Seaborn
* MatPlotLib

# Técnicas de Machine Learning:
* Deep Learning
* Transferência de aprendizagem: Rede Resnet
* Divisão de dados: Holdout


# Construção:

Para esse projeto em particular foram usada 2 redes neurais a primeira uma rede neural convolucional para classificação de imagens que contenham peças com defeito que recebeu grande parte da sua arquitetura atráves de um rede neural maior já treinada chamada de Resnet através de transferência de aprendizagem. A Resnet é uma arquitetura de rede neural que foi treinada com uma base de 11 milhoes de imagens chamada imagenet. Já a segunda uma rede neural para segmentação dos defeitos encontrados, também criada usando transferência de aprendizado, porém, utilizando uma variante da Resnet, a ResUnet.

Foram utilizadas duas bases de dados a primeira com imagens de peças com e sem defeito e a segunda com apenas imagens de peças com defeitos mas aplicadas uma mascára para destacar a localização do defeito na peça. Foram feitas algumas análises descritivas para obtenção de informações como o número de imagens de peças com defeito, os tipos de defeitos e a quantidade de imagens por tipo de defeito.

Na primeira rede a Camada de entrada e as camadas ocultas foram transferidas da Resnet, a camada de saída foi personalizada. A primeira rede alcançou uma acurácia de 88%.

