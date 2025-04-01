# 📈 Network Analysis of S&P 500 Stocks using Gurobi and NetworkX

This project applies graph theory to stock market data to uncover structural relationships among companies in the S&P 500 index. Using correlation networks, we identify sector dominance, explore inter-company relationships, and visualize the market as a dynamic system.

---

## 🚀 Project Summary

- Analyzed daily log returns of S&P 500 companies from April 2020 onward to study stock behavior during and post-COVID
- Built correlation-based and distance-based networks to model inter-company relationships
- Applied **Maximum Clique** and **Minimum Spanning Tree (MST)** analysis
- Explored sector clustering and threshold-based network behavior (from -0.2 to 0.9)

---

## 🛠 Technologies & Libraries

- Python 3.8+
- Pandas, NumPy, Matplotlib, Seaborn
- NetworkX (graph modeling)
- Gurobi (for Maximum Clique optimization)

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
- Lower thresholds showed a broader spread of sectors (e.g., Real Estate, Energy, Financial Services, Communication Services)

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

**Threshold based Correlation network**

**(θ = 0.8) :**
![Theta 0.8](./12(0.8).png)
**(θ = 0.6) :**

**(θ = 0.25) :**

**Maximum Cliques in threshold networks**

**(θ = 0.8) :**

**(θ = 0.6) :**

**(θ = 0.25) :**

**Sector in Maximum Clique**

**(θ = 0.8) :**

**(θ = 0.6) :**

**(θ = 0.25) :**

**Distance-based Minimum spanning tree :**

![Minimum Spanning Tree](./Minimum%20Spanning%20Tree.png)

(For more detailed explanation and Visuals, See [Analysis of S&P 500 stocks_report.pdf](./Analysis%20of%20S&P%20500%20stocks_report.pdf))

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

Feel free to reach out via [LinkedIn](https://www.linkedin.com/in/prannoy-k/) or open an issue for questions or collaboration ideas!
