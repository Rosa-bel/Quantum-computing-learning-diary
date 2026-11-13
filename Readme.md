# Quantum Computing Practice

A personal learning journal in quantum computing: notebooks where I implement well-known algorithms, work through challenges found online, and try to understand *why* things work, not just that they work.

This is not a library or a framework. It is a trace of my learning path, shared in case it helps others who are starting out in quantum computing and want to see how someone else approaches the same problems.

> **Credits:** some of the notebooks are based on or adapted from material found on GitHub, written by the [IBM Qiskit community](https://github.com/Qiskit) and other authors working on quantum computing. See [Acknowledgements](#acknowledgements).

---

## What you will find here

- **Famous algorithms** implemented from scratch and tested on simulators.
- **Online challenges** (circuit design, variational algorithms, oracle construction, and similar problems) with my attempts and the reasoning behind them.
- **Small experiments** to build intuition: what happens to the amplitudes, which gate does what, why a given trick works.

Most notebooks mix code with written explanations, because the goal is understanding rather than just a working solution.

## Topics covered

| Area | Examples |
|---|---|
| Foundations | qubits, superposition, phases, statevector simulation |
| Circuit construction | building oracles, diagonal operators, multi-controlled gates |
| Classic algorithms | the well-known algorithms that every course covers |
| Variational methods | VQE-style problems, ansatz design |
| Quantum machine learning | notes and experiments around QML |

## Notebooks

| Notebook | What it covers |
|---|---|
| Diagonal ±1 matrix to circuit | Turning any diagonal matrix with entries +1 / -1 into a circuit using the ANF (algebraic normal form) and the Möbius transform, with Z / CZ / CCZ gates built step by step |

More notebooks will be added as I go.

## How to read the notebooks

1. Start with the markdown cells. They explain the idea before the code.
2. Run the cells in order. Most notebooks build up one step at a time.
3. Check the verification cells (usually a comparison of a simulated statevector or matrix with the expected one). They are there to confirm the reasoning.

Notebooks are not meant to be optimal or polished. Some contain dead ends or comments about what confused me, and I kept them on purpose.

## Getting started

**Requirements**

- Python 3.12 or later
- [Qiskit](https://qiskit.org/)
- NumPy
- Jupyter

**Install and run**

```bash
git clone <repository-url>
cd <repository-folder>

python -m venv .venv
source .venv/bin/activate        # on Windows: .venv\Scripts\activate

pip install qiskit numpy jupyter
jupyter notebook
```

Everything runs on a local simulator. No quantum hardware or account is needed.

## Conventions used

- **Qiskit is little-endian**: qubit 0 is the least significant bit, so the index of a basis state is `x = x0 + 2·x1 + 4·x2 + ...`.
- Basis states are written as bit strings in the order `x2 x1 x0`.
- Amplitudes are read from the statevector (`Statevector(circuit)`), not from measurements, so phases stay visible.

## Notes and caveats

- This is a learning repository. Explanations may be incomplete, and some of my reasoning may contain mistakes.
- Challenge solutions are my own attempts and are not necessarily the best known ones.
- If you spot an error or a clearer way to explain something, I would be glad to hear about it.

## Acknowledgements

Part of this repository builds on the work of others. Notebooks adapted from existing material come from the IBM Qiskit community and from other authors who share their quantum computing work on GitHub. The original source and author are credited at the top of each notebook concerned, and all rights remain with the original authors.

## Feedback

Suggestions, corrections and questions are welcome. Feel free to open an issue or a pull request.