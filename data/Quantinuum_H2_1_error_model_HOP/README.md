# Quantinuum H2-1 Error Model HOP results

- 500 random 21 qubit QV circuits
- `fold_global` circuit folding using Mitiq
- Circuit folding scale factors of lambda=1 and lambda=2
- HOP is computed using 2000 shots for lambda=1 and 2000 shots for lambda=2
- Error model is depolarizing noise, and measurement error bit flips, based on the randomized benchmarking calibrations of Quantinuum H2-1
  - 2023_03_10 calibration data from https://github.com/CQCL/quantinuum-hardware-specifications/

The data format is a JSON file where the keys are the circuit folding scale factors and the values are a list of length 500, corresponding to the heavy output probability (HOP) for each of the 500 random Quantum Volume circuits. 
