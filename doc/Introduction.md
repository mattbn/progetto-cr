# 1. - Introduzione
## 1.1. - Informazioni sul progetto
<ins>**Progetto per l'esame di Calcolatori Elettronici e Reti di Calcolatori**</ins>

Il contenuto della repository è una combinazione di alcuni documenti Markdown e di un Jupyter notebook. Lo scopo del progetto è fornire dati riguardanti i tempi di esecuzione dello stesso algoritmo di ML (*Machine Learning*) su diverse unità di calcolo, in modo da poterli comparare.

La parte di codice include alcune librerie esterne utili per semplificarne lo sviluppo (disponibili sotto le rispettive licenze):
 - [numpy](https://numpy.org/doc/stable/license.html)
 - [pandas](https://github.com/pandas-dev/pandas/blob/main/LICENSE)
 - [Tensorflow](https://github.com/tensorflow/tensorflow/blob/master/LICENSE)

Il Jupyter notebook contenuto nella repository ha al suo interno una spiegazione dettagliata dei vari passaggi dell'algoritmo, per cui essi verranno introdotti solo a grandi linee nei documenti Markdown.

## 1.2. - Tensorflow 2
Il progetto utilizza la libreria [Tensorflow 2](https://www.tensorflow.org) in combinazione con [Keras](https://keras.io) per lo sviluppo e la gestione del modello di ML.
Tensorflow è una popolare libreria per il ML che semplifica enormemente lo sviluppo di modelli e consente l'esecuzione degli stessi sulle Tensor Processing Unit (TPU) di Google.

## 1.3. - Google Colab
La parte applicativa del progetto è strutturata come un Jupyter notebook eseguibile sulla piattaforma [Google Colab](https://colab.research.google.com).
Google Colab mette a disposizione di tutti (è sufficiente avere un account Google), a titolo gratuito (con limiti sulle prestazioni), unità di calcolo direttamente dai datacenter Google.

