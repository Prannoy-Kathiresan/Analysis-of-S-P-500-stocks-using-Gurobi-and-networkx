# 📈 Network Analysis of S&P 500 Stocks

This project applies graph theory to stock market data to uncover structural relationships among companies in the S&P 500 index. Using correlation networks, we identify sector dominance, explore inter-company relationships, and visualize the market as a dynamic system.

> 👨‍💻 Developed by: Nimit Kapadia, Prannoy Kathiresan, Shreekant Gokhale

---

## 🚀 Project Summary

- Analyzed daily log returns of 494 S&P 500 companies post-April 2020
- Built correlation-based and distance-based graphs
- Applied **Maximum Clique** and **Minimum Spanning Tree (MST)** analysis
- Explored sector clustering and threshold-based network behavior (from -0.2 to 0.9)

---

## 🛠 Technologies & Libraries

- Python 3.8+
- Pandas, NumPy, Matplotlib, Seaborn
- NetworkX (graph modeling)
- Gurobi & `gurobipy` (for Maximum Clique optimization)

---

## 🧪 Methods

### ✅ Data Processing
- Calculated daily **log returns** for stationarity
- Created a **Pearson correlation matrix**
- Converted correlations to distances: `d = √(2(1 - correlation))`

### 🔗 Correlation Networks
- Applied threshold values θ = -0.2 to 0.9 to build filtered graphs
- Extracted **Maximum Cliques** at each threshold to find tightly connected subgroups
- Color-coded nodes by sector

### 🌳 Minimum Spanning Tree (MST)
- Constructed MST from the distance matrix
- Visualized structural relationships and sector clustering

---

## 📊 Key Insights

- **Financial Services** was the dominant sector at higher correlation thresholds
- MST visualizations revealed strong intra-sector ties
- Lower thresholds showed a broader spread of sectors (e.g., Basic Materials, Industrials)

---

## 📂 Project Structure

```
├── data/                 # Raw & processed stock data
├── notebooks/            # Exploratory and visual analysis
├── scripts/              # Core logic for network construction and analysis
├── results/              # Visualizations and output graphs
└── report/               # Final PDF report and summary
```

---

## 🖼 Sample Visualizations

- Sector-labeled Maximum Clique graphs across thresholds
- Correlation-based threshold networks (θ = -0.2 to 0.9)
- MST graph showing company proximity by sector

*(See `/results` or [final-results.pdf](./report/final-results.pdf))*

---

## 📈 Future Improvements

- Add temporal network analysis to study market evolution
- Apply entropy and centrality measures for deeper structural insights
- Leverage findings for portfolio optimization and diversification strategies

---

## 📦 Setup Instructions

Clone the repo and install dependencies:

```bash
git clone https://github.com/your-username/sp500-network-analysis.git
cd sp500-network-analysis
pip install -r requirements.txt
```

### ⚡ Gurobi Note
This project uses the Gurobi Optimizer for solving the Maximum Clique problem. To use it:

1. [Get an academic license](https://www.gurobi.com/academia/academic-program-and-licenses/)
2. Install it with:

```bash
pip install gurobipy
```

---

## 📒 References

- Kaggle S&P 500 Stock Dataset  
- Kukreti et al. (2020), *Frontiers in Physics*  
- Kumar & Deo (2012), *Phys Rev E*  
- Boginski et al. (2003, 2004), *Financial and Economic Networks*

---

## 📩 Contact

Feel free to reach out via [LinkedIn](https://www.linkedin.com/in/prannoy-kathiresan) or open an issue for questions or collaboration ideas!
