**Laboratório 22 - Crie um notebook usando o chat do Github Copilot e
forneça respostas com base nos dados do teste**

**INTRODUÇÃO**

Este conjunto de dados tested_worldwide.csv é originário do Kaggle. Este
conjunto de dados, que contém o número de testes realizados ao longo do
tempo, é importante para ajudar a compreender os casos relatados
diariamente e entender como a COVID-19 está realmente se espalhando em
cada país.

**INSTRUÇÕES**

1.  Abra o Visual Studio Code no menu Iniciar do Windows e abra a pasta
    navegando até C:\Labfiles\CopilotHackathon

![A screenshot of a computer Description automatically
generated](./media/image1.png)

2.  Clique no botão **Yes, I Trust the Author**.

![BrokenImage](./media/image2.png)

3.  Clique no ícone do **Copilot** no canto inferior direito e selecione
    **Github Copilot Chat.**

![BrokenImage](./media/image3.png)

4.  Digite seu prompt create a new notebook in a project. Use o comando
    /newnotebook e nomeie-o como "COVID19 Worldwide Testing Data".

![BrokenImage](./media/image4.png)

5.  Você pode ver as instruções do Copilot ajudando você com
    orientações. Siga os passos e crie o notebook.

    - Abra a paleta de comandos pressionando **Ctrl+Shift+P.**

    - Digite Jupyter: Create New Blank Notebook e pressione Enter.

![BrokenImage](./media/image5.png)

- Um novo notebook será criado. Salve-o com o nome
  COVID19WorldwideTesting Data.ipynb. Você também pode perguntar ao
  Copilot como salvar um novo notebook.

![BrokenImage](./media/image6.png)

- Vá para a pasta de destino - **excercisefiles-? dataengineer** entre
  em COVID19WorldwideTesting Data.ipynb e salve o arquivo.

![BrokenImage](./media/image7.png)

6.  Você deve ver que o arquivo foi criado na pasta **dataengineer**.

![A screenshot of a computer Description automatically
generated](./media/image8.png)

7.  Use o Copilot e o Copilot Chat para desenvolver o exercício e apoiar
    o seu aprendizado.

**EXERCÍCIO**

Nossa análise tenta fornecer uma resposta para esta pergunta: **Quais
países relataram o maior número de casos positivos em relação ao número
de testes realizados?**

**Tarefa 1: Importar as bibliotecas necessárias**

1.  Clique em Notebook kernel e digite \#Import Required Libraries.
    Incluindo Pandas e pressione Enter

![A screenshot of a computer Description automatically
generated](./media/image9.png)

2.  Pressione a tecla Tab. Isso o levará ao final da linha. Pressione
    Enter e pressione novamente a tecla Tab para adicionar todas as
    bibliotecas.

![A screenshot of a computer Description automatically
generated](./media/image10.png)

\# Import the necessary libraries, including pandas.

\# Import Required Libraries

\# Here we are importing the necessary libraries for our task

import pandas as pd \# pandas is a software library written for the
Python programming language for data manipulation and analysis.

![A screenshot of a computer Description automatically
generated](./media/image11.png)

**Tarefa 2: Carregar o conjunto de dados**

1.  Use pandas para carregar o arquivo 'tested_worldwide.csv' do nível
    raiz.

2.  Peça ajuda ao Github Copilot sobre como carregar dados. Digite: Use
    pandas to load the 'tested_worldwide.csv' file from the root level

![BrokenImage](./media/image12.png)

3.  Digite o código abaixo em um Notebook e execute-o. Ele solicitará
    que você selecione o **ambiente Python**. Selecione-o.

![BrokenImage](./media/image13.png)

4.  Selecione o ambiente recomendado. O script será executado e
    fornecerá os resultados.

![BrokenImage](./media/image14.png)

![A screenshot of a computer Description automatically
generated](./media/image15.png)

Tarefa 3 : Compreendendo os Dados

