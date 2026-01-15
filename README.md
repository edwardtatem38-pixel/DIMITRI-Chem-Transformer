# DIMITRI-Chem-Transformer 🧪🤖

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
