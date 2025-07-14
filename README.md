# 🚗 Jack's Car Rental Problem — Dynamic Programming with Policy Iteration

This project implements the classic **Jack's Car Rental** problem from the book *"Reinforcement Learning: An Introduction"* by **Richard S. Sutton and Andrew G. Barto**, using **Policy Iteration** to solve it as a Markov Decision Process (MDP).

## 📌 Problem Overview

Jack owns two locations for car rentals. Each day, rental and return requests occur at both locations, modeled as **Poisson random variables**. Jack can move cars between the two locations overnight, with costs and constraints. The objective is to determine the **optimal car transfer policy** that maximizes long-term expected returns.

**This project covers:**

- ✅ The original version of the problem  
- 🔁 A modified version with:  
  - Free transfer of one car  
  - Parking cost for more than 10 cars at a location  

## 🔍 Key Concepts

- **Markov Decision Processes (MDP)**  
- **Policy Evaluation**  
- **Policy Improvement**  
- **Policy Iteration**  
- **Poisson Distribution modeling**  
- **Temporal Difference Learning** (in concept)  
- **Numba JIT** compilation for performance optimization  

## ⚙️ Implementation Highlights

- **State Space**: Number of cars at each location (0–20)  
- **Action Space**: Cars moved between locations (–5 to +5)  
- **Reward**: +$10 per rental, –$2 per moved car, optional parking penalties  
- **Environment Simulation**: Uses `scipy.stats.poisson` and precomputed transition probabilities  
- **Visualization**: Heatmaps for optimal policy and state values using `seaborn` and `matplotlib`  

## 🧠 Algorithm Used

**Policy Iteration**:
- **Policy Evaluation**: Compute value function for the current policy until convergence.  
- **Policy Improvement**: Improve the policy greedily based on updated values.  
- Repeat until the policy is stable.  
