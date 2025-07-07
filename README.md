# Optimisation in Memory-Constrained Architectures

**Project Title:**  
Benchmarking First vs. Second-Order Optimizers on ResNet-18 (CIFAR-10)

**Authors:**  
- Nouhaila Hajjaoui  
- Salma Salama  
- Salah Eddine Khaldouni  

**Supervisors:**  
- Prof. Faouzia Benabbou  
- Dr. Zineb Ellaky  

## Project Structure

├── CodeOptimisationFinale5.ipynb      
├── Rapport_Optimisation_v3_tex.pdf                            
├── README.md                          


## Description

This project benchmarks four optimizers under memory-constrained conditions:

- **SGD with momentum**
- **Adam**
- **Shampoo**
- **K-FAC**

The benchmark focuses on the **ResNet-18** architecture using the **CIFAR-10** dataset and uses **gradient checkpointing** to simulate constrained environments.

Metrics measured:
- Accuracy
- Training time
- GPU/CPU consumption
- Stability across seeds
- RAM and GPU memory usage


## How to Run

### 1. Open the Notebook

Use the following notebook:

**`CodeOptimisationFinale5.ipynb`**

> The notebook is **fully self-contained**: it includes all necessary code to load libraries, the CIFAR-10 dataset, optimizers (SGD, Adam, Shampoo, K-FAC), and run all experiments.

> Fully compatible with **Google Colab** or **Kaggle** (tested with dual Tesla T4 GPUs).


### 2. Execution

**No manual installation is required** if you run the notebook on Kaggle or Colab.  
Simply **run each cell in order**, no modification needed.


## Results Summary

| Optimizer | Accuracy (%) | Time (min) | Stability (σ) | GPU Mem (MB) | RAM (MB) |
|-----------|--------------|------------|----------------|----------------|----------|
| **Adam**      | 89.58       | 18.48      | 0.2870         | 1426           | 2453     |
| **SGD**       | 86.77       | 18.16      | 0.3332         | 1174           | 2300     |
| **K-FAC**     | 87.72       | 33.70      | 0.4060         | 4443           | 2703     |
| **Shampoo**   | 81.62       | 50.18      | 0.3961         | 1739           | 2638     |

> See `Rapport_Optimisation_v3_tex.pdf` for full analysis and figures.


## Conclusion

- **Adam** shows the best trade-off between accuracy and convergence.
- **SGD** is ideal for memory-constrained environments.
- **K-FAC** is accurate but memory-intensive.
- **Shampoo** suffers from instability and high training time.



## References

1. Kingma & Ba (2014), Adam
2. Martens & Grosse (2015), K-FAC
3. Anil et al. (2020), Shampoo
4. Chen et al. (2016), Gradient Checkpointing

For more details, see the bibliography in the PDF report.
