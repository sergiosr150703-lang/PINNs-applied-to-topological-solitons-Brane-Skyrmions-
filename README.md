# Quantization of Topological Solitons in Brane Theories

**Author:** Sergio Sánchez Rentero  
**Institution:** Universidad Complutense de Madrid (Master in Theoretical Physics)  
**Contact:** sergis15@ucm.es  
**Links:** [GitHub Profile](https://github.com/sergiosr150703-lang) 

## Associated Thesis
This repository contains the source code for the Master's Thesis: *"Quantization of Topological Solitons in Brane Theories"* (Academic Year 2025-26). 

*(Note: A link to the final PDF or arXiv preprint will be added here once published).*

## Project Overview (Abstract)
In this work, we investigate the canonical quantization of **topological solitons in brane-world scenarios**. We focus specifically on Brane-Skyrmions. These topological field configurations are similar to standard Skyrmions and emerge as solutions to the Dirac-Nambu-Goto action with an induced curvature term. By **quantizing the spin collective coordinates** of the Brane-Skyrmion, we find that the resulting Hamiltonian contains contributions at arbitrarily high orders in $J^2$. This provides a clear advantage over the standard Skyrme model. Furthermore, we implement a **Physics-Informed Neural Network (PINN)** to find the soliton profile that **minimizes the energy**, properly incorporating the backreaction from the quantized spin degrees of freedom. Finally, we discuss the potential applications of this framework to **describe hadronic spectra**. These results show the theoretical potential of brane-defect models and the increasing importance of neural networks in theoretical physics.

## Repository Structure
The repository is divided into two main computational frameworks: symbolic/exact numerical calculations and machine learning optimization.

* **`Mathematica/`**
  * `Perturbative Brane-Skyrmions.nb`: Symbolic computation notebook. It calculates the perturbative Hamiltonian for the rotating soliton and derives the Taylor series expansion terms for the induced scalar curvature.
  * `Brane-Skyrmions profile.nb`: Numerical computation notebook. It solves the non-linear second-order differential equation for the classical, static Brane-Skyrmion profile using the exact Shooting Method.

* **`Python_PINN/`**
  * `Brane-Skyrmions_PINN.ipynb`: The core Machine Learning notebook. It defines the PINN architecture in PyTorch, evaluates the dynamic energy functionals, and performs the phenomenological fits to empirical hadronic spectra (Nucleon and Delta resonances).

## Requirements & Dependencies
To run the codes in this repository, you will need:

**For the Python PINN:**
* Python 3.8+
* `torch` (PyTorch)
* `numpy`
* `matplotlib`
* `ipywidgets` (for live training visualizations in Jupyter)

**For the Mathematica Notebooks:**
* Wolfram Mathematica 13.0 or higher.

## Usage Guide
1. **Classical Baseline (Optional):** Run `Brane-Skyrmions profile.nb` in Mathematica to generate the exact classical profiles and export the results as `.csv` files into the `Data/` folder.
2. **Perturbative Coefficients (Optional):** Run `Perturbative Brane-Skyrmions.nb` if you wish to verify the symbolic derivation of the Hamiltonian expansion.
3. **Neural Network Optimization:** Open `Brane-Skyrmions_PINN.ipynb` in Jupyter Notebook. Ensure the path to the ground-truth `.csv` data is correctly set if you wish to plot the shooting method comparison. Run the cells sequentially to train the PINN and obtain the quantized dynamic profiles.

## License
This project is licensed under the [MIT License / GNU GPLv3] - see the LICENSE file for details. You are free to use, modify, and distribute this code, provided proper attribution is given.
