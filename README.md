
📊 **Portfolio Backtesting and Dollar Cost Averaging (DCA) Simulation**

🌟 **Project Overview**

This repository contains the Python scripts used to perform a quantitative **backtesting** analysis of a personal investment portfolio. The primary goal is to demonstrate the statistical effectiveness of the **Dollar Cost Averaging (DCA)** strategy against a single **Lump Sum** investment over a volatile period (2020–2025).

As an **Economist and Data Scientist**, the methodology prioritizes **evidence-based decision-making** and risk management over market timing. This simulation is the foundation of my strategy as a Popular Investor on eToro.

🚀 **Key Results Highlight**

| Scenario | Total Invested | Final Portfolio Value | Return (%) |
| :--- | :--- | :--- | :--- |
| A (Lump Sum) | $5,000 | $13,652 | 173.0% |
| B (DCA Monthly) | $15,000 | **$29,003** | 93.4% |

**Key Finding:** Although the Lump Sum had a higher percentage return (due to timing the 2020 market bottom), the **DCA strategy yielded 112% more absolute capital** ($29,003 vs. $13,652), proving its superiority for the average investor with a stable monthly income.

-----------------
💻 **Technical Stack**

**Primary Language:** Python 3.x

**Data Acquisition:** yfinance (for historical stock data)

**Data Manipulation:** pandas, numpy

**Visualization:** matplotlib.pyplot (with professional styling)

------------------

📈 **Portfolio Composition Under Analysis**

The backtesting was conducted on a high-conviction, growth-oriented portfolio, balanced by defensive assets for long-term resilience.


|Ticker|Asset Description|Weight|
| :--- | :--- | :--- | 
SPYG|S&P 500 Growth ETF|35%
BRK.B|Berkshire Hathaway (Value/Quality)|25%
SMH|VanEck Semiconductor ETF|16%
VTI|Vanguard Total Stock Market ETF|14%
IEMG|iShares Core Emerging Markets ETF|10%
Total||100%

-------------------------------

📊 **Simulation Methodology**

**1. Data Preparation**

- Historical Adjusted Close prices were downloaded from Yahoo Finance for the period **January 1, 2020, to November 26, 2025.**

- The **portfolio's daily return** was calculated using the weighted average of the individual asset returns.

**2. Scenario Definitions**

|Scenario|Initial Investment|Monthly Contribution|Total Timeframe|
| :--- | :--- | :--- | :--- |
|Objective A| (Lump Sum)$5,000 (Jan 1, 2020) |$0|5 Years - Benchmark for single-point entry.|
|Objective B| (DCA)$1,000 (Jan 1, 2020) and |**$200** |5 Years - Simulates the typical eToro copier behavior.|

**3. Key Calculation (DCA Logic)**

The core script iteratively calculates the portfolio value by:
1. Applying the daily portfolio return to the existing capital.
2. Adding the monthly contribution ($200) on the first trading day of each subsequent month.
3. Tracking the total capital contributed versus the final market value to visualize the profit gap.

-----------------------

🚀 **Getting Started**

To replicate this analysis, follow these steps:

**Prerequisites**

You need Python installed, along with the required libraries.

Bashpip install yfinance pandas numpy matplotlib

**Execution**
1. Clone this repository:
   Bash
   git clone [(https://github.com/Andalejo1109/Portfolio-management-and-optimization/)]
   
   cd [Portfolio-management-and-optimization]

3. Run the Python script:
   Bash
   python Simulacion_dca.py
   
The script will print the final metrics table and display the comparative line chart.

----------------------
🎓 ***About the Author**
[Andres Alejandro Rodriguez Lozano]

I am an **Economist, Data Scientist (MSc)**, and University Professor specializing in quantitative analysis and data-driven risk management. I believe that sound investment decisions are based on statistical probability, not market noise.

eToro Profile: Copy my strategy directly on eToro: [(https://etoro.tw/4lkmjxn)]

LinkedIn: [(https://www.linkedin.com/in/andalejo/)]

📝 **License**

This project is open-source and available under the MIT License.


