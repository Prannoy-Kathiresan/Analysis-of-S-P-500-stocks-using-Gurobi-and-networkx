# 📈 Network Analysis of S&P 500 Stocks

This project applies graph theory to stock market data to uncover structural relationships among companies in the S&P 500 index. Using correlation networks, we identify sector dominance, explore inter-company relationships, and visualize the market as a dynamic system.

> 🧑‍💻 Developed by: Nimit Kapadia, Prannoy Kathiresan, Shreekant Gokhale

---

## 🚀 Project Summary

- Analyzed daily log returns of 494 S&P 500 companies post-April 2020
- Built correlation-based and distance-based graphs
- Applied **Maximum Clique** and **Minimum Spanning Tree (MST)** analysis
- Explored sector clustering and threshold-based network behavior

---

## 🛠 Technologies & Libraries

- Python 3.8+
- Pandas, NumPy, Matplotlib
- NetworkX (for graph modeling)
- Seaborn (optional for better plots)

---

## 🧪 Methods

### ✅ Data Processing
- Calculated daily **log returns** for stationarity
- Created a **Pearson correlation matrix**
- Converted correlations to distances: `d = √(2(1 - correlation))`

### 🔗 Correlation Networks
- Applied varying thresholds (e.g., θ = 0.25, 0.6, 0.9)
- Extracted **Maximum Cliques** at each level to detect strongly interconnected stocks
- Color-coded nodes by sector

### 🌳 Minimum Spanning Tree (MST)
- Visualized full market structure without data loss
- Highlighted intra-sector proximity and structure

---

## 📊 Key Insights

- **Financial Services** dominated at higher correlation thresholds
- MST revealed strong intra-sector clustering, indicating sectoral coherence
- Lower thresholds showed diversification and emergence of other sectors (e.g., Basic Materials, Industrials)

---

## 📂 Project Structure

├── data/                 # Raw & processed stock data
├── notebooks/            # Exploratory and visual analysis
├── scripts/              # Core logic for network construction and analysis
├── results/              # Visualizations and output graphs
└── report/               # Final PDF report and summary

---

## 🖼 Sample Visualizations

- Maximum Clique sector distributions across thresholds  
- Correlation threshold networks (θ = 0.25 to θ = 0.9)  
- MST showing proximity between company stocks  

*(See `/results` for visual outputs or [final-results.pdf](./report/final-results.pdf))*

---

## 📈 Future Improvements

- Add temporal analysis for evolving networks
- Integrate entropy and centrality metrics for robustness
- Use network patterns for portfolio optimization strategies

---

## 📦 Setup Instructions

Clone the repo and install dependencies:

```bash
git clone https://github.com/your-username/sp500-network-analysis.git
cd sp500-network-analysis
pip install -r requirements.txt
