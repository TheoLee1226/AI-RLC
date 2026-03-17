# AI-RLC
**Physics-Informed Neural Networks for RLC Circuit Modeling**

This project demonstrates how **Physics-Informed Neural Networks (PINNs)** can be applied to model and analyze an **RLC circuit**.  
Instead of relying solely on traditional numerical methods, the neural network is trained while enforcing the **underlying physical laws of the circuit**.

The goal is to explore how machine learning can assist in:

- Modeling electrical systems  
- Predicting circuit responses  
- Fitting experimental data  
- Comparing learned models with physical simulations  

---

# Project Overview

An RLC circuit follows a differential equation derived from **Kirchhoff's Voltage Law (KVL)**:

$$
L \frac{d^2 q}{dt^2} + R \frac{dq}{dt} + \frac{q}{C} = V(t)
$$

where

- $R$ — resistance  
- $L$ — inductance  
- $C$ — capacitance  
- $q(t)$ — charge  
- $V(t)$ — input voltage  

Traditional approaches solve this equation numerically.  
In this project, a **Physics-Informed Neural Network (PINN)** is trained to satisfy both:

1. Observed data  
2. The governing differential equation  

This allows the model to learn physically consistent behavior.

---

# Repository Structure

```text
AI-RLC
│
├── RLCpinn_simulation.ipynb
│   Generate simulated RLC circuit data
│
├── RLCpinn_fit.ipynb
│   Train PINN model to fit circuit behavior
│
├── RLCpinn_predict.ipynb
│   Use the trained model to predict system response
│
├── RLCpinn_predict_compare.ipynb
│   Compare PINN predictions with simulation results
│
└── README.md

---

# Methods

This project uses **Physics-Informed Neural Networks (PINNs)** which combine:

- Neural networks
- Differential equation constraints
- Data fitting

The training loss includes:

Data loss:

$$
L_{\text{data}}
$$

Physics loss:

$$
L_{\text{physics}}
$$

Total loss:

$$
L = L_{\text{data}} + \lambda L_{\text{physics}}
$$

This ensures the model predictions satisfy the **RLC differential equation**.

---

# Technologies Used

- Python  
- PyTorch / TensorFlow  
- NumPy  
- Matplotlib  
- Jupyter Notebook  

---

# Applications

Possible applications include:

- Circuit system identification  
- Sensor modeling  
- Electrical system prediction  
- Physics-guided machine learning research  

---

# Future Work

Potential improvements:

- Real experimental data integration  
- Parameter estimation of $R$, $L$, $C$  
- Noise-robust PINN training  
- Comparison with classical ODE solvers  

---

# Author

**Theo Lee**  
National Cheng Kung University  

