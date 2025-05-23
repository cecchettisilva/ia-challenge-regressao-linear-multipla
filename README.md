# Desafio de Regressão Linear Múltipla

## Objetivo

O objetivo deste exercício é construir um modelo de machine learning capaz de prever o valor do aluguel de um imóvel com base em suas características. Através da análise de um dataset de imóveis, você irá:

1. **Explorar os dados:** Realizar uma análise exploratória dos dados para entender a distribuição das variáveis, identificar possíveis outliers e correlações.
2. **Preparar os dados:** Limpar os dados, tratar valores ausentes e codificar variáveis categóricas.
3. **Construir um modelo:** Utilizar um algoritmo de regressão linear para construir um modelo que relacione as características do imóvel com o valor do aluguel.
4. **Avaliar o modelo:** Avaliar a performance do modelo utilizando métricas adequadas e analisar os resíduos para verificar a qualidade das previsões.
5. **Interpretar os resultados:** Analisar os coeficientes do modelo para entender a importância de cada variável na previsão do valor do aluguel.

## Estrutura do Projeto

- **dataset_aluguel.csv**: Arquivo contendo os dados de entrada para análise.
- **desafio-regressao-linear-multipla.ipynb**: Notebook principal com o código e análises realizadas.
- **app_gradio_aluguel.ipynb**: Aplicação para executar as predições através da UI do Gradio.
- **Pipfile** e **Pipfile.lock**: Arquivos para gerenciamento de dependências do projeto.

## Instalação

1. Certifique-se de ter o Python 3.8 ou superior instalado.
2. Instale o gerenciador de pacotes `pipenv` com o comando:
   ```bash
   pip install pipenv
   ```
3. Navegue até o diretório do projeto e instale as dependências com:
   ```bash
   pipenv install <nome_da_biblioteca>
   ```
4. Ative o ambiente virtual:
   ```bash
   pipenv shell
   ```

## Execução

1. Abra o arquivo `desafio-regressao-linear-multipla.ipynb` em um ambiente compatível com Jupyter Notebook, como o VS Code ou Jupyter Lab.
2. Execute os blocos de código sequencialmente para reproduzir a análise e os resultados.

## Etapas do Projeto

### 1. Importação de Bibliotecas
- Importamos bibliotecas como `pandas`, `scikit-learn`, `seaborn` e `matplotlib` e demais para manipulação de dados, visualização e construção do modelo.

### 2. Carregamento e Visualização dos Dados
- Carregamos os dados do arquivo CSV e realizamos uma inspeção inicial para entender a estrutura e verificar a presença de valores nulos.

### 3. Análise Exploratória dos Dados (EDA)
- Calculamos estatísticas descritivas e criamos gráficos de dispersão e mapas de calor para analisar a correlação entre as variáveis.

### 4. Construção do Modelo de Regressão Linear
- Dividimos os dados em conjuntos de treino e teste.
- Treinamos um modelo de regressão linear para prever a área irrigada com base nas horas de irrigação.
- Imprimimos a equação da reta obtida pelo modelo.

### 5. Avaliação do Modelo
- Avaliamos o desempenho do modelo utilizando métricas como MSE (Erro Quadrático Médio) e MAE (Erro Absoluto Médio).
- Visualizamos os resultados reais e preditos em gráficos.

### 6. Análise de Resíduos
- Calculamos os resíduos do modelo e verificamos sua normalidade utilizando testes estatísticos e gráficos QQ-Plot.

### 7. Predições de Exemplo
- Utilizamos o modelo para prever a área irrigada para diferentes valores de aluguel.
- Também é possível executar uma aplicação UI através do Gradio, para realizar predições diversas, baseada no modelo de ML criado.

## Conclusão

Este projeto demonstrou como a regressão linear múltipla pode ser utilizada para modelar relações entre variáveis e otimizar a predição de alugueis de casas.
Para um modelo mais preciso e com uma melhor capacidade de predição, seria interessante adicionar no dataset os seguintes itens:
- número de banheiros
- área útil
- presença de algo relacionado à lazer (pscina, churrasqueira, quadra, etc)
- com mobilia ou sem
- distância até o centro
- o que há nas proximidades
- bairro (está muito amplo apenas subúrbio e periferia)
- índice de segurança da região
- duração do contrato
- tipo de garantia exigida (fiador, caução, etc)
- valor de IPTU

Estas melhorias tornariam o modelo mais robusto por:
- capturar mais dimensões que influenciam o preço
- permitir análises mais granulares
- melhorar a capacidade de generalização
- reduzir o erro de previsão
- aumentar a interpretabilidade do modelo

O dataset atual, embora funcional, deixa de capturar muitas nuances importantes do mercado imobiliário que poderiam melhorar significativamente a precisão das previsões.