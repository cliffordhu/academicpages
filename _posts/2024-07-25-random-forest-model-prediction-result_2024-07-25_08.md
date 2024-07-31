---
title: '2024-07-25 Random Forest Model Prediction Result'
date: 2024-07-25
permalink: /posts/2024/07/random-forest-model-prediction-result_2024-07-25_08/
tags:
  - rf reg result
  - rf clf result
  - updated on 2024-07-25
---
## Ticker Rank List: Uptrend to Downtrend This document presents a rank list of tickers based on their predicted trend, from uptrend to downtrend. The predictions are generated by three different models:
 CSV Result can be download [ Here ](https://cliffordhu.github.io/images/2024-07-25-random-forest-model-prediction-result_2024-07-25_08.csv) 

* **0- LSTM Model (15-Day Lookback):** This model uses Long Short-Term Memory (LSTM) networks to predict the next 15 days' price slope (K-slope). 
* **1- RF Model (15-Day Lookback):** This random forest (RF) classification model predicts whether the future 15-day price slope is positive based on 300 decision trees trained on 260 features. These features encompass: 
     * a. Price action- EMA,Passed Gain, Vol. ATR?...  
     * b. Momentum indicators  RSI, CCI,...  
     * c. Oscillation indicators  BB, MACD, KDJ... 
     * d. Macroeconomic indicators Interest Rate, VIX, Exchange Rate, gloal market, CPI? GDP? Fed decision? Employeement rate change? 
 * **2- RF Model (39-Day Lookback):** Similar to model 1, but with a 39-day lookback window for its predictions. 

 **Model Training Date:** 2024-07-25-08 
 
 **Important Considerations:** 
 
 * **Bias:** The model is biased towards long positions and may not be accurate for short positions. It's recommended for portfolio sizing, ticker screening, risk management, not for day trading.
 * **Unforeseen Events:** Avoid using the model near major events like earnings announcements, Fed decisions, etc., as it may not capture these impacts. It's best suited for stable instruments like indices and ETFs.
 * **Overfitting:** Due to the inherent overfitting problem, this model is best used as a directional guidance tool within your investment strategy. For example, consider a put-shorting scenario:
     * Select candidates only when: 
         * The classification RF model (CLF) votes indicate a high probability of a positive price move.
         * The LSTM and regression RF (REG) K-means are positive. 
         * The past 5 days' trend for all indicators is positive. 
 
 **Disclaimer:** This model is provided for informational purposes only and should not be considered financial advice. Always conduct your own research and due diligence before making investment decisions.



** Result Table **

</details>

|    | Symbol                                                  | 0 LSTM Prediction                            | 0 5-day Trend of LSTM                        | 1 Vote for Positve %   | 1 5-day Trend of Vote                        | 1 K mean predicted by reggresion             | 1 5-day Trend of K mean                      | 2 Vote for Positve %   | 2 5-day Trend of Vote                        | 2 K mean predicted by reggresion             | 2 5-day Trend of K mean                      |   3 LDA Gain Loss dB |     Total | Sector   |   Rank |   Rank Percent |
|---:|:--------------------------------------------------------|:---------------------------------------------|:---------------------------------------------|:-----------------------|:---------------------------------------------|:---------------------------------------------|:---------------------------------------------|:-----------------------|:---------------------------------------------|:---------------------------------------------|:---------------------------------------------|---------------------:|----------:|:---------|-------:|---------------:|
|  0 | [XLE](https://finance.yahoo.com/quote/XLE/financials)   | <span style="color: red;"> -0.125 </span>    | <span style="color: green;"> 0.03518 </span> | 67.0%                  | <span style="color: green;"> 0.3451 </span>  | <span style="color: green;"> 0.03032 </span> | <span style="color: green;"> 0.0186 </span>  | 65.0%                  | <span style="color: green;"> 0.3839 </span>  | <span style="color: green;"> 0.03241 </span> | <span style="color: green;"> 0.01784 </span> |          13.6934     | 16.7713   | ETF      |      1 |           0.98 |
|  1 | [XLK](https://finance.yahoo.com/quote/XLK/financials)   | <span style="color: red;"> -0.37858 </span>  | <span style="color: green;"> 0.01372 </span> | 63.0%                  | <span style="color: green;"> 0.07511 </span> | <span style="color: red;"> -0.00678 </span>  | <span style="color: red;"> -0.00062 </span>  | 66.0%                  | <span style="color: green;"> 0.08069 </span> | <span style="color: red;"> -0.03015 </span>  | <span style="color: red;"> -0.0074 </span>   |          11.7476     | 14.1946   | ETF      |      2 |           0.96 |
|  2 | [VDE](https://finance.yahoo.com/quote/VDE/financials)   | <span style="color: red;"> -0.13727 </span>  | <span style="color: green;"> 0.10547 </span> | 69.0%                  | <span style="color: green;"> 0.35926 </span> | <span style="color: green;"> 0.04677 </span> | <span style="color: green;"> 0.01889 </span> | 64.0%                  | <span style="color: green;"> 0.24282 </span> | <span style="color: green;"> 0.03838 </span> | <span style="color: green;"> 0.01216 </span> |           9.27288    | 12.4342   | ETF      |      3 |           0.94 |
|  3 | [XBI](https://finance.yahoo.com/quote/XBI/financials)   | <span style="color: green;"> 0.04624 </span> | <span style="color: green;"> 0.07287 </span> | 55.0%                  | <span style="color: green;"> 0.36747 </span> | <span style="color: red;"> -0.03494 </span>  | <span style="color: green;"> 0.01152 </span> | 55.0%                  | <span style="color: green;"> 0.34604 </span> | <span style="color: red;"> -0.01976 </span>  | <span style="color: green;"> 0.01606 </span> |          11.3906     | 12.4044   | ETF      |      4 |           0.92 |
|  4 | [IGV](https://finance.yahoo.com/quote/IGV/financials)   | <span style="color: red;"> -0.04777 </span>  | <span style="color: green;"> 0.02213 </span> | 57.0%                  | <span style="color: green;"> 0.11822 </span> | <span style="color: green;"> 0.00029 </span> | <span style="color: green;"> 0.00046 </span> | 51.0%                  | <span style="color: green;"> 0.01947 </span> | <span style="color: green;"> 0.01114 </span> | <span style="color: green;"> 0.00652 </span> |          11.2932     | 11.9838   | ETF      |      5 |           0.9  |
|  5 | [TAN](https://finance.yahoo.com/quote/TAN/financials)   | <span style="color: red;"> -0.03475 </span>  | <span style="color: green;"> 0.10275 </span> | 45.0%                  | <span style="color: green;"> 0.02062 </span> | <span style="color: red;"> -0.09559 </span>  | <span style="color: red;"> -0.0078 </span>   | 47.0%                  | <span style="color: red;"> -0.04944 </span>  | <span style="color: red;"> -0.14173 </span>  | <span style="color: red;"> -0.00753 </span>  |          12.328      | 11.5047   | ETF      |      6 |           0.88 |
|  6 | [OIH](https://finance.yahoo.com/quote/OIH/financials)   | <span style="color: red;"> -2.64199 </span>  | <span style="color: green;"> 0.07016 </span> | 48.0%                  | <span style="color: red;"> -0.03152 </span>  | <span style="color: red;"> -0.258 </span>    | <span style="color: green;"> 0.02793 </span> | 51.0%                  | <span style="color: red;"> -0.12138 </span>  | <span style="color: red;"> -0.07331 </span>  | <span style="color: green;"> 0.12261 </span> |          11.3268     |  8.59825  | ETF      |      7 |           0.86 |
|  7 | [VOO](https://finance.yahoo.com/quote/VOO/financials)   | <span style="color: red;"> -0.31146 </span>  | <span style="color: green;"> 0.18121 </span> | 59.0%                  | <span style="color: red;"> -0.10683 </span>  | <span style="color: green;"> 0.07027 </span> | <span style="color: green;"> 0.0367 </span>  | 61.0%                  | <span style="color: red;"> -0.11674 </span>  | <span style="color: green;"> 0.05046 </span> | <span style="color: green;"> 0.03402 </span> |           5.61268    |  7.2437   | ETF      |      8 |           0.84 |
|  8 | [XOP](https://finance.yahoo.com/quote/XOP/financials)   | <span style="color: red;"> -0.09376 </span>  | <span style="color: green;"> 0.12266 </span> | 50.0%                  | <span style="color: red;"> -0.00428 </span>  | <span style="color: red;"> -0.42808 </span>  | <span style="color: green;"> 0.02671 </span> | 54.0%                  | <span style="color: green;"> 0.04198 </span> | <span style="color: red;"> -0.50156 </span>  | <span style="color: green;"> 0.02623 </span> |           6.65905    |  6.95718  | ETF      |      9 |           0.82 |
|  9 | [WCLD](https://finance.yahoo.com/quote/WCLD/financials) | <span style="color: red;"> -0.00339 </span>  | <span style="color: green;"> 0.0108 </span>  | 56.0%                  | <span style="color: green;"> 0.20938 </span> | <span style="color: green;"> 0.0506 </span>  | <span style="color: green;"> 0.00239 </span> | 56.0%                  | <span style="color: green;"> 0.22984 </span> | <span style="color: green;"> 0.05886 </span> | <span style="color: green;"> 0.00933 </span> |           5.639      |  6.7893   | ETF      |     10 |           0.8  |
| 10 | [XLU](https://finance.yahoo.com/quote/XLU/financials)   | <span style="color: red;"> -0.04886 </span>  | <span style="color: red;"> -0.00725 </span>  | 58.0%                  | <span style="color: green;"> 0.03687 </span> | <span style="color: red;"> -0.08191 </span>  | <span style="color: red;"> -0.01151 </span>  | 58.0%                  | <span style="color: red;"> -0.02252 </span>  | <span style="color: red;"> -0.09497 </span>  | <span style="color: red;"> -0.01451 </span>  |           4.988      |  6.53582  | ETF      |     11 |           0.78 |
| 11 | [QQQ](https://finance.yahoo.com/quote/QQQ/financials)   | <span style="color: red;"> -0.47862 </span>  | <span style="color: green;"> 0.12861 </span> | 60.0%                  | <span style="color: red;"> -0.11959 </span>  | <span style="color: green;"> 0.03242 </span> | <span style="color: green;"> 0.01432 </span> | 58.0%                  | <span style="color: red;"> -0.0121 </span>   | <span style="color: red;"> -0.01199 </span>  | <span style="color: green;"> 0.01386 </span> |           4.64764    |  6.0093   | ETF      |     12 |           0.76 |
| 12 | [XLV](https://finance.yahoo.com/quote/XLV/financials)   | <span style="color: red;"> -0.15003 </span>  | <span style="color: green;"> 0.01744 </span> | 40.0%                  | <span style="color: red;"> -0.08408 </span>  | <span style="color: red;"> -0.03184 </span>  | <span style="color: green;"> 0.00316 </span> | 42.0%                  | <span style="color: red;"> -0.09691 </span>  | <span style="color: red;"> -0.02845 </span>  | <span style="color: green;"> 0.00434 </span> |           7.72301    |  5.81397  | ETF      |     13 |           0.73 |
| 13 | [VGT](https://finance.yahoo.com/quote/VGT/financials)   | <span style="color: red;"> -0.2849 </span>   | <span style="color: green;"> 0.14389 </span> | 54.0%                  | <span style="color: red;"> -0.05949 </span>  | <span style="color: red;"> -0.00035 </span>  | <span style="color: green;"> 0.01794 </span> | 55.0%                  | <span style="color: green;"> 0.01192 </span> | <span style="color: green;"> 0.05142 </span> | <span style="color: green;"> 0.02033 </span> |           4.86212    |  5.47077  | ETF      |     14 |           0.71 |
| 14 | [VHT](https://finance.yahoo.com/quote/VHT/financials)   | <span style="color: red;"> -0.00241 </span>  | <span style="color: green;"> 0.08782 </span> | 51.0%                  | <span style="color: green;"> 0.20375 </span> | <span style="color: red;"> -0.01881 </span>  | <span style="color: green;"> 0.01911 </span> | 53.0%                  | <span style="color: green;"> 0.20862 </span> | <span style="color: red;"> -0.01332 </span>  | <span style="color: green;"> 0.01681 </span> |           4.73826    |  5.14433  | ETF      |     15 |           0.69 |
| 15 | [VBR](https://finance.yahoo.com/quote/VBR/financials)   | <span style="color: red;"> -0.5149 </span>   | <span style="color: red;"> -0.02642 </span>  | 56.0%                  | <span style="color: red;"> -0.02684 </span>  | <span style="color: red;"> -0.04484 </span>  | <span style="color: red;"> -0.00229 </span>  | 56.0%                  | <span style="color: red;"> -0.05844 </span>  | <span style="color: red;"> -0.03246 </span>  | <span style="color: green;"> 0.00554 </span> |           4.52963    |  5.12614  | ETF      |     16 |           0.67 |
| 16 | [XLC](https://finance.yahoo.com/quote/XLC/financials)   | <span style="color: green;"> 0.07312 </span> | <span style="color: green;"> 0.00818 </span> | 76.0%                  | <span style="color: red;"> -0.07405 </span>  | <span style="color: green;"> 0.11945 </span> | <span style="color: green;"> 0.0064 </span>  | 76.0%                  | <span style="color: red;"> -0.03993 </span>  | <span style="color: green;"> 0.11903 </span> | <span style="color: green;"> 0.00256 </span> |          -0.178978   |  5.08855  | ETF      |     17 |           0.65 |
| 17 | [XPH](https://finance.yahoo.com/quote/XPH/financials)   | <span style="color: green;"> 0.00359 </span> | <span style="color: green;"> 0.02186 </span> | 39.0%                  | <span style="color: green;"> 0.06445 </span> | <span style="color: green;"> 0.01072 </span> | <span style="color: green;"> 0.01004 </span> | 41.0%                  | <span style="color: red;"> -0.01338 </span>  | <span style="color: green;"> 0.01725 </span> | <span style="color: green;"> 0.01345 </span> |           6.4883     |  4.48122  | ETF      |     18 |           0.63 |
| 18 | [IBB](https://finance.yahoo.com/quote/IBB/financials)   | <span style="color: red;"> -0.14367 </span>  | <span style="color: green;"> 0.02083 </span> | 35.0%                  | <span style="color: green;"> 0.23944 </span> | <span style="color: green;"> 0.06619 </span> | <span style="color: green;"> 0.02595 </span> | 41.0%                  | <span style="color: green;"> 0.33902 </span> | <span style="color: green;"> 0.08263 </span> | <span style="color: green;"> 0.03039 </span> |           6.90727    |  4.35541  | ETF      |     19 |           0.61 |
| 19 | [VPU](https://finance.yahoo.com/quote/VPU/financials)   | <span style="color: red;"> -0.08221 </span>  | <span style="color: green;"> 0.01061 </span> | 61.0%                  | <span style="color: red;"> -0.1217 </span>   | <span style="color: green;"> 0.07161 </span> | <span style="color: green;"> 0.01086 </span> | 61.0%                  | <span style="color: red;"> -0.00258 </span>  | <span style="color: green;"> 0.06998 </span> | <span style="color: green;"> 0.00048 </span> |           1.76065    |  3.90874  | ETF      |     20 |           0.59 |
| 20 | [XLY](https://finance.yahoo.com/quote/XLY/financials)   | <span style="color: red;"> -0.3793 </span>   | <span style="color: green;"> 0.03697 </span> | 48.0%                  | <span style="color: green;"> 0.15578 </span> | <span style="color: red;"> -0.02749 </span>  | <span style="color: green;"> 0.01429 </span> | 51.0%                  | <span style="color: green;"> 0.06602 </span> | <span style="color: red;"> -0.00035 </span>  | <span style="color: green;"> 0.0194 </span>  |           4.23109    |  3.83213  | ETF      |     21 |           0.57 |
| 21 | [DXJ](https://finance.yahoo.com/quote/DXJ/financials)   | <span style="color: red;"> -0.12609 </span>  | <span style="color: green;"> 0.01927 </span> | 60.0%                  | <span style="color: red;"> -0.06741 </span>  | <span style="color: green;"> 0.05349 </span> | <span style="color: green;"> 0.00206 </span> | 61.0%                  | <span style="color: red;"> -0.10084 </span>  | <span style="color: green;"> 0.03902 </span> | <span style="color: green;"> 0.00343 </span> |           1.76839    |  3.74516  | ETF      |     22 |           0.55 |
| 22 | [XRT](https://finance.yahoo.com/quote/XRT/financials)   | <span style="color: red;"> -0.11306 </span>  | <span style="color: green;"> 0.06278 </span> | 44.0%                  | <span style="color: green;"> 0.01072 </span> | <span style="color: red;"> -0.02794 </span>  | <span style="color: red;"> -0.00281 </span>  | 45.0%                  | <span style="color: red;"> -0.02001 </span>  | <span style="color: red;"> -0.03272 </span>  | <span style="color: green;"> 0.00062 </span> |           4.66258    |  3.43104  | ETF      |     23 |           0.53 |
| 23 | [VCR](https://finance.yahoo.com/quote/VCR/financials)   | <span style="color: red;"> -0.22579 </span>  | <span style="color: green;"> 0.14558 </span> | 59.0%                  | <span style="color: green;"> 0.00296 </span> | <span style="color: red;"> -0.05074 </span>  | <span style="color: green;"> 0.01576 </span> | 62.0%                  | <span style="color: green;"> 0.13615 </span> | <span style="color: red;"> -0.05132 </span>  | <span style="color: green;"> 0.01206 </span> |           1.19713    |  3.05028  | ETF      |     24 |           0.51 |
| 24 | [TLT](https://finance.yahoo.com/quote/TLT/financials)   | <span style="color: red;"> -0.08315 </span>  | <span style="color: red;"> -0.04301 </span>  | 42.0%                  | <span style="color: green;"> 0.27253 </span> | <span style="color: red;"> -0.02984 </span>  | <span style="color: green;"> 0.00712 </span> | 44.0%                  | <span style="color: green;"> 0.19957 </span> | <span style="color: red;"> -0.01958 </span>  | <span style="color: green;"> 0.00676 </span> |           4.02366    |  2.50703  | ETF      |     25 |           0.49 |
| 25 | [VNQ](https://finance.yahoo.com/quote/VNQ/financials)   | <span style="color: red;"> -0.04314 </span>  | <span style="color: green;"> 0.01366 </span> | 47.0%                  | <span style="color: green;"> 0.06732 </span> | <span style="color: red;"> -0.05374 </span>  | <span style="color: red;"> -0.0072 </span>   | 48.0%                  | <span style="color: green;"> 0.14148 </span> | <span style="color: red;"> -0.06534 </span>  | <span style="color: red;"> -0.01868 </span>  |           3.02551    |  2.49655  | ETF      |     26 |           0.47 |
| 26 | [VOX](https://finance.yahoo.com/quote/VOX/financials)   | <span style="color: red;"> -0.25182 </span>  | <span style="color: green;"> 0.06668 </span> | 67.0%                  | <span style="color: red;"> -0.19294 </span>  | <span style="color: green;"> 0.06055 </span> | <span style="color: red;"> -0.00564 </span>  | 71.0%                  | <span style="color: red;"> -0.172 </span>    | <span style="color: green;"> 0.02849 </span> | <span style="color: red;"> -0.00648 </span>  |          -1.10882    |  2.42257  | ETF      |     27 |           0.45 |
| 27 | [FIDU](https://finance.yahoo.com/quote/FIDU/financials) | <span style="color: green;"> 0.00567 </span> | <span style="color: green;"> 0.01361 </span> | 57.0%                  | <span style="color: red;"> -0.07591 </span>  | <span style="color: green;"> 0.02432 </span> | <span style="color: green;"> 0.00027 </span> | 54.0%                  | <span style="color: red;"> -0.04183 </span>  | <span style="color: green;"> 0.02432 </span> | <span style="color: green;"> 0.0017 </span>  |           1.08084    |  2.25036  | ETF      |     28 |           0.43 |
| 28 | [XLRE](https://finance.yahoo.com/quote/XLRE/financials) | <span style="color: red;"> -0.13589 </span>  | <span style="color: red;"> -0.00317 </span>  | 51.0%                  | <span style="color: green;"> 0.36338 </span> | <span style="color: red;"> -0.02002 </span>  | <span style="color: red;"> -0.00734 </span>  | 53.0%                  | <span style="color: green;"> 0.24599 </span> | <span style="color: red;"> -0.03394 </span>  | <span style="color: red;"> -0.01012 </span>  |           1.99637    |  2.23594  | ETF      |     29 |           0.41 |
| 29 | [SOXX](https://finance.yahoo.com/quote/SOXX/financials) | <span style="color: red;"> -0.33785 </span>  | <span style="color: green;"> 0.03673 </span> | 60.0%                  | <span style="color: red;"> -0.0603 </span>   | <span style="color: green;"> 0.04935 </span> | <span style="color: green;"> 0.00782 </span> | 66.0%                  | <span style="color: red;"> -0.04023 </span>  | <span style="color: green;"> 0.03668 </span> | <span style="color: green;"> 0.00438 </span> |          -0.356803   |  1.88716  | ETF      |     30 |           0.39 |
| 30 | [IAI](https://finance.yahoo.com/quote/IAI/financials)   | <span style="color: red;"> -0.16609 </span>  | <span style="color: green;"> 0.03863 </span> | 53.0%                  | <span style="color: green;"> 0.18106 </span> | <span style="color: red;"> -0.03764 </span>  | <span style="color: red;"> -0.0039 </span>   | 50.0%                  | <span style="color: green;"> 0.11036 </span> | <span style="color: red;"> -0.04125 </span>  | <span style="color: green;"> 0.0017 </span>  |           1.56051    |  1.74059  | ETF      |     31 |           0.37 |
| 31 | [IYM](https://finance.yahoo.com/quote/IYM/financials)   | <span style="color: red;"> -0.18918 </span>  | <span style="color: green;"> 0.0399 </span>  | 55.0%                  | <span style="color: red;"> -0.141 </span>    | <span style="color: red;"> -0.05066 </span>  | <span style="color: green;"> 0.01628 </span> | 59.0%                  | <span style="color: red;"> -0.18166 </span>  | <span style="color: red;"> -0.06621 </span>  | <span style="color: green;"> 0.01824 </span> |           0.00789521 |  1.22296  | ETF      |     32 |           0.35 |
| 32 | [IYT](https://finance.yahoo.com/quote/IYT/financials)   | <span style="color: green;"> 0.04843 </span> | <span style="color: green;"> 0.02343 </span> | 61.0%                  | <span style="color: green;"> 0.0612 </span>  | <span style="color: red;"> -0.00492 </span>  | <span style="color: red;"> -0.00113 </span>  | 63.0%                  | <span style="color: green;"> 0.03495 </span> | <span style="color: red;"> -0.00718 </span>  | <span style="color: red;"> -0.00127 </span>  |          -1.78898    |  0.685151 | ETF      |     33 |           0.33 |
| 33 | [SPY](https://finance.yahoo.com/quote/SPY/financials)   | <span style="color: red;"> -0.34869 </span>  | <span style="color: green;"> 0.14216 </span> | 56.0%                  | <span style="color: red;"> -0.16528 </span>  | <span style="color: green;"> 0.02741 </span> | <span style="color: green;"> 0.03018 </span> | 59.0%                  | <span style="color: red;"> -0.10854 </span>  | <span style="color: green;"> 0.03516 </span> | <span style="color: green;"> 0.03099 </span> |          -2.03897    | -0.887944 | ETF      |     34 |           0.31 |
| 34 | [SMH](https://finance.yahoo.com/quote/SMH/financials)   | <span style="color: red;"> -0.10529 </span>  | <span style="color: green;"> 0.0424 </span>  | 59.0%                  | <span style="color: red;"> -0.02549 </span>  | <span style="color: green;"> 0.07028 </span> | <span style="color: green;"> 0.00226 </span> | 61.0%                  | <span style="color: green;"> 0.06567 </span> | <span style="color: green;"> 0.10192 </span> | <span style="color: green;"> 0.00754 </span> |          -3.33471    | -1.4591   | ETF      |     35 |           0.29 |
| 35 | [IWM](https://finance.yahoo.com/quote/IWM/financials)   | <span style="color: red;"> -0.17301 </span>  | <span style="color: green;"> 0.07805 </span> | 46.0%                  | <span style="color: red;"> -0.00017 </span>  | <span style="color: red;"> -0.10292 </span>  | <span style="color: red;"> -0.00199 </span>  | 46.0%                  | <span style="color: green;"> 0.11037 </span> | <span style="color: red;"> -0.09729 </span>  | <span style="color: green;"> 0.01493 </span> |          -0.556705   | -1.60443  | ETF      |     36 |           0.27 |
| 36 | [IHI](https://finance.yahoo.com/quote/IHI/financials)   | <span style="color: green;"> 0.01222 </span> | <span style="color: green;"> 0.00615 </span> | 57.0%                  | <span style="color: green;"> 0.16518 </span> | <span style="color: red;"> -0.00577 </span>  | <span style="color: green;"> 0.0006 </span>  | 56.0%                  | <span style="color: green;"> 0.24336 </span> | <span style="color: red;"> -0.00477 </span>  | <span style="color: green;"> 0.0011 </span>  |          -3.29507    | -2.04219  | ETF      |     37 |           0.24 |
| 37 | [VIS](https://finance.yahoo.com/quote/VIS/financials)   | <span style="color: red;"> -0.37969 </span>  | <span style="color: red;"> -0.06005 </span>  | 55.0%                  | <span style="color: red;"> -0.08997 </span>  | <span style="color: green;"> 0.01352 </span> | <span style="color: green;"> 0.01014 </span> | 58.0%                  | <span style="color: red;"> -0.06024 </span>  | <span style="color: green;"> 0.00385 </span> | <span style="color: green;"> 0.01019 </span> |          -4.41157    | -3.53024  | ETF      |     38 |           0.22 |
| 38 | [XLB](https://finance.yahoo.com/quote/XLB/financials)   | <span style="color: red;"> -0.02403 </span>  | <span style="color: green;"> 0.03597 </span> | 50.0%                  | <span style="color: red;"> -0.12209 </span>  | <span style="color: red;"> -0.01359 </span>  | <span style="color: green;"> 0.01697 </span> | 54.0%                  | <span style="color: green;"> 0.0659 </span>  | <span style="color: red;"> -0.01962 </span>  | <span style="color: green;"> 0.01297 </span> |          -4.51473    | -4.10142  | ETF      |     39 |           0.2  |
| 39 | [VFH](https://finance.yahoo.com/quote/VFH/financials)   | <span style="color: red;"> -0.13351 </span>  | <span style="color: red;"> -0.00961 </span>  | 49.0%                  | <span style="color: red;"> -0.25622 </span>  | <span style="color: red;"> -0.04584 </span>  | <span style="color: red;"> -0.00489 </span>  | 51.0%                  | <span style="color: red;"> -0.22861 </span>  | <span style="color: red;"> -0.05074 </span>  | <span style="color: red;"> -0.00387 </span>  |          -4.19268    | -4.35991  | ETF      |     40 |           0.18 |
| 40 | [VTV](https://finance.yahoo.com/quote/VTV/financials)   | <span style="color: red;"> -0.26266 </span>  | <span style="color: green;"> 0.00976 </span> | 58.0%                  | <span style="color: red;"> -0.02078 </span>  | <span style="color: green;"> 0.00512 </span> | <span style="color: green;"> 0.01194 </span> | 56.0%                  | <span style="color: red;"> -0.02135 </span>  | <span style="color: green;"> 0.00063 </span> | <span style="color: green;"> 0.00548 </span> |          -5.84943    | -4.76087  | ETF      |     41 |           0.16 |
| 41 | [VDC](https://finance.yahoo.com/quote/VDC/financials)   | <span style="color: red;"> -0.01434 </span>  | <span style="color: green;"> 0.0556 </span>  | 51.0%                  | <span style="color: red;"> -0.27602 </span>  | <span style="color: red;"> -0.01312 </span>  | <span style="color: red;"> -0.00256 </span>  | 53.0%                  | <span style="color: red;"> -0.20941 </span>  | <span style="color: green;"> 0.00459 </span> | <span style="color: green;"> 0.00112 </span> |          -5.29651    | -4.90068  | ETF      |     42 |           0.14 |
| 42 | [KIE](https://finance.yahoo.com/quote/KIE/financials)   | <span style="color: red;"> -0.07643 </span>  | <span style="color: green;"> 0.01324 </span> | 50.0%                  | <span style="color: red;"> -0.18959 </span>  | <span style="color: red;"> -0.00867 </span>  | <span style="color: red;"> -0.0007 </span>   | 51.0%                  | <span style="color: red;"> -0.15872 </span>  | <span style="color: red;"> -0.009 </span>    | <span style="color: red;"> -0.00072 </span>  |          -5.44452    | -5.36466  | ETF      |     43 |           0.12 |
| 43 | [XLF](https://finance.yahoo.com/quote/XLF/financials)   | <span style="color: red;"> -0.09749 </span>  | <span style="color: red;"> -0.01693 </span>  | 52.0%                  | <span style="color: red;"> -0.41119 </span>  | <span style="color: red;"> -0.01641 </span>  | <span style="color: green;"> 0.00079 </span> | 58.0%                  | <span style="color: red;"> -0.30694 </span>  | <span style="color: red;"> -0.01935 </span>  | <span style="color: red;"> -0.00056 </span>  |          -7.54489    | -6.60822  | ETF      |     44 |           0.1  |
| 44 | [IYK](https://finance.yahoo.com/quote/IYK/financials)   | <span style="color: red;"> -0.03557 </span>  | <span style="color: green;"> 0.0023 </span>  | 58.0%                  | <span style="color: green;"> 0.03118 </span> | <span style="color: green;"> 0.00724 </span> | <span style="color: red;"> -0.00118 </span>  | 55.0%                  | <span style="color: red;"> -0.05339 </span>  | <span style="color: green;"> 0.00066 </span> | <span style="color: red;"> -0.00205 </span>  |          -7.88668    | -6.63402  | ETF      |     45 |           0.08 |
| 45 | [IYJ](https://finance.yahoo.com/quote/IYJ/financials)   | <span style="color: red;"> -0.16922 </span>  | <span style="color: green;"> 0.003 </span>   | 53.0%                  | <span style="color: green;"> 0.26618 </span> | <span style="color: red;"> -0.02675 </span>  | <span style="color: green;"> 0.00667 </span> | 56.0%                  | <span style="color: green;"> 0.22481 </span> | <span style="color: green;"> 0.00118 </span> | <span style="color: green;"> 0.00655 </span> |          -7.66486    | -6.95433  | ETF      |     46 |           0.06 |
| 46 | [ITA](https://finance.yahoo.com/quote/ITA/financials)   | <span style="color: red;"> -0.08371 </span>  | <span style="color: green;"> 0.03625 </span> | 54.0%                  | <span style="color: green;"> 0.05421 </span> | <span style="color: red;"> -0.04234 </span>  | <span style="color: red;"> -0.00431 </span>  | 53.0%                  | <span style="color: red;"> -0.00608 </span>  | <span style="color: red;"> -0.02037 </span>  | <span style="color: green;"> 0.00293 </span> |          -7.66924    | -7.03543  | ETF      |     47 |           0.04 |
| 47 | [VYM](https://finance.yahoo.com/quote/VYM/financials)   | <span style="color: red;"> -0.19291 </span>  | <span style="color: green;"> 0.04085 </span> | 49.0%                  | <span style="color: red;"> -0.27523 </span>  | <span style="color: red;"> -0.0072 </span>   | <span style="color: green;"> 0.00263 </span> | 50.0%                  | <span style="color: red;"> -0.21771 </span>  | <span style="color: red;"> -0.00243 </span>  | <span style="color: green;"> 0.0042 </span>  |          -7.51242    | -7.80043  | ETF      |     48 |           0.02 |
| 48 | [XLI](https://finance.yahoo.com/quote/XLI/financials)   | <span style="color: red;"> -0.08148 </span>  | <span style="color: green;"> 0.0212 </span>  | 55.0%                  | <span style="color: red;"> -0.06948 </span>  | <span style="color: green;"> 0.00309 </span> | <span style="color: green;"> 0.00489 </span> | 58.0%                  | <span style="color: green;"> 0.08333 </span> | <span style="color: green;"> 0.01203 </span> | <span style="color: green;"> 0.00784 </span> |         -11.0592     | -9.87552  | ETF      |     49 |           0    |
 </details>
