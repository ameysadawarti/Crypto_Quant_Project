# Crypto_Quant_Project

## Description

This project aims to provide insights into the cryptocurrency market by analyzing market data and developing a trading strategy based on high momentum. We analyse the behaviour of high momentum on large coins based on market capitalization, approximately >$70m, by creating a predictor, measured as the distance of previous week closing price from 4-week high.


## Steps

- 1. Extract a list of top 300 cryptocurrency coins based on market capitalization (mkt cap approx > $70 million) using coinmarketcap API.
- 2. Get weekly price data for these 300 coins.
- 3. Generate the High momentum predictor h𝑚𝑜𝑚𝑡,h at the end of week 𝑡 computed over previous 4 weeks defined as:

		    h𝑚𝑜𝑚𝑡,h = ln(𝐶𝑡) − ln(𝐻𝑡,4)
	
  Where,              
      𝐶𝑡   	= 	market close price of week 𝑡                
      𝐻𝑡,4 	= 	highest intraday price attained over the past 4 weeks

- 4. Sort the coins based on computed high momentum predictor values, then divide into 5 equal quintiles portfolios for every week
- 5. Generate equal weights for each quintile portfolios
- 6. Compute the following week return of these portfolios
- 7. Calculate stats for each portfolio


## Performance Stats

### Return Statistics:

|             | Quintile 1  | Quintile 2  | Quintile 3  | Quintile 4  | Quintile 5  |
| :---        |    :----:   |    :----:   |    :----:   |    :----:   |    :----:   |
| SR          | 1.555097    | 2.158741    |  1.614615   | 1.674715    | *2.632260*    |
| Return      | 2.788966    | 4.94431     |  3.545087   | 3.719108    | *7.355663*    |
| Volatility  | 1.793435    | 2.290368    |  2.195623   | 2.220741    | *2.79442*     |

### Cummulative Returns:

![image](https://github.com/ameysadawarti/Crypto_Quant_Project/assets/47478596/f161bbb0-9561-4915-8b8a-db2a68e906d8)

### Turnover for Quintile 5:

![image](https://github.com/ameysadawarti/Crypto_Quant_Project/assets/47478596/e15ad04e-43c0-4bf3-906d-cf9ea830e3b4)


## Conclusion/Result Analysis

Upon reviewing the obtained results, it is evident that the quintile 5 portfolio exhibits the most favorable Sharpe Ratio, signifying a superior risk-adjusted return compared to other quintiles. Therefore, we can employ the high momentum predictor to capitalize on the trading potential of quintile 5 portfolio. Moreover, the average turnover for quintile 5 is low = 0.08, translating to minimized transaction costs.








