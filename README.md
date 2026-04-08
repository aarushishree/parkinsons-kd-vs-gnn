🧠 Parkinson’s Disease Detection in Unaligned Multimodal Data using Knowledge Distillation vs Graph Neural Networks
📌 Overview

This project presents a comparative study between Knowledge Distillation (KD) and Graph Neural Networks (GNN) for early detection of Parkinson’s disease using unaligned multimodal data:

🧠 Brain MRI
✍️ Handwriting (spiral & wave patterns)
🎙️ Voice (biomedical speech features)
⚠️ Unaligned Multimodal Setting

Unlike traditional multimodal learning, the datasets used in this study are unaligned, meaning:

Samples across modalities do not correspond to the same individuals
No direct pairing exists between brain, handwriting, and voice samples

This reflects real-world scenarios, where collecting synchronized multimodal data is often impractical.

🚀 Key Contributions
✅ Proposed a Knowledge Distillation (MADTKD) framework for unaligned multimodal learning
✅ Developed a Graph Neural Network (MHGNet) with inter-modal edge construction
✅ Designed soft-label based cross-modal connections for unaligned data
✅ Performed extensive ablation studies
✅ Demonstrated that KD outperforms GNN in unaligned settings
✅ Provided comprehensive experimental evaluation with visual evidence
📊 Results Summary
Method	Accuracy	AUC	F1 Score
KD (MADTKD)	84.62%	0.9517	0.8504
GNN (MHGNet)	71.79%	0.8552	0.7352
🔍 Key Insight

Knowledge Distillation provides better generalization and stability, while GNN struggles to model cross-modal relationships in unaligned multimodal datasets.

🧪 Datasets

This project uses publicly available datasets from different sources (unaligned):

🎙️ Voice Dataset
Source: UCI Parkinson’s Dataset : https://archive.ics.uci.edu/dataset/174/parkinsons
Features include jitter, shimmer, HNR, RPDE, etc.
✍️ Handwriting Dataset
Kaggle: Parkinson's Drawings Dataset : https://www.kaggle.com/datasets/kmader/parkinsons-drawings
Spiral and wave patterns used for Parkinson’s detection
🧠 Brain MRI Dataset
Kaggle: Parkinson's Brain MRI Dataset : https://www.kaggle.com/datasets/irfansheriff/parkinsons-brain-mri-dataset
MRI scans labeled for classification

⚠️ Note:
These datasets are independently collected and unaligned, meaning:

No subject-level correspondence exists across modalities
This introduces additional complexity in multimodal learning

Datasets are not included in this repository due to licensing restrictions.

📂 Repository Structure
parkinsons-kd-vs-gnn/
├── main_notebook.ipynb     # Complete pipeline (EDA → KD → GNN → Comparison)
├── figures/                # All experimental figures used in paper
├── requirements.txt        # Dependencies
└── README.md
⚙️ Installation
pip install -r requirements.txt
▶️ How to Run
Open main_notebook.ipynb in Google Colab
Download datasets from the links above
Update dataset paths if required
Run all cells sequentially
📈 Figures

The figures/ directory contains all experimental visualizations:

📊 Training curves
🔍 Confusion matrices
📈 ROC curves
🔬 KD and GNN ablation studies
⚖️ KD vs GNN comparison
🧠 Methodology
🔹 Knowledge Distillation (MADTKD)
Teacher models: Brain & Handwriting
Student model: Voice
Multi-source distillation with confidence weighting
Designed specifically for unaligned multimodal data
🔹 Graph Neural Network (MHGNet)
Intra-modal k-NN graphs
Inter-modal edges using soft-label similarity
Attempts to bridge unaligned modalities via graph structure
🔬 Experimental Findings
KD significantly improves voice modality performance
GNN struggles with noisy cross-modal relationships
Inter-modal edges introduce instability in unaligned data
KD achieves higher AUC → better decision boundaries
📌 Reproducibility
Full pipeline available in a single notebook
Pre-generated figures included
Dependencies listed in requirements.txt
👩‍💻 Author

Aarushi Shreevastava
B.Tech Computer Science & Engineering

📜 License

For academic and research purposes only

⭐ Acknowledgment

Thanks to open-source datasets and the research community
