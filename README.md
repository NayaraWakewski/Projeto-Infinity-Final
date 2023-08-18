# Projeto Infinity Curso Data Science - Encerramento
Projeto Final de Encerramento do Curso de Data Science da Infinity School

![texto alt](https://cdn.eadplataforma.app/client/infinityschool/upload/others/e993f6d822d15efdb3585d1b733e4020.png)


# Análise de Dados dos Twitters do Presidente Lula e Ex-Presidente Bolsonaro.

Este é um repositório que contém informações e ferramentas para análise de dados e a construção de um Modelo de Aprendizado de Maquina. Esse projeto faz parte do encerramento do Curso de Data Science da Infinity School.


## ⚙️ Instalando as Bibliotecas necessárias.

**Importando as Bibliotecas**: Nesta etapa, importamos as bibliotecas necessárias para execução do Projeto. Trabalharemos com: 

**pandas as pd:** Para manipulação e análise de dados tabulares.

**matplotlib.pyplot as plt:** Para criação de visualizações gráficas.

**datetime:** Para manipulação de datas e horários.

**nltk:** Para processamento de linguagem natural.

**nltk.corpus.stopwords:** Lista de palavras irrelevantes (stop words) da NLTK.

**nltk.tokenize.word_tokenize:** Para dividir um texto em palavras individuais (tokenização).

**re:** Para trabalhar com expressões regulares e padrões de texto.

**wordcloud.WordCloud:** Para gerar nuvens de palavras.

**collections.Counter:** Para contar elementos em uma coleção.

**plotly.express as px:** Para criar visualizações interativas.

**plotly.offline as pyo:** é um módulo da biblioteca Plotly que permite criar gráficos interativos e visualizações utilizando Python, que podem ser exibidos diretamente no ambiente local, sem a necessidade de uma conexão com a internet.

Além disso, há o uso de funções nltk.download() para fazer o download de recursos específicos do NLTK, como a lista de stop words e o tokenizador.


## 🚀 Começando - ANÁLISE DE DADOS.

Nesta primeira parte do projeto, realizamos a análise de dados dos Twitters do Presidente Lula e do Ex-Presidente Bolsonaro. O objetivo é extrair alguns insights a partir desses dados e identificando tendências.

1. **Dataframe**: Após a instalação das bibliotecas importamos os arquivos JSON 'LulaOficial.json' e 'jairbolsonaro.json' e transformamos em dataframe.

2. **Formatando a coluna de DATA**: Para uma melhor análise de dados, formatamos a coluna data, tanto a nivel de formatação, como para o tipo datetime.

3. **Selecionando as Colunas para Análises**: Nesta etapa, selecionamos apenas colunas importantes para este projeto, que foram: ['created_at', 'full_text', 'display_text_range', 'favorite_count', 'retweet_count'].

4. **Contagem Total dos Twitters**: Esta análise realiza a contagem total de tweets ao longo do tempo, bem como a média de retweets e favoritos para os políticos Lula e Bolsonaro. Ele converte as colunas 'created_at' em objetos de data e hora, contabiliza o número de tweets por mês para cada político, calcula as médias de retweets e favoritos para ambos os políticos e imprime os resultados.
O resultado final inclui a contagem total de tweets por mês para Lula e Bolsonaro, seguido das médias de retweets e favoritos para cada um deles. São gerado gráficos e o código usa plt.tight_layout() para garantir uma boa distribuição dos subplots e, em seguida, plt.show() para exibir os gráficos. Isso permite visualizar as tendências ao longo do tempo na contagem de tweets e comparar as médias de retweets e favoritos entre os políticos Lula e Bolsonaro.

5. **Análise de Dados (Engajamento Twitter) - GRÁFICO DE LINHAS**: Essa etapa calcula o engajamento (soma de retweets e favoritos) para os políticos Lula e Bolsonaro, cria um DataFrame consolidado para o gráfico, converte a coluna 'created_at' para datetime, filtra os dados por um intervalo de datas específico, cria um gráfico interativo de linha comparando o engajamento ao longo do tempo e, finalmente, salva o gráfico como um arquivo HTML.
Ele é focado em calcular, visualizar e comparar o engajamento dos políticos Lula e Bolsonaro no Twitter ao longo de um intervalo de datas específico. O gráfico interativo de linha mostra as tendências de engajamento ao longo do tempo para cada político.

![grafico](https://user-images.githubusercontent.com/79403619/261483127-28963a34-b726-446e-9acd-5eded296af17.png)

6. **Análise de Dados (Engajamento Twitter) - GRÁFICO DE BARRAS**: Essa etapa calcula o engajamento (soma de retweets e favoritos) para os políticos Lula e Bolsonaro, cria um DataFrame consolidado para o gráfico, agrupa os dados por período e político, gera um gráfico de barras dinâmico comparando o engajamento ao longo do tempo e salva o gráfico como um arquivo HTML.
O código foca na análise comparativa do engajamento dos políticos Lula e Bolsonaro ao longo do tempo, utilizando um gráfico de barras dinâmico para visualizar as diferenças no engajamento mensal entre os políticos.

![grafico2](https://user-images.githubusercontent.com/79403619/261483149-73fd1242-ac3f-453f-95fc-dc20148c1825.png)

7. **Análise de Dados (Engajamento Twitter) - GRÁFICO DE DISPERSÃO**: Essa etapa cria um DataFrame consolidado para o gráfico de dispersão, define um intervalo de datas para filtrar os dados, gera um gráfico de dispersão que mostra a relação entre retweets e favoritos com a data e o filtro aplicados, e exibe o gráfico utilizando a função pyo.plot. O objetivo principal é visualizar a relação entre retweets e favoritos para os políticos Lula e Bolsonaro, considerando um intervalo de datas específico. O gráfico de dispersão ajuda a identificar padrões ou tendências entre as métricas de engajamento.

![grafico3](https://user-images.githubusercontent.com/79403619/261483170-f734529b-f02c-49b8-b31f-1e9bda6399fa.png)

8. **Análise de Dados (Palavras mais Faladas)**: Nessa etapa criei um DataFrame consolidado para processamento de texto a partir dos tweets de Lula e Bolsonaro. Realizando o pré-processamento do texto usando a biblioteca NLTK, incluindo a conversão para minúsculas, remoção de URLs, hashtags, pontuação e stopwords. Em seguida, calcula a frequência das palavras mais faladas para Lula e Bolsonaro, calcula o percentual dessas palavras em relação ao total de palavras, e finalmente, gera um gráfico de barras comparando o percentual das palavras mais faladas para ambos os políticos.
O objetivo é identificar as palavras mais frequentes nos tweets de Lula e Bolsonaro, permitindo uma análise superficial das principais palavras utilizadas por cada político. O gráfico de barras apresenta visualmente o percentual das palavras mais faladas para ambos.

![analise](https://user-images.githubusercontent.com/79403619/261483066-5bc04a5f-0c81-412c-baf8-0d97451327ca.png)


9. **Nuvem de Palavras** Nessa etapa estamos criando um código onde é gerado uma nuvem de palavras para os tweets dos políticos Lula e Bolsonaro. Utiliza a biblioteca WordCloud para gerar a nuvem de palavras com base nas frequências das palavras nos tweets. O gráfico resultante mostra a nuvem de palavras para os tweets dos políticos Lula e Bolsonaro.
O objetivo é visualizar de forma gráfica as palavras mais frequentes nos tweets, destacando as palavras que são mais utilizadas.

> Lula
![output_LULA](https://github.com/NayaraWakewski/Projeto-Infinity-Final-Curso/assets/79403619/960696ab-45f6-4d94-b864-8e0dbff235b6)

> Bolsonaro
![output_bolsonaro](https://github.com/NayaraWakewski/Projeto-Infinity-Final-Curso/assets/79403619/05f83dec-4ed7-4b2b-95b2-452d79a5c9e6)


10. **Análise de uma data específica (Histórica)**: Afim de acrescentarmos informações no projeto, decidi criar um código para analisar o que foi postado por ambos, em uma data específica histórica.  

**Ao seguir essas etapas, buscamos obter uma compreensão aprofundada dos dados fornecidos, lembrando que a intenção da Análise é não ter nenhum vies político.**


## 🚀 MODELO DE APRENDIZADO DE MAQUINA.

**Criando um Código de Aprendizado de Maquina**: Foi proposto um DESAFIO de criar um modelo de aprendizado de maquina, que fosse capaz de identificar se uma "fala", "texto", seria de orientação política de **ESQUERDA** ou **DIREITA**, com base nos dataframe do Presidente Lula e do Ex-Presidente Bolsonaro. 

A acurácia do modelo ficou em 94%. E após a criação do modelo foi feita uma etapa de teste, para avaliação. Conforme print abaixo:

![teste](https://user-images.githubusercontent.com/79403619/261483086-df4c660b-8ce7-4ecc-a467-2498be712eb2.jpg)

   
### 🛠️ Instalação/Ferramentas

> **Para elaboração do Projeto utilizamos as seguintes ferramentas:**

- **Visual Studio Code** - utilizado para organizar as etapas do projeto, testar as query em Sql e fazer o projeto em Python.
- **Github** - Plataforma de hospedagem de código, que utilizamos para subir o projeto.



## ⚙️ Exemplo código Python do Aprendizado de Máquina em Python:


- **Importando Bibliotecas**

```python:

#Importando Bibliotecas
import pandas as pd #Importa a biblioteca pandas com um alias 'pd', frequentemente usada para manipulação e análise de dados tabulares.
from sklearn.model_selection import train_test_split #Importa o Módulo do scikit-learn para seleção de modelos e avaliação de desempenho.
from sklearn.feature_extraction.text import CountVectorizer #Importa o Módulo para extração de características de texto para modelos de aprendizado de máquina.
from sklearn.naive_bayes import MultinomialNB #Importa o Módulo para implementação de algoritmos de classificação Naive Bayes.
from sklearn.metrics import accuracy_score #Importa o Módulo para métricas de avaliação de modelos de aprendizado de máquina, como acurácia.

#Combinando dataframes.
df = pd.concat([df_lula, df_bolsonaro], ignore_index=True)

#Definindo Classe e Rótulos
df['class'] = ['esquerda'] * len(df_lula) + ['direita'] * len(df_bolsonaro)

#Dividindo o Dataframe
X_train, X_test, y_train, y_test = train_test_split(df['full_text'], df['class'], test_size=0.2, random_state=42)

#Criando uma matriz de frequencia.
vectorizer = CountVectorizer()
X_train_vectorized = vectorizer.fit_transform(X_train)
X_test_vectorized = vectorizer.transform(X_test)

#Treinando um Modelo
model = MultinomialNB()
model.fit(X_train_vectorized, y_train)

#Previsão
predictions = model.predict(X_test_vectorized)

#Acurácia do Modelo
accuracy = accuracy_score(y_test, predictions)
print(f'Acurácia do modelo: {accuracy:.2f}')
```


## 🎁 Expressões de gratidão

* Compartilhe com outras pessoas esse projeto 📢;
* Quer saber mais sobre o projeto? Entre em contato para tomarmos um :coffee:;
* Leia a Newsletter no Linkedin Miaudados (Assinar no LinkedIn https://www.linkedin.com/build-relation/newsletter-follow?entityUrn=7084687709755043840)

---
⌨️ com ❤️ por [Nayara Vakevskii](https://github.com/NayaraWakewski) (https://www.linkedin.com/in/nayaraba/) 😊
