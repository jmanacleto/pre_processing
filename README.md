Aqui está uma descrição que você pode usar no README do seu GitHub para descrever o projeto de clusterização de textos que você desenvolveu:

---

# Projeto de Clusterização de Textos

Este projeto tem como objetivo realizar a **clusterização de textos** para agrupar documentos semelhantes em diferentes categorias. Utilizando técnicas de **Processamento de Linguagem Natural (NLP)** e o algoritmo de **K-means**, foram processados dados textuais e organizados em grupos, facilitando a análise e interpretação dos conteúdos.

## Etapas do Projeto

### 1. Carregamento e Pré-processamento dos Dados
Os dados foram carregados a partir de um **dataframe** contendo as colunas `Título_Público` e `Descricao_pública`. O principal foco foi trabalhar com a descrição dos textos. O pré-processamento incluiu:

- **Remoção de stopwords**: Palavras comuns que não carregam muito significado foram removidas para focar nas palavras mais importantes.
- **Tokenização**: Os textos foram divididos em tokens (palavras) para processamento posterior.
- **Lematização/Stemming**: Palavras foram reduzidas às suas raízes para uniformizar o conteúdo.

### 2. Vetorização com TF-IDF
Para converter os textos em um formato numérico utilizável pelo algoritmo de clusterização, foi aplicada a técnica de **TF-IDF (Term Frequency-Inverse Document Frequency)**, que transforma os textos em vetores de características com base na importância de cada termo no corpus.

### 3. Clusterização com K-means
Com os textos vetorizados, o algoritmo de **K-means** foi aplicado para agrupar os textos em clusters. A escolha do número de clusters foi feita de maneira exploratória, e o resultado final foi a criação de grupos de textos semelhantes, atribuídos a diferentes categorias numéricas.

### 4. Visualização dos Resultados
Os textos foram organizados em um novo dataframe, incluindo uma coluna de clusters, para facilitar a visualização. O próximo passo foi gerar uma visualização gráfica dos clusters com a ajuda de técnicas de redução de dimensionalidade, como **PCA** (Análise de Componentes Principais).

### 5. Interpretação e Análise
Cada cluster criado foi analisado para entender quais características comuns os textos de cada grupo compartilham. Isso possibilita uma visão mais clara sobre as similaridades entre os documentos, oferecendo insights valiosos.

## Tecnologias Utilizadas

- **Python**
  - Pandas
  - Scikit-learn
  - NLTK
  - Matplotlib
- **Processamento de Linguagem Natural**
  - Tokenização
  - Stopwords
  - TF-IDF
- **Algoritmo de Clusterização**
  - K-means
- **Visualização de Dados**
  - PCA

## Como Executar o Projeto

1. Clone este repositório:
   ```bash
   git clone https://github.com/jmanacleto/pre_processing
   ```
2. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```
3. Execute o script de clusterização:
   ```bash
   python clusterizacao_textos.py
   ```

## Próximos Passos

- Implementar técnicas mais avançadas de NLP, como **Word2Vec**.
- Testar outros algoritmos de clusterização, como **DBSCAN** ou **Hierarchical Clustering**.
- Melhorar a visualização dos clusters utilizando t-SNE ou outras abordagens de redução de dimensionalidade.
