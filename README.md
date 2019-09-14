# Code for "Model weight theft with just noise inputs: The curious case of the petulant attacker"

## Generating spatially correlated data from Ising simulations
Refer to `cython_ising.ipynb`. This notebook contains code for generating MNIST-like images generated from Ising simulations via Gibbs sampling with 10 different thresholds for the inverse temperature parameter, beta. The beta values which are used are as follows: (0.0, 0.1, ... 0.9). The resulting files are in the same shape as the MNIST training and test sets, with labels corresponding to the beta value being used, and are saved as `train-images-isingmnist.npz`, `train-labels-isingmnist.npz`, `t10k-images-isingmnist.npz`, and `t10k-labels-isingmnist.npz`.

## `*_one_pixel.ipynb`
These files include the experiments for model extraction using the Bernoulli noise prior, among other priors, for various datasets. 

## `qmnist_numpy_prep.ipynb`
This notebook downloads data from the [facebookresearch/qmnist](https://github.com/facebookresearch/qmnist) repository. The exact preprocessing steps used to construct the original MNIST dataset have long been lost. This leaves us with no reliable way to associate its characters with the ID of the writer and little hope to recover the full MNIST testing set that had 60K images but was never released. The official MNIST testing set only contains 10K randomly sampled images and is often considered too small to provide meaninful confidence intervals.

The *QMNIST* dataset was generated from the original data found in the NIST Special Database 19 with the goal to match the MNIST preprocessing as closely as possible.
