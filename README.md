# Code for "Model weight theft with just noise inputs: The curious case of the petulant attacker"

## Generating spatially correlated data from Ising simulations
Refer to `cython_ising.ipynb`. This notebook contains code for generating MNIST-like images generated from Ising simulations via Gibbs sampling with 10 different thresholds for the inverse temperature parameter, beta. The beta values which are used are as follows: (0.0, 0.1, ... 0.9). The resulting files are in the same shape as the MNIST training and test sets, with labels corresponding to the beta value being used, and are saved as `train-images-isingmnist.npz`, `train-labels-isingmnist.npz`, `t10k-images-isingmnist.npz`, and `t10k-labels-isingmnist.npz`.

## `*_one_pixel.ipynb`
These files include the experiments for model extraction using the Bernoulli noise prior, among other priors, for various datasets. 
