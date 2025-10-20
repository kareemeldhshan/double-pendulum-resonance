# Double Pendulum: Modes and Resonance

A study of normal modes and resonance behavior in a double pendulum system using Python.

---

## 📘 Overview

This project investigates the **motion of a double pendulum**, focusing on its **normal modes**, **coupled oscillations**, and **resonance behavior**.  
Using both analytical derivations and numerical integration, the notebook demonstrates how two pendulums coupled through a common pivot or spring exchange energy and exhibit rich dynamical behavior.

---

## 🧮 Derivation Summary

Starting from the **Lagrangian formulation**, the motion of each pendulum is described by generalized coordinates  
\[
\theta_1(t), \quad \theta_2(t)
\]
representing small angular displacements from equilibrium.

The **kinetic energy** and **potential energy** are given by:

\[
T = \frac{1}{2} m l^2 (\dot{\theta}_1^2 + \dot{\theta}_2^2), \quad
V = mgl \left( \frac{\theta_1^2 + \theta_2^2}{2} \right) + k (\theta_1 - \theta_2)^2
\]

Using the **Euler–Lagrange equations**,

\[
\frac{d}{dt} \left( \frac{\partial L}{\partial \dot{\theta}_i} \right) -
\frac{\partial L}{\partial \theta_i} = 0, \quad i = 1, 2
\]

we obtain the **coupled equations of motion**:

\[
\begin{aligned}
\ddot{\theta}_1 + \frac{g}{l} \theta_1 + \frac{2k}{m}(\theta_1 - \theta_2) &= 0 \\
\ddot{\theta}_2 + \frac{g}{l} \theta_2 - \frac{2k}{m}(\theta_1 - \theta_2) &= 0
\end{aligned}
\]

Solving for harmonic motion \( \theta_i = A_i e^{i\omega t} \) yields the **normal mode frequencies**:

\[
\omega_{\pm}^2 = \frac{g}{l} + \frac{2k}{m} \left( 1 \pm 1 \right)
\]

- **Symmetric mode** (in-phase): \( \omega_-^2 = \frac{g}{l} \)  
- **Antisymmetric mode** (out-of-phase): \( \omega_+^2 = \frac{g}{l} + \frac{4k}{m} \)

At resonance, energy periodically transfers between pendulums, producing beating patterns characteristic of coupled oscillators.

---

## ⚙️ Features

- Derivation of the coupled equations of motion  
- Linearization and identification of normal modes  
- Resonance analysis via numerical integration  
- Visualization of amplitude exchange and phase relationships  
- Code cells structured for clarity and educational use  

---

## 📂 Contents

- **`Double_Pendulum_Modes_and_Resonance.ipynb`** — Complete notebook with derivations, code, and plots  
- *(Optional)* Add any figures or data files to a `/figures` or `/data` folder  

---

## 🧰 Requirements

Install the required Python packages:

```bash
py -m pip install numpy matplotlib scipy
```

or, if you use the standard Python command:

```bash
pip install numpy matplotlib scipy
```

---

## 🚀 Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/double-pendulum-modes.git
   cd double-pendulum-modes
   ```
2. Open the notebook:
   ```bash
   jupyter notebook Double_Pendulum_Modes_and_Resonance.ipynb
   ```
3. Run all cells to reproduce the analysis and visualizations.

---

## 📊 Results Preview

To add a figure or animation preview later, include something like:

```markdown
![Double Pendulum Simulation](figures/pendulum.gif)
```

---

## 🧠 Insights

- The system exhibits **two characteristic frequencies**, corresponding to in-phase and out-of-phase oscillations.  
- The **energy exchange** between pendulums results in slow beating patterns at near-resonant frequencies.  
- The notebook provides both theoretical and computational verification of these behaviors.

---

## 🏷️ License

Released under the MIT License.

---

## ✍️ Author

Developed by **Kareem Ali**  
Physics and Python Enthusiast
