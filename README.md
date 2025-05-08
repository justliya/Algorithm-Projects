# TSLA Stock Threshold Detector (Binary Search Project)

This project uses **binary search** to detect the **first time Tesla's stock (TSLA) crossed a critical price threshold**, using real historical market data. It then visualizes the result alongside key political and economic events that resulted in TSLA stock market crash between **December 2024 and March 2025**.

---

##  Key Features

-  **Binary Search** to efficiently detect the first occurrence of a threshold breach in stock prices
- 📈 Visualization of TSLA stock data with:
  - 🟢 First threshold-cross point
  - 🟥 Inauguration (Jan 20, 2025)
  - 📈 All-Time High (Dec 17, 2024)
- 📊 Monthly and daily view options
- 💾 Real historical data 

---

## 💡 Binary Search Use Case

Given a sorted list of timestamps and high prices:
- The algorithm finds the **earliest date** when `TSLA high ≥ target threshold` (e.g., $275)
- Much faster and cleaner than a linear scan using O(Log n) time analysis.

### Pseudocode:

while low <= high:
mid = (low + high) // 2
if price[mid] ≥ threshold:
result = mid
high = mid - 1
else:
low = mid + 1

---

## Technologies Used

- `Python` 
- `pandas'
- `matplotlib` 
- `datetime` 
- `wget`
- Google Colab 

---

## Dataset

- Sources: [NASDAQ Historical TSLA Data](https://www.nasdaq.com/market-activity/stocks/tsla/historical) and [Alpha Vantage Historical TSLA Data Api] (https://www.alphavantage.co/documentation/)
- File: [`HistoricalData.csv`](./HistoricalData.csv)
- Range: **Dec 1, 2024 → Mar 31, 2025**
- Fields used: `Date`, `Close/Last`, and `High`

---

##  How to Run It (Google Colab)

1. Open the notebook in [Google Colab](https://colab.research.google.com/)
2. At the top of the notebook, run this cell:
   ```python
   !wget https://raw.githubusercontent.com/justliya/Algorithm-Projects/main/HistoricalData.csv

	3.	Run all cells to:
	•	Load and clean the dataset
	•	Run the binary search to detect the first threshold cross
	•	Visualize the full stock trend and annotated events


Author

Aaliyah Johnson
Full Stack Developer | AI Enthusiast | Algorithm Explorer
GitHub: @justliya



📎 License

MIT License
