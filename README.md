# Quantum Error Correction (QEC) Simulation: Cat States

This project simulates and visualizes a basic Quantum Error Correction (QEC) protocol for a **Schr&ouml;dinger Cat State** using the QuTiP library. 

## Overview

In quantum computing, "Cat States" are superpositions of two coherent states with opposite phases. These states are highly sensitive to environmental noise, particularly **photon loss**, which changes the parity of the state. This simulation demonstrates how to detect such an error using parity measurements and restore the original state.

## Key Features

- **State Preparation**: Generates an initial "Even" Cat State ($|\alpha\rangle + |-\alpha\rangle$).
- **Error Simulation**: Introduces a single-photon loss event ($a$ operator), which transforms the Even Cat into an "Odd" Cat State.
- **Error Detection (Syndrome)**: Uses the parity operator $e^{i\pi a^\dagger a}$ to identify the change in the quantum state.
- **Recovery**: Applies a recovery operation to restore the state with high fidelity (~0.9285).
- **Dynamic Visualization**: Produces a looping animation of the Wigner function to show the evolution: 
  1. Initial State → 2. Photon Loss → 3. Recovery Process → 4. Reset.

## Technical Requirements

- **Python 3.x**
- **QuTiP**: Quantum Toolbox in Python
- **NumPy & Matplotlib**: For numerical calculations and plotting
- **FFmpeg**: Required for generating the HTML5 video animation

## How to Use

1.  **Install Dependencies**: Run `pip install qutip`.
2.  **Run the Simulation**: Execute the main Python cell. It will perform the quantum mechanical calculations and determine the recovery success.
3.  **View Results**: The output includes a "Result" message confirming the error detection and an embedded HTML5 video showing the Wigner function transformation in real-time.

## Results

The recovery process is evaluated using **Fidelity**, which measures how close the restored state is to the original. In this specific configuration ($\\alpha = 2.5$, $N=40$), we achieve a fidelity of approximately **0.9285**.
