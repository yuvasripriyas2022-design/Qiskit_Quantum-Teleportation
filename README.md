# 🧠 Qiskit Quantum Teleportation

This repository demonstrates **Quantum Teleportation** using **Qiskit 2.x** — a fundamental quantum information protocol that transfers an unknown quantum state from one qubit (Alice) to another (Bob) using **entanglement** and **quantum operations**.

---

## 📘 Description

The Jupyter notebook [`Qiskit_Quantum Teleportation.ipynb`](./Qiskit_Quantum%20Teleportation.ipynb) implements the *coherent version* of quantum teleportation, which avoids classical conditional operations (`.c_if`) and instead uses quantum-controlled corrections for full compatibility with **Qiskit 2.x**.

### ✨ Key Steps in the Notebook
1. **State Preparation** — creates an arbitrary single-qubit state \(|ψ⟩\).
2. **Entanglement Creation** — forms a Bell pair between Alice and Bob.
3. **Bell Measurement (Coherent)** — applies quantum gates to perform Bell-basis transformation.
4. **Coherent Corrections** — teleports \(|ψ⟩\) to Bob using controlled gates.
5. **Simulation and Verification** — computes fidelity (expected ≈ 1.0).
6. **Visualization** — shows Bloch sphere of Bob’s qubit.

---

## ⚙️ Requirements

- Python 3.9+
- Qiskit 2.x
- Matplotlib
- NumPy

To install the required libraries:

```bash
pip install qiskit qiskit-aer matplotlib numpy
```

---

## ▶️ How to Run

1. Open the notebook in JupyterLab or VSCode.
2. Run all cells to simulate the teleportation process.
3. Observe:
   - The **fidelity** between Alice’s and Bob’s qubits (≈ 1.0).
   - Bloch sphere visualization confirming successful teleportation.

---

## 🎓 Student Programming Tasks

To deepen your understanding, try the following tasks using the same notebook:

### 🧩 **Task 1: Custom State Teleportation**
Modify the input state preparation:
```python
qc.ry(theta, 0)
qc.rz(phi, 0)
```
Experiment with different values of `theta` and `phi` (e.g., π/4, π/2, etc.) and visualize how the Bloch vector changes.

---

### 🔄 **Task 2: Add Classical Measurement**
Modify the code to include actual **measurements** of qubits 0 and 1, and then use conditional corrections with `if_test()` or `.c_if()` syntax.

---

### 📈 **Task 3: Fidelity Analysis**
Run teleportation for multiple random states (sample 10–20 different `(theta, phi)` pairs) and compute the **average fidelity**.  
Plot fidelity values to show teleportation accuracy.

---

### 🎨 **Task 4: Step-by-Step Visualization**
Insert Bloch sphere visualizations after each major operation (`H`, `CX`, `CZ`) to create an animation showing how the quantum state “moves” across qubits.

---

### 🔍 **Task 5: Introduce Noise**
Use `AerSimulator(noise_model=...)` to add a small depolarizing or amplitude damping noise model.  
Study how teleportation fidelity decreases under noisy conditions.

---

## 🧩 Output Example

```
Fidelity between initial and teleported states: 1.000000
```

A Bloch sphere visualization appears confirming that Bob’s qubit matches Alice’s initial state.
