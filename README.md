# DIMITRI-Chem-Transformer 🧪🤖

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/edwardtatem38-pixel/DIMITRI-Chem-Transformer/blob/main/Chemistry_llm_2.ipynb)

---

A Sequence-to-Sequence Transformer model for chemical reaction prediction, benchmarked on the USPTO dataset.

## 📊 Performance Benchmark
- **Dataset Size:** 10,000 Reactions (Forward Synthesis)
- **Architecture:** Transformer (Encoder-Decoder)
- **Format:** SELFIES (Self-Referencing Embedded Strings)
- **Hardware:** NVIDIA T4 GPU
- **Final Training Loss:** 1.5257

## 🔬 Key Results
The model successfully generalized to unseen reactions (e.g., Index #5005), demonstrating:
1. **Structural Integrity:** Correct generation of aromatic rings and branching.
2. **Atom Conservation:** Accurately tracking Halogens (Br, Cl, F) from reactants to products.
3. **Valid SMILES:** High percentage of chemically decodable outputs via RDKit.

## 🛠️ Usage
Requires `torch`, `selfies`, and `rdkit`.

## 💾 Model Weights (DIMITRI-v1)
The trained weights for this benchmark are hosted on Google Drive to ensure high-speed access and bypass GitHub file size limits.

**Download the weights here:** 👉 [DIMITRI Model Weights Folder](https://drive.google.com/drive/folders/1gLkvvnXhgnRBBA4zeClgK18qnpGOpNAe?usp=sharing)

### 🧪 How to Load
After downloading `chemist_model_sprint.pth` and uploading it to your own Colab session, use the following code:
```python
model.load_state_dict(torch.load('chemist_model_sprint.pth'))
model.eval()