1.  Use a função head() para exibir as primeiras 5 linhas do conjunto de
    dados

2.  Peça ao Github Copilot para ajudá-lo com o código para exibir as
    primeiras 5 linhas do conjunto de dados.

![BrokenImage](./media/image16.png)

3.  Clique em **+code** para abrir um novo kernel. Digite apenas \#
    display first 5 rows of dataset. Ele irá prever automaticamente sua
    solicitação. Basta pressionar Tab e depois pressionar Enter.

![Screens screenshot of a computer screen Description automatically
generated](./media/image17.png)

4.  O **Copilot** prevê o comando que você está procurando, então
    pressione Tab para aceitar o código. Você sempre tem a opção de
    editar/escrever seu próprio código.

![BrokenImage](./media/image18.png)

5.  Pressione a tecla Tab e aceite o código. Execute o kernel.

![BrokenImage](./media/image19.png)

6.  Você deverá ver os resultados.

![A screenshot of a computer screen Description automatically
generated](./media/image20.png)

![A screenshot of a computer Description automatically
generated](./media/image21.png)

7.  Peça ajuda ao seu Copilot para exibir o número de linhas e colunas
    no dataframe. Clique em +code, insira o código e depois execute o
    kernel. Você também pode usar o código abaixo:

8.  num_rows, num_cols = data.shape

9.  print("Number of rows:", num_rows)

print("Number of columns:", num_cols)

![BrokenImage](./media/image22.png)

10. Peça ajuda ao seu Copilot para exibir os tipos de dados de cada
    coluna. Você também pode usar data.dtypes.

![A screenshot of a computer Description automatically
generated](./media/image23.png)

11. Peça ao seu GitHub Copilot para fornecer o código para exibir o
    número de valores ausentes em cada coluna.

![A screenshot of a computer Description automatically
generated](./media/image24.png)

12. Adicione um novo kernel, insira o código abaixo e execute-o. Você
    também pode usar o código sugerido pelo Copilot e verificar.

13. missing_values = df.isnull().sum()

print(missing_values)

![A screenshot of a computer program Description automatically
generated](./media/image25.png)

14. Execute o código abaixo em um novo kernel para exibir o número de
    valores únicos em cada coluna. Verifique com o seu Copilot o código
    e os resultados.

15. unique_values = df.nunique()

print(unique_values)

![A screenshot of a computer Description automatically
generated](./media/image26.png)

**Tarefa 4 : Limpeza de Dados**

1.  Execute o código abaixo para excluir as colunas que não são
    necessárias para a análise. Peça o código ao seu Copilot e verifique
    os resultados.

data = df\[\['Country_Region', 'positive', 'total_tested'\]\]

![A screenshot of a computer Description automatically
generated](./media/image27.png)

2.  Digite \#Rename the columns to make them more readable em um novo
    kernel e aceite o código.

![A screenshot of a computer Description automatically
generated](./media/image28.png)

3.  Você pode usar o código abaixo e executá-lo.

