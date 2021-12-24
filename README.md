## StockPrediction_Project using GAN

### 1. Dataset
* Using dataset since 2000 in FAANG (FACEBOOK, Amazon, Apple, Netflix, Google) dataset 
* I think it shows the stock data of IT companies growing in the stock market well.
* https://www.kaggle.com/aayushmishra1512/faang-complete-stock-data?select=Apple.csv

### 2. Project goals 
* (1) Soving follw up problem(right shift) with LSTM model in stock prediction. This problem is relevent to information vanishing with LSTM
* (2) Making model that predict whether tomorrow stock' price will be increased or decreased
* Therefore, Create a predictive model for Adj Close using stock data from 2000 to 2020 of FAANG companies 

### 3. Analyzing previous approaches
* Bidirectional LSTM is consisted of 20 LSTM cell in hiddem layer and 1 output in linear layer.
* Bidirectional LSTM uses RMSE in objective and Adam in optimizer.
* reference paper : ‘양방향 LSTM 순환신경망 기반 주가 예측 모델’ 
* paper link : https://scienceon.kisti.re.kr/srch/selectPORSrchArticle.do?cn=JAKO201819355173173&dbt=NART

### 4. Time Series GAN
* reference paper: Stock Market Prediction on High-Frequency Data Using Generative Adversarial Nets
* link :  https://www.hindawi.com/journals/mpe/2018/4907423/
* LSTM in the generator predicts the data of the next time point like the basic LSTM model. 
* In Discriminator, the existing stock price data from time 1 to time T and the generated prediction value were received as input to distinguish the authenticity of the data. 1d convolution layer was used in discriminator
![image](https://user-images.githubusercontent.com/59464208/147327583-b68bc243-b84b-4ac6-a58d-cb8eb680c338.png)
