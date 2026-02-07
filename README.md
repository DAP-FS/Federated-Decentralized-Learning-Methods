# FedAvg Reproduction on MNIST (IID vs Non-IID)

This repository reproduces key MNIST experiments from:

**McMahan et al. (AISTATS 2017)** — *Communication-efficient learning of deep networks from decentralized data*  
using **Federated Averaging (FedAvg)** with **IID** and **non-IID** client partitions, and two model families:
- **2NN (MLP with 2 hidden layers)**  
- **CNN (2 conv layers + FC)**

This README documents the exact experimental design, hyperparameters, and results reported in the experiment note.  

---

## What We Reproduce

### Core question
Train deep networks on **decentralized, non-IID** data with **minimal communication**, measuring:
- **test accuracy vs communication rounds**
- **rounds-to-target accuracy** under different client sampling rates and data heterogeneity

### Conditions reproduced
- Dataset: **MNIST**
- Clients: **N = 100**
- Clients sampled per round: **m ∈ {10, 50}**
- Data partitions: **IID** and **non-IID**
- Models: **2NN** and **CNN**
- Client training: sequential execution with a **running sum of model parameters** for aggregation (memory-saving approach)
- Evaluation: test accuracy computed **after every round**
- Reported metric: **first round** where test accuracy crosses:
  - **XX** for 2NN
  - **XX** for CNN

---

## Repository Layout (suggested)
> Adjust if your repo differs; keep naming consistent for collaborators.
