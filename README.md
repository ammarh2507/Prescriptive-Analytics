# 🏥 Physician Scheduling Optimization

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Gurobi](https://img.shields.io/badge/Optimizer-Gurobi-orange)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)
![Type](https://img.shields.io/badge/Type-Prescriptive%20Analytics-purple)

## 📌 Overview
This project develops an optimized physician scheduling system using **Gurobi (MIP)** and **Python**.  
The objective is to **minimize the number of physicians** while ensuring demand coverage and complying with realistic labor constraints.

---

## ⚙️ Key Features
- 3-shift system: **Early (E), Late (L), Night (N)**  
- Weekly cyclic schedule  
- Real-world constraints:
  - Max 40 hours/week  
  - 10-hour rest between shifts  
  - 2 consecutive days off  
  - Limited shift-type combinations  
  - Max 3 consecutive night shifts  

---

## 🧠 Approach

### 🔹 Deterministic Model (Q2)
- Uses **mean demand + emergency buffer**
- Output: **28 physicians**

### 🔹 Simulation Analysis (Q3)
- Tested across 14 demand scenarios  
- Measured:
  - Undercoverage (physician-hours)
  - Utilization per shift

### 🔹 Stochastic Model (Q4)
- Accounts for demand uncertainty  
- Constraint:
  > Expected undercoverage ≤ 1 physician-hour per shift  
- Output: **29 physicians** (more robust schedule)

---

## 📊 Key Insights
- Deterministic solutions are cost-efficient but less robust  
- Stochastic optimization improves reliability with minimal cost increase  
- Night shifts show **low utilization**, indicating overstaffing due to constraints and safety buffers  

---

## 🛠️ Tech Stack
- Python (Pandas, NumPy, Matplotlib)  
- Gurobi Optimizer  

---

## 📁 Files
- `Prescriptive Analytics Final Project.ipynb` → Full implementation  
- `Project_Data.csv` → Demand data (14 weeks)  

---

## 🚀 Run Locally
```bash
pip install pandas numpy matplotlib gurobipy
jupyter notebook
