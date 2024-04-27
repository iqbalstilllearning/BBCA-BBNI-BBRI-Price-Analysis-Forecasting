![Slide1](https://github.com/iqbalstilllearning/BBCA-BBNI-BBRI-Price-Analysis-Forecasting/assets/105572256/8d4e6735-2546-40cf-b7a3-c802320fb4e5)
# **Problem Statement**

The stock trading of Bank Central Asia (BBCA), Bank Negara Indonesia (BBNI), and Bank Rakyat Indonesia (BBRI) exhibits significant price fluctuations during specific time periods. The objective of this project is to conduct a comprehensive analysis of stock prices, identify significant trends, and develop forecasting models to assist investors in making more informed investment decisions. Unpredictable stock price fluctuations pose a significant challenge for investors. By understanding trends and having reliable predictive models, investors can mitigate risks and make more informed investment decisions. The project will focus on the analysis and prediction of stock prices for BBCA, BBNI, and BBRI over a specific period (1 jan 2019- 10 jan 2024). The data used will include daily closing prices, trading volumes, and other technical indicators. The developed predictive model will be evaluated based on its performance in forecasting future stock prices.

- The dataset utilized originates from Kaggle Account ([Here](https://www.kaggle.com/caesarmario/datasets)).
- The source code for this project is available on my GitHub ([Here](https://github.com/iqbalstilllearning/BBCA-BBNI-BBRI-Price-Analysis-Forecasting))
- Notebook: [Link](https://github.com/iqbalstilllearning/BBCA-BBNI-BBRI-Price-Analysis-Forecasting/blob/main/BBCA%2C%20BBNI%2C%20BBRI%20Price%20Analysis%20%26%20Forecasting.ipynb)

# **Research Questions**
1. What was the extent of the change in closing prices and trading volumes of shares over time? What is comparative analysis of stocks in each banks?
2. What was the percentage growth in stock prices for each bank?
3. What was the daily stock returns for each bank?
4. How can one conduct technical analysis of stocks using candlestick charts?
5. How effective are LSTM models in forecasting stock prices? and what are the results of forecasting for the next 30 days?

# 1. What was the extent of the change in closing prices and trading volumes of shares over time? What is comparative analysis of stocks in each banks?

**CLOSING PRICE**
![output1](https://github.com/iqbalstilllearning/BBCA-BBNI-BBRI-Price-Analysis-Forecasting/assets/105572256/fb5bd53d-e0ea-463b-a133-8220631c93d5)
![output2](https://github.com/iqbalstilllearning/BBCA-BBNI-BBRI-Price-Analysis-Forecasting/assets/105572256/271553a6-1085-4c23-a978-4a4f887aa1a1)
BBCA:

- Highest closing price: 9,625.00 IDR
- Lowest closing price: 4,084.94 IDR
- Average closing price: 6,790.35 IDR
- Range (Highest - Lowest): 5,540.06 IDR

BBNI:

- Highest closing price: 5,650.00 IDR
- Lowest closing price: 1,375.54 IDR
- Average closing price : 3,351.50 IDR
- Range (Highest - Lowest): 4,274.46 IDR

BBRI:

- Highest closing price: 5,750.00 IDR
- Lowest closing price: 1,893.82 IDR
- Average closing price: 3,876.18 IDR
- Range (Highest - Lowest): 3,856.18 IDR

Key findings:

- All three banks experienced significant fluctuations in their closing prices over the given period, with an overall increasing trend, particularly notable around 2020. Additionally, all three banks showed an upward trend overall, but with varying degrees of volatility.
- BBCA had the highest range of change, followed by BBNI and then BBRI.
- BBCA had the highest overall growth, reaching a closing price of around 9,625 IDR, compared to BNI's 5,650 IDR and BRI's 5,750 IDR.
- BBCA outperformed BNI and BRI in terms of overall price appreciation.
- BNI and BRI had similar growth patterns, with BNI experiencing slightly higher peaks but also deeper dips compared to BRI.
- BNI appeared to be the most volatile, with the largest swings in both directions.
- BBCA and BRI exhibited somewhat less volatility, but still had periods of significant price movements.

TRADING VOLUMES
![output3](https://github.com/iqbalstilllearning/BBCA-BBNI-BBRI-Price-Analysis-Forecasting/assets/105572256/97539c6a-46e5-4e9e-adae-e4f0463bb9ba)

BBCA:

- Trading volume seems to have increased steadily from 2019 to 2021, with occasional peaks and dips.
- A significant surge in volume is visible around late 2020 and early 2021, followed by a period of relative stability.
- There appears to be a slight downward trend in volume from late 2021 to 2023.

BNI:

- BNI's trading volume exhibits a more volatile pattern compared to BBCA.
- Several sharp peaks and troughs are noticeable throughout the period, with no clear upward or downward trend.
- The highest volume spike seems to occur around mid-2020, followed by a significant drop and then another smaller peak in late 2021.

BRI:

- BRI's trading volume also shows considerable fluctuations, with several notable peaks and valleys.
- Similar to BNI, there's no consistent upward or downward trend over the period.
- The most prominent volume surges appear to be in late 2019 and early 2020, followed by a period of lower volume and then another peak in late 2021.

Comparative Analysis:

- BBCA generally had the highest and most consistent trading volume compared to BNI and BRI.
- BNI and BRI experienced more extreme fluctuations in volume, with higher peaks and deeper troughs compared to BBCA.
- It's important to note that without specific values on the y-axis, it's difficult to directly compare the magnitudes of volume changes between - the banks.

# 2. What was the percentage growth in stock prices for each bank?
GROWTH OF STOCK
![output4](https://github.com/iqbalstilllearning/BBCA-BBNI-BBRI-Price-Analysis-Forecasting/assets/105572256/59b110d6-ebdd-47af-b751-29df32e29215)
- BBCA has the highest share growth percentage from 2019 to present (Jan 2024) followed by BBRI, and then BBNI.

# 3. What was the daily stock returns for each bank?
DAILY RETURN
![output5](https://github.com/iqbalstilllearning/BBCA-BBNI-BBRI-Price-Analysis-Forecasting/assets/105572256/02bc9a95-95b9-40ea-950e-22e92d29bf9d)
![output6](https://github.com/iqbalstilllearning/BBCA-BBNI-BBRI-Price-Analysis-Forecasting/assets/105572256/841988c4-97d9-43ed-8d41-c885667da1e1)
![output7](https://github.com/iqbalstilllearning/BBCA-BBNI-BBRI-Price-Analysis-Forecasting/assets/105572256/f78f0989-3cd8-4914-92f2-7b20871b791b)

Overall Volatility:

- Maximum daily return for BCA was 13.65%, which occurred on March 26, 2020. The minimum daily return was -7.91%, and it occurred on March 17, 2020.
-  Maximum daily return for BNI was 17.33%, which occurred on June 8, 2020. The minimum daily return was -11.72%, and it occurred on March 9, 2020.
- Maximum daily return for BRI was 20,49%, which occurred on March 26, 2020. The minimum daily return was -9.09%, and it occurred on August 25, 2020.

Distribution of Returns:

- BCA: The distribution appears slightly skewed towards negative returns, suggesting a slightly higher frequency of losses than gains.
- BNI: The distribution is roughly symmetrical, indicating a balance between positive and negative returns.
- BRI: Similar to BCA, the distribution appears slightly skewed towards negative returns.

Range of Daily Returns:

- The majority of daily returns for all three banks fall within a relatively narrow range of -5% to +5%. This suggests that while these stocks can experience significant daily fluctuations, most changes are modest in percentage terms.

# 4. How can one conduct technical analysis of stocks using candlestick charts?
- Notebook: [Link](https://github.com/iqbalstilllearning/BBCA-BBNI-BBRI-Price-Analysis-Forecasting/blob/main/BBCA%2C%20BBNI%2C%20BBRI%20Price%20Analysis%20%26%20Forecasting.ipynb)

# 5. How effective are LSTM models in forecasting stock prices? and what are the results of forecasting for the next 30 days?
![output8](https://github.com/iqbalstilllearning/BBCA-BBNI-BBRI-Price-Analysis-Forecasting/assets/105572256/940eca31-331a-413c-8109-0911ae80ab33)
![output9](https://github.com/iqbalstilllearning/BBCA-BBNI-BBRI-Price-Analysis-Forecasting/assets/105572256/a903be54-9261-4977-8656-9b7597e45efe)
![output10](https://github.com/iqbalstilllearning/BBCA-BBNI-BBRI-Price-Analysis-Forecasting/assets/105572256/775f1e8f-c9ca-4ae4-8227-3e84988650f6)
Key findings:
- The LSTM model appears to be effective in capturing patterns in the data, as reflected by the low MAPE values.
- The slightly better performance on the validation set compared to the testing set raises concerns about potential overfitting, and further steps should be taken to address this.

The evaluation metrics for the forecast of BCA using LSTM models provide valuable insights into the model's performance. Based on RMSE and MAE results, the model performed slightly better on the validation dataset, suggesting it may have overfitted the training data to some extent. It's essential to assess whether the model can generalize well to unseen data. The MAPE scores indicate relatively good accuracy, especially since they fall below the 5% threshold. However, caution is warranted due to market volatility, and the model should be considered as part of a broader analysis.

Based on forecasting results using the LSTM model for the next 30 days, it can be seen that only BBCA shares are expected to increase, while BBNI and BBRI shares are predicted to experience a decline. 
But besides that, it's important to note that stock price forecasting is inherently challenging due to the dynamic nature of financial markets, and no model can guarantee accurate predictions.

![close](https://github.com/iqbalstilllearning/BBCA-BBNI-BBRI-Price-Analysis-Forecasting/assets/105572256/829f623f-2b7f-4c19-8623-7c1975b691cc)
**Links: [[Linkedin](https://www.linkedin.com/in/muhammadiqbal-/)] [[Github](https://github.com/iqbalstilllearning/)] [[Gmail](muhammadiqbal4edu@gmail.com)]**
