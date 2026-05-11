# EAMs-for-bounded-continuous-data



This repository contains the code and data used in our paper [Extending evidence accumulation models to bounded continuous self-report data](https://arxiv.org/pdf/2604.26055). In this paper, we fit and compare two models (the half-circular diffusion model (HCDM) and the beta diffusion model (BDDM)) to an empirical dataset.
The details of the method are described in our paper:

Wu, Y., Szűcs, T., Moors, A., & Tuerlinckx, F. (2026). Extending Evidence Accumulation Models to Bounded Continuous Self-report Data. 
<em>arXiv preprint arXiv:2604.26055</em>, available for free at: [https://arxiv.org/pdf/2604.26055](https://arxiv.org/pdf/2604.26055).

## Cite

```bibtex
@article{wu2026extending,
  title={Extending Evidence Accumulation Models to Bounded Continuous Self-report Data},
  author={Wu, Yufei and Szűcs, Tamás and Moors, Agnes and Tuerlinckx, Francis},
  journal={arXiv preprint arXiv:2604.26055},
  year={2026}
}
```

The repository is divided into four distinct parts.
## [notebooks_gpu](notebooks_gpu)

### [data](notebooks_gpu/affect_data_bf.txt)
- [affect_data](notebooks_gpu/affect_data_bf.txt): the empirical dataset used in this paper
  
### [jupyter notebook](notebooks_gpu)
- [inference_hcdm_gpu](notebooks_gpu/inference_hcdm_gpu.ipynb): code for simulating data from the HCDM on a GPU (raw cuda kernels), code for using the simulated data to train neural networks and learn a HCDM posterior estimator with amortized Bayesian inference (ABI), and code for the inference on the empirical dataset
- [inference_bddm_gpu](notebooks_gpu/inference_bddm_gpu.ipynb): code for simulating data from the BDDM on a GPU (raw cuda kernels), code for using the simulated data to train neural networks and learn a BDDM posterior estimator with ABI, and code for the inference on the empirical dataset
- [model_comparison_gpu](notebooks_gpu/model_comparison.ipynb): code for simulating data from both HCDM and BDDM (raw cuda kernels), code using the simulated data to train neural networks and learn a probabilistic classifier between two models with amortized Bayesian model comparison (ABMC), code for the model comparison based on the empirical dataset

## [notebooks_cpu](notebooks_cpu)

### [jupyter notebook](notebooks_cpu)
- [inference_hcdm_cpu](notebooks_cpu/inference_hcdm_cpu.ipynb): code for simulating data from the HCDM on a CPU, code for using the simulated data to train neural networks and learn a HCDM posterior estimator with ABI
- [inference_bddm_cpu](notebooks_cpu/inference_bddm_cpu.ipynb): code for simulating data from the BDDM on a CPU, code for using the simulated data to train neural networks and learn a BDDM posterior estimator with ABI

## [networks](networks)
- contains the trained neural networks in the paper and can be used to reproduce the results in the paper.
  
## License

MIT
