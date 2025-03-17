# Cryptocurrency Price Prediction Using FFT and Machine Learning

## 📌 Project Overview
This project explores the effectiveness of **Fast Fourier Transform (FFT)** for cryptocurrency price prediction and its comparison with **traditional regression models**. Additionally, **Granger Causality** is used to determine if AAVE price movements can predict Bitcoin price fluctuations.

## 📊 Methods & Approach
1. **Data Preprocessing**  
   - Collected **AAVE/USDT** and **BTC/USDT** price data.  
   - Applied **differentiation** and **Gaussian filtering** to remove non-stationary trends.

2. **Feature Engineering**  
   - Extracted **top 5 dominant frequencies** using **FFT**.  
   - Used log-returns and Fourier features as inputs for predictive models.

3. **Predictive Models**  
   - **Baseline Ridge Regression** (Market Cap & Volume as predictors).  
   - **FFT-based LSTM** (Time-series model incorporating spectral features).  

4. **Granger Causality Analysis**  
   - Tested if AAVE Fourier features **Granger-cause** BTC price movements.

##  Results
| Model                | RMSE  |
|----------------------|------|
| **Ridge Regression** | 0.024 |
| **FFT-Based LSTM**   | 0.04507 |

- **Regression performed better** in direct price estimation.
- **FFT-based LSTM captured periodic patterns** but had higher RMSE.
- **Granger Causality confirmed that AAVE signals influence BTC prices** (p = 0.0034).



## 🚀 Future Work
- Optimize **hyperparameters** for the FFT-LSTM model.
- Develop a **hybrid model** combining **regression and FFT-based predictors**.
- Extend analysis to **other cryptocurrencies** to validate cross-market dependencies.

## 📂 Repository Structure

## 🛠 Setup & Usage
```bash
# Clone the repository
git clone https://github.com/yourusername/cryptocurrency-forecasting.git
cd cryptocurrency-forecasting

# Install dependencies
pip install -r requirements.txt

# Run the main script
python main.py
```
For queries, reach out to Shivam Singh(shs046@ucsd.edu) and Albert Zhong(azhong@ucsd.edu)
