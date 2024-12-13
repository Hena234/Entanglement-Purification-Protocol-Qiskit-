# Qiskit Two-Qubit Protocol Simulation

## Exercise Overview

This repository contains a Qiskit implementation of a two-qubit quantum protocol exercise . The script demonstrates quantum circuit creation, simulation, and post-selection techniques.

### Implementation Details

- Uses a 4-qubit quantum circuit
- Applies Hadamard gates to qubits 0 and 2
- Introduces a small RZ gate rotation (0.01) on qubits 0 and 2
- Implements controlled-NOT (CNOT) gates between qubit pairs
- Performs measurements on all qubits
- Post-selects results for "00" and "11" states

## Prerequisites

- Python 3.8+
- Qiskit
- Matplotlib

## Installation

```bash
pip install qiskit matplotlib
```

## Code Breakdown

### Circuit Preparation
- Initialize 4-qubit circuit
- Apply Hadamard gates: `qc.h([0,2])`
- Add RZ gate rotation: `qc.rz(0.01,[0,2])`
- Apply CNOT gates: `qc.cx([0,2],[1,3])` and `qc.cx([0,1],[2,3])`
- Perform Hadamard gates on qubits 0 and 1
- Measure all qubits

### Simulation and Post-Processing
- Use Qiskit's `Sampler` for circuit execution
- Extract binary probabilities
- Post-select results for "00" and "11" states
- Visualize results using histogram plots

## Running the Simulation

```bash
python two_qubit_protocol.py
```

## Visualization

The script generates two histogram plots:
1. Measurement outcomes for "11" states
2. Measurement outcomes for "00" states

## Key Quantum Concepts

- Quantum state preparation
- Hadamard gates
- Controlled-NOT (CNOT) gates
- Noise modeling with RZ rotation
- Post-selection technique

## Requirements

- Qiskit
- Matplotlib for visualization

## License

[Apache 2.0]
```