df.rename(columns={'Country_Region': 'Country', 'positive': 'Positive
Cases', 'total_tested': 'Total Tested'}, inplace=True)

![A screenshot of a computer Description automatically
generated](./media/image29.png)

4.  Peça ao seu Copilot para Drop the rows that have missing values e
    execute o código em um novo kernel ou digite \#Drop the rows that
    have missing values em um novo kernel, pressione Enter. Pressione
    Tab e aceite o código.

![A screenshot of a computer Description automatically
generated](./media/image30.png)

5.  Adicione um novo +Code kernel e digite \#Convert the data types of
    the columns to the appropriate types, pressione **Tab** para aceitar
    o código, pressione Enter novamente e depois Tab. Gere o código para
    Positive cases, Total Tested e country, e então execute-o.

![A screenshot of a computer Description automatically
generated](./media/image31.png)

6.  Adicione um novo +Code kernel e digite \#Display the number of
    missing values in each column, depois pressione Enter. Em seguida,
    pressione Tab para aceitar o código. Você também pode pedir ajuda no
    GitHub Copilot Chat.

![A screenshot of a computer program Description automatically
generated](./media/image32.png)

![A screenshot of a computer screen Description automatically
generated](./media/image33.png)

**Tarefa 5 : Extraindo os Dez Principais Países com Mais Casos de
Covid-19.**

1.  Peça ajuda ao Copilot Chat para gerar o código, Crie uma nova
    estrutura de dados que contenha o número total de casos positivos
    para cada país. Ou abra um novo +Code kernel e digite: #Create a new
    dataframe that contains the total number of positive cases for each
    country. Pressione Enter e depois Tab para aceitar o código
    sugerido.

![A screenshot of a computer Description automatically
generated](./media/image34.png)

2.  Em um novo código, insira os prompts abaixo, pressione Enter após
    cada um para aceitar o código e execute-o:

3.  \# Group the data by 'Country' and calculate the sum of 'Positive
    Cases'

4.  total_positive_cases = data.groupby('Country')\['Positive
    Cases'\].sum()

5.  \# Create a new dataframe with the total positive cases for each
    country

6.  df_total_positive_cases = pd.DataFrame({'Country':
    total_positive_cases.index, 'Total Positive Cases':
    total_positive_cases.values})

7.  \# Display the new dataframe

df_total_positive_cases

![A screenshot of a computer screen Description automatically
generated](./media/image35.png)

8.  Peça ao Copilot para ordenar o dataframe em ordem decrescente do
    número total de casos positivos Ou digite \# Sort the dataframe in
    descending order of the total number of positive cases no novo Code
    kernel, pressione Tag para aceitar o código e execute-o.

![A screenshot of a computer Description automatically
generated](./media/image36.png)

9.  Peça ao seu chat do Github Copilot para ajudá-lo a Exibir os dez
    países com mais casos positivos Ou digite \# Display the top ten
    countries with the most positive cases no new code kernel e
    execute-o. Lembre-se de que você só precisa exibir os resultados.

![A screenshot of a computer Description automatically
generated](./media/image37.png)

**Tarefa 6: Identificar o maior positivo entre os casos testados**

1.  Peça ao seu GitHub Copilot Chat para ajudá-lo com isso: Criar uma
    nova estrutura que contenha o número total de testes realizados para
    cada país ou abrir um novo Code kernel e digitar \# Create a new
    dataframe that contains the total number of tests conducted for each
    country e pressione Tab para aceitar o código. Você pode editar o
    código, se necessário, e executá-lo.

2.  \# Group the data by 'Country' and calculate the sum of 'Total
    Tested'

3.  total_tests = data.groupby('Country')\['Total Tested'\].sum()

4.  

5.  \# Create a new dataframe with the total tests conducted for each
    country

6.  df_total_tests = pd.DataFrame({'Country': total_tests.index, 'Total
    Tests': total_tests.values})

7.  \# Display the new dataframe

df_total_tests

![A screenshot of a computer Description automatically
generated](./media/image38.png)

8.  Peça ao seu Github Copilot Chat para ordenar o dataframe em ordem
    decrescente do número total de testes realizados. Ou abra um novo
    code kernel, digite \# Sort the dataframe in descending order of the
    total number of tests conducted e pressione Tab para aceitar o
    código e executá-lo.

![A screenshot of a computer program Description automatically
generated](./media/image39.png)

9.  Peça ao seu Github Copilot Chat para exibir os dez países com mais
    testes realizados ou abra um novo code kernel, digite \# Display the
    top ten countries with the most tests conducted e pressione a tecla
    Tab para aceitar o código e executá-lo.

![A screenshot of a computer program Description automatically
generated](./media/image40.png)

**Tarefa 7: Identificar os três países com o maior número de casos
positivos em relação ao número de testes realizados.**

1.  Peça ao seu Github Copilot Chat para combinar as duas estruturas de
    dados criadas nas etapas anteriores. Ou abra um novo kernel de
    código e digite \# Display the top ten countries with the most tests
    conducted e pressione a tecla Tab para aceitar o código e
    executá-lo.

![A screenshot of a computer Description automatically
generated](./media/image41.png)

2.  Peça ao seu Github Copilot Chat para criar uma nova coluna que
    contenha a proporção de casos positivos em relação ao número de
    testes realizados. Ou abra um novo code kernel e digite \# Create a
    new column that contains the ratio of positive cases to the number
    of tests conducted. Em seguida, pressione a tecla Tab para aceitar o
    código e executá-lo.

![A screenshot of a computer Description automatically
generated](./media/image42.png)

3.  Peça ao seu Github Copilot Chat para ordenar o dataframe em ordem
    decrescente da proporção de casos positivos em relação ao número de
    testes realizados. Ou abra um novo code kernel e digite \# Sort the
    dataframe in descending order of the ratio of positive cases to the
    number of tests conducted. Em seguida, pressione a tecla Tab para
    aceitar o código e executá-lo.

![A screenshot of a computer Description automatically
generated](./media/image43.png)

4.  Peça ao seu Github Copilot Chat para exibir os três países com a
    maior proporção de casos positivos em relação ao número de testes
    realizados. Ou abra um novo code kernel e digite \#Display the top
    three countries with the highest ratio of positive cases to the
    number of tests conducted. Em seguida, pressione a tecla Tab para
    aceitar o código e executá-lo.

5.  \#Display the top three countries with the highest ratio of positive
    cases to the number of tests conducted

6.  top_countries = merged_df.nlargest(3, 'Positive Test Rate')

top_countries\[\['Country', 'Positive Test Rate'\]\]

![A screenshot of a computer Description automatically
generated](./media/image44.png)

**Tarefa 8: Exibindo os resultados**

1.  Peça ao seu Github Copilot Chat para exibir os resultados em um
    gráfico que mostre os três países com a maior proporção de casos
    positivos em relação ao número Ou abra um novo code kernel e digite
    \# Display the results a chart that shows the top three countries
    with the highest ratio of positive cases to the number e pressione a
    tecla Tab para aceitar o código e executá-lo.

2.  \#Display the results a chart that shows the top three countries
    with the highest ratio of positive cases to the number

3.  import matplotlib.pyplot as plt

top_countries.plot(x='Country', y='Positive Test Rate', kind='bar')

![A screenshot of a computer program Description automatically
generated](./media/image45.png)

4.  Peça ao seu Github Copilot Chat para exibir os resultados em um
    gráfico que mostre os dez países com o maior número de casos
    positivos. Ou abra um novo code kernel e digite \# Display the
    results in a chart that shows the top ten countries with the most
    positive cases. Em seguida, pressione a tecla Tab para aceitar o
    código e executá-lo.

5.  \#Display the results in a chart that shows the top ten countries
    with the most positive cases

6.  import matplotlib.pyplot as plt

7.  df_total_positive_cases.head(10).plot(x='Country', y='Total Positive
    Cases', kind='bar')

8.  plt.xlabel('Country')

9.  plt.ylabel('Total Positive Cases')

10. plt.title('Top Ten Countries with the Most Positive Cases')

plt.show()

![A screenshot of a computer screen Description automatically
generated](./media/image46.png)

11. Peça ao seu Github Copilot Chat para exibir os resultados em um
    gráfico que mostre os dez países com o maior número de testes
    realizados. Ou abra um novo code kernel e digite \# Display the
    results in a chart that shows the top ten countries with the most
    tests conducted. Em seguida, pressione a tecla Tab para aceitar o
    código e executá-lo.

![A screenshot of a computer Description automatically
generated](./media/image47.png)

**Tarefa 9: Conclusão**

1.  Quais são suas conclusões?

2.  Quais são as limitações desta análise??

3.  Quais são os próximos passos que você tomaria para melhorar esta
    análise?
