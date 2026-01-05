# 🎬 TikTok-Style Recommendation Analytics & A/B Testing

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white"/>
  <img src="https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white"/>
  <img src="https://img.shields.io/badge/Scikit--Learn-F7931E?style=flat&logo=scikit-learn&logoColor=white"/>
  <img src="https://img.shields.io/badge/SciPy-8CAAE6?style=flat&logo=scipy&logoColor=white"/>
  <img src="https://img.shields.io/badge/Matplotlib-11557C?style=flat"/>
</p>

---

## 📌 Overview

This project simulates a **short-form video recommendation system** and evaluates the impact of personalization using **controlled A/B testing**.  
The goal is to measure **causal engagement uplift** while ensuring **creator fairness and long-tail discovery**, similar to real-world experimentation workflows used at large-scale platforms.

---

## 🎯 Problem Statement

How can we verify that a personalized recommendation algorithm:
- increases user engagement  
- produces statistically valid improvements  
- does not harm creator diversity  

without relying on offline accuracy alone?

---

## 🧠 Core Concepts Used

- Implicit feedback modeling (watch time)
- Collaborative filtering
- A/B experimentation
- Statistical significance testing
- Algorithmic fairness (creator exposure)

---

## 🏗️ System Design

### 1. Data Simulation
- Generated realistic user–video interactions using **latent user preferences**
- Modeled behavioral noise to reflect real user variability
- Used watch time as the primary engagement signal

---

### 2. Recommendation Strategies

**Control (A): Popularity-Based Feed**
- Ranks videos by average watch time
- Same recommendations shown to all users
- Serves as a non-personalized baseline

**Treatment (B): Personalized Feed**
- Built using **Truncated SVD (collaborative filtering)**
- Learns latent user preferences and video characteristics
- Generates personalized top-K recommendations per user

---

### 3. A/B Experimentation
- Users randomly split into control and treatment groups
- Compared watch time on *recommended content*
- Measured uplift using exposure-aligned metrics
- Validated results using a two-sample t-test

---

### 4. Statistical Validation
- Computed uplift in average watch time
- Verified statistical significance (p-value)
- Ensured causal interpretation of results

---

### 5. Fairness & Creator Analysis
- Measured creator exposure inequality using **Gini coefficient**
- Evaluated **long-tail exposure share**
- Ensured personalization supports discovery of smaller creators

---

## 📊 Key Results

- Engagement uplift of approximately **52%** over popularity baseline
- Results statistically significant (**p < 1e-50**)
- Personalized feed allocated **~46% of exposure to long-tail creators**
- Baseline feed resulted in zero long-tail exposure

---

## ⚖️ Fairness Insight

Uniform exposure is not inherently fair.  
Personalization introduces exposure variance, but significantly improves **creator discovery** and ecosystem health.

---

## 🛠️ Technologies Used

- Python  
- Pandas, NumPy  
- Scikit-learn (Truncated SVD)  
- SciPy (statistical testing)  
- Matplotlib  
- Jupyter / Paperspace  

---

## 🚀 Why This Project Matters

- Focuses on **causal evaluation**, not just model performance
- Mirrors real-world product experimentation pipelines
- Balances engagement optimization with fairness considerations
- Demonstrates end-to-end data science thinking

---

## 🔮 Future Work

- Neural collaborative filtering (two-tower models)
- Retention and session-level metrics
- Exploration–exploitation strategies
- Online learning simulations

---

## 📄 Author

Anandha Ragaven Ravi  
M.S. in Applied Artificial Intelligence  

