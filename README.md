# Low-Rank Matrix Completion (LRMC) Quantum State Tomography

## Overview
This repository contains the implementation of the Low-Rank Matrix Completion (LRMC) method for quantum state tomography, as proposed in our paper titled "Efficient Quantum State Estimation with Low-Rank Matrix Completion." This method is designed to efficiently estimate pure quantum states with a minimal number of measurements. The LRMC method utilizes local Pauli measurements to reconstruct the density matrix of a quantum state by completing missing entries using a low-rank matrix completion algorithm. The approach significantly reduces the complexity of quantum state estimation compared to traditional methods.

The implementation provided here aims to validate and benchmark the accuracy of LRMC on noisy intermediate-scale quantum (NISQ) devices. This code can be used to perform quantum state estimation on simulated data, or on real quantum devices such as those provided by IBMQ, for up to several qubits.

## Citation
If you use this code, please cite our paper:

```
@article{tariq2024efficient,
  title={Efficient quantum state estimation with low-rank matrix completion},
  author={Tariq, Shehbaz and Farooq, Ahmad and Rehman, Junaid Ur and Duong, Trung Q and Shin, Hyundong},
  journal={EPJ Quantum Technology},
  volume={11},
  number={1},
  pages={50},
  year={2024},
  publisher={Springer Berlin Heidelberg}
}
```

## Method Summary
The LRMC approach reconstructs the quantum state using only \(2n + 1\) local Pauli measurements for an \(n\)-qubit state, which makes it experimentally more feasible compared to entangling bases measurements that are prone to errors in NISQ devices. The core steps of the LRMC algorithm include:

1. **Measurement**: Local Pauli measurements are taken on each subsystem of the quantum state.
2. **Matrix Completion**: The density matrix is reconstructed using matrix completion, where missing elements are computed via rank-1 approximations.
3. **Singular Value Shrinkage**: The rank of the reconstructed matrix is controlled using the Eckart-Young theorem to ensure accurate estimation.

Our experimental results show that the LRMC approach outperforms contemporary methods, such as scalable estimation and the five-basis method, in terms of fidelity and computational efficiency.

## Running the Code
The provided Jupyter notebook contains all the necessary steps to implement the LRMC method. Users can modify the parameters such as the number of qubits, the number of shots, and the backend (simulated or real quantum hardware). Please make sure to remove any sensitive information, such as API keys, before using the code.

## Requirements
- Python 3.7+
- Qiskit
- QuTiP
- NumPy
- Pandas
- Matplotlib

You can install the required packages using:
```sh
pip install qiskit qutip numpy pandas matplotlib
```

## License
This code is licensed under the MIT License. For more information, refer to the LICENSE file.

## Acknowledgments
We acknowledge the use of IBMQ for running some of the experiments in this project. Special thanks to the National Research Foundation of Korea (NRF) for supporting this work.

## Contact
For questions or inquiries, please contact Shehbaz Tariq at [shehbaz@khu.ac.kr](mailto:shehbaz@khu.ac.kr) and Ahmad Farooq at [ahmad.farooq@aalto.fi](mailto:ahmad.farooq@aalto.fi)

