# Temporal-Hyperedge-Modeling-simplified-TPP-

# Temporal Hyperedge Modeling (Simplified TPP)

This project implements a lightweight, CPU-friendly model for temporal hyperedge interaction prediction, inspired by recent work on temporal point processes and dynamic graphs.

## References
This project reimplements and extends:
> Gracious, T., & Dukkipati, A. (2025). Deep Representation Learning
> for Forecasting Recursive and Multi-Relational Events in Temporal
> Networks. *AAAI 2025*.
Built upon prior work:
> Gracious, T., & Dukkipati, A. (2023). Dynamic Representation Learning
> with Temporal Point Processes for Higher-Order Interaction Forecasting.
> *AAAI 2023*.

---

## 🚀 Highlights

* Dynamic node embeddings over time
* Continuous-time evolution using neural ODEs
* Hyperedge (group interaction) modeling
* Structure-aware hard negative sampling (our contribution)

---

## 📊 Results

| Model                           | AUC    | AP      |
| ------------------------------- | -----  | -----   |
| Random Negative Sampling        | 0.4740 | 0.1610 |
| Structure-Aware Sampling        | 0.5260 | 0.1866 |

---

## 🧠 Key Idea

We explore how negative sampling affects learning in temporal models.

Instead of random negatives, we use **structure-aware hard negatives**:

* nodes sampled from 1-hop neighbors
* more challenging examples → better representations

---

## 📊 Dataset

Synthetic dataset with:

* temporal event sequences
* community structure
* variable hyperedge sizes

This allows controlled experimentation without heavy computation.

---

## 🔬 Method Overview

* Node embeddings evolve over time (ODE-based drift)
* Interactions update embeddings (GRU-based)
* Hyperedges modeled via aggregation
* Contrastive learning with negative sampling

---

## 🔗 Inspiration

Inspired by research on:

* Temporal point processes
* Dynamic graph learning
* Hypergraph interaction modeling

---

## 🛠️ Run

```bash
pip install torch torchdiffeq numpy pandas scikit-learn matplotlib
python notebook.ipynb
```

---

## 📌 Future Work

* Extend to real-world datasets
* Implement full likelihood-based TPP training
* Explore attention-based hyperedge encoding

---

