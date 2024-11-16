# Heart Failure Prediction with LSTM  

Este repositório apresenta um modelo de previsão de falha cardíaca utilizando redes neurais Long Short-Term Memory (LSTM). A ideia original foi baseada no trabalho de [Karnika Kapoor](https://www.kaggle.com/code/karnikakapoor/heart-failure-prediction-ann/notebook), que implementou um modelo com redes neurais artificiais (ANN) para o mesmo dataset. Aqui, adaptamos a abordagem para explorar o uso de LSTMs, que são especialmente eficazes para dados sequenciais.  

## Dataset  
O dataset utilizado é o **Heart Failure Clinical Records Dataset**, disponível no Kaggle, e contém informações clínicas de pacientes com insuficiência cardíaca. Este dataset pode ser encontrado em:  
[Heart Failure Clinical Records Dataset](https://www.kaggle.com/datasets/andrewmvd/heart-failure-clinical-data)  

### Estrutura do Dataset:  
- **Características:** Incluem variáveis como idade, nível de creatinina, fração de ejeção e outros marcadores clínicos.  
- **Alvo:** `DEATH_EVENT` (1 para morte, 0 para sobrevivência).  

## Alterações Feitas  
- **Modelo Original:** Redes neurais artificiais (ANN) foram utilizadas no notebook original.  
- **Abordagem Modificada:**  
  - Implementamos um modelo baseado em LSTMs, transformando os dados em sequências para aproveitar a capacidade dessas redes em lidar com dependências temporais.  
  - Criamos janelas deslizantes para simular dados sequenciais, já que o dataset não possui uma estrutura temporal explícita.  

## Principais Etapas  
1. **Pré-processamento dos dados:**  
   - Normalizamos as variáveis contínuas utilizando *StandardScaler*.  
   - Criamos sequências de entrada utilizando uma abordagem de janelas deslizantes.  

2. **Construção do modelo LSTM:**  
   - Implementamos uma arquitetura com duas camadas LSTM e camadas de *Dropout* para regularização.  
   - A saída é uma unidade sigmoidal para prever a probabilidade de falha cardíaca.  

3. **Treinamento e Validação:**  
   - Dividimos o dataset em conjuntos de treinamento e teste.  
   - Utilizamos *EarlyStopping* para evitar overfitting.  

4. **Avaliação:**  
   - Analisamos a performance do modelo com métricas como acurácia, matriz de confusão e relatório de classificação.  

## Resultados  
- O modelo LSTM foi treinado com uma divisão de 75% para treino e 25% para teste.  
- Métricas de avaliação como precisão, recall e F1-Score são apresentadas no notebook.  

## Visualizações  
- Gráficos de evolução de *loss* e acurácia durante o treinamento.  
- Matriz de confusão e relatório de classificação para o conjunto de teste.  

## Como Utilizar  
1. Clone este repositório:  
   ```bash
   git clone https://github.com/seuusuario/heart-failure-prediction-lstm.git
   cd heart-failure-prediction-lstm
   ```  
2. Certifique-se de instalar as dependências listadas no arquivo `requirements.txt`.  
3. Execute o notebook ou script Python para treinar o modelo.  

## Referências  
- Kaggle Notebook Original: [Heart Failure Prediction: ANN](https://www.kaggle.com/code/karnikakapoor/heart-failure-prediction-ann/notebook)  
- Kaggle Dataset: [Heart Failure Clinical Records Dataset](https://www.kaggle.com/datasets/andrewmvd/heart-failure-clinical-data)  

## Licença  
Este projeto está licenciado sob a licença MIT. Sinta-se à vontade para contribuir ou utilizar o código como referência para seus projetos!  
