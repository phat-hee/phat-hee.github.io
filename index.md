# Welcome 
I'm **Mohammad Fathi**, a **Master's graduate in Data Mining** from **Kharazmi University** (GPA: 3.74/4.0).  
My research interests are **Artificial Intelligence, Data Mining, and Computational Neuroscience**, with a focus on **neuroimaging analysis**, **biomedical signal processing**, and **BCI**.

I completed my master's degree **ranked 2nd** in my program, conducting my thesis research at the **Kharazmi Cognitive and Brain Science Lab** under the supervision of **Dr. Mir Mohsen Pedram**. I developed a **temporal graph neural network (TGNN)** framework to classify **Mild Cognitive Impairment (MCI)** and **healthy controls (HC)** using **fNIRS** resting-state data, earning a perfect thesis grade of **20/20**.

In my current job, I work with **NLP and LLM methods for RAG systems**.

## 🔬 Projects

### 🧠 fNIRS-based MCI Classification
Designed and implemented a **temporal graph neural network (GConvGRU)** to classify **Mild Cognitive Impairment (MCI)** and **Healthy Controls (HC)** from resting-state fNIRS data.  
[🔗 GitHub Repository](https://github.com/phat-hee/mci_fnirs_tgnn)  
I performed **all preprocessing and modeling steps** except for data acquisition.  
- Applied a **15-second sliding window** to segment preprocessed fNIRS signals.  
- Constructed temporal graphs representing functional connectivity dynamics.  
- Implemented and trained the **TGNN** architecture using PyTorch Geometric.  
- Evaluated model interpretability using graph-based feature importance analysis.  

This project formed the core of my **Master's thesis**, earning a perfect grade (20/20).

---
### ⚡ EEG Temporal Graph Neural Network for AD and FTD  
[🔗 GitHub Repository](https://github.com/phat-hee/eeg__temporalgraph_ad_ftd_hc)

Developed a **temporal graph neural network (TGNN)** framework to classify **Alzheimer's Disease (AD)**, **Frontotemporal Dementia (FTD)**, and **Healthy Controls (HC)** from resting-state EEG data. 
We used multiple explainability techniques (Integrated Gradients, Saliency Maps, and DeepLIFT from the Captum library) to identify the most influential nodes in the graph-based model. We then compared these model-derived nodes to two external references: (1) clinical reports describing the affected regions, and (2) a lobe-wise analysis. This let us evaluate how well the explainability outputs align with known clinical findings at both the node and lobe levels.  
I was responsible for **all stages of the technical development**, including data handling, model design, and full code implementation, while collaborating with a **team of researchers** who focused on report writing and documentation.  

- Processed pre-cleaned EEG data and generated **temporal functional connectivity graphs** using **Granger causality**.  
- Designed, coded, and optimized the entire **PyTorch-based pipeline**: graph generation, feature extraction, model architecture, and training.  
- Experimented with multiple GNN architectures and finalized a **GraphSAGE + LSTM** hybrid with **attention-based fusion** across **alpha** and **beta** frequency bands.  
- Performed both **whole-brain** and **lobe-level** analyses to identify the regions most relevant for each impairment type.  
- Showed that **attention mechanisms** improved interpretability by highlighting the contribution of frequency bands and brain regions.  
- Used explainability methods to identify important nodes and compared them to clinical reports and our lobe-wise method.

This project extended the framework from my **Master's thesis** (fNIRS) to EEG, showing the **cross-modality potential** of temporal GNNs for neurodegenerative disease classification.

---
### 🧩 ABIDE fMRI Graph Analysis
Generated temporal graphs from resting-state fMRI data (ABIDE-I) using a sliding window and **causality-based graph construction**, then classified autism vs. controls with graph neural networks.  
Used **Captum** Saliency maps (SmoothGrad: saliency with noise averaging) to identify key nodes and features driving the classification.

---
### 🫁 Calibrated Ensemble for Lung CT Classification
Built a calibrated, architecture-diverse ensemble (**Xception, DenseNet121, ResNet50V2**) for four-class lung CT classification: adenocarcinoma, large cell carcinoma, squamous cell carcinoma, and normal.

- Trained with augmentation, random oversampling, and focal loss; combined validation-selected models in a **weighted ensemble**.  
- Applied **temperature scaling** (ECE 0.084 → 0.062) and class-specific decision scaling, all tuned on validation data only.  
- Used **predictive entropy** for uncertainty-based referral: entropy was higher for errors (p<0.001), and deferring the 10% most uncertain cases raised accuracy from 77.8% to 83.0%.  
- Test results: 77.8% accuracy, 83.5% balanced accuracy, macro AUROC 0.980. Showed that high AUROC can hide uneven subtype performance (adenocarcinoma vs. squamous confusion).

---
### DBT-CLIP: Breast Cancer Classification via Transfer Learning
[🔗 GitHub Repository](https://github.com/phat-hee/DBT-CLIP-Breast-Cancer-Classification-via-Transfer-Learning)

Developed a CLIP-based deep learning pipeline to classify breast cancer screening images into four categories (Benign, Actionable, Cancer, Normal) from Digital Breast Tomosynthesis (DBT) data.

- Used CLIP (ViT-B/32) as a frozen feature extractor to generate 512-dimensional embeddings from mammography images.  
- Applied Albumentations augmentations (flips, rotations, brightness/contrast, shift-scale-rotate) only to minority classes during training-time feature extraction to avoid leakage into validation/test sets.  
- Handled severe imbalance with SMOTETomek (SMOTE oversampling + Tomek links undersampling) applied exclusively to training features.  
- Built a 2-layer MLP classifier (512→256→128→4) with batch normalization and dropout (p=0.5), optimized using Adam (lr=1e-3, weight_decay=1e-5).  
- Used Focal Loss (γ=2.0) combined with Effective Number of Samples (β=0.999) for dynamic class weighting.  
- Trained with cosine annealing over 30 epochs, early stopping, mini-batches (32), and model checkpointing.

This project showed how transfer learning with vision-language models, hybrid resampling, focal loss, and strict leak-prevention can give robust multi-class classification on medical imaging tasks with severe class imbalance.

---

## 📚 Publications
### ✅ Accepted
- **Calibrated Ensemble Deep Learning for Four-Class Lung CT Image Classification and Uncertainty-Based Referral**  
  *M. Fathi\*, M. Gholami\*, N. Alipour, M. Faramarzi, N. Deravi, D. Yarahmadi* (\*equal contribution)  
  [_Digital Health_]  

### 🧠 Under Review
- **Classification of Healthy Controls vs. Alzheimer's and Frontotemporal Dementia Using Temporal Graph Neural Networks: A Resting-State EEG Study**  
  *M. Fathi, M. Faramarzi, M. Gholami, M.M. Pedram*  
  [_Neuroinformatics_]  
  🔗 [GitHub Repository](https://github.com/phat-hee/eeg__temporalgraph_ad_ftd_hc)
- **A Novel Hybrid Method Based on Deep Learning for Alzheimer's Disease Diagnosis**  
  *M. Fathi, M. Faramarzi, M. Gholami, M.M. Pedram*  
  [_Applied Intelligence_]  

---

### ⚙️ Work in Progress
- **Graph Neural Networks with Explainability for Classifying Autism Spectrum Disorder in the ABIDE-I Resting-State fMRI Dataset**  
  *M. Fathi, M. Faramarzi, M. Gholami, M. Pakravan*

---

## 🎓 Teaching & Outreach
- **Teaching Assistant (Machine Learning Course):** Designed assignments, mentored students, and supported coursework at Kharazmi University.  
- **Workshop Speaker:** Led a university seminar on *AI in Neuroscience*, discussing applications in **BCI**, **neuroimaging**, and **cognitive research**.  
- **Research Assistant:** Acquired and preprocessed fNIRS/EEG data, and trained students to operate neuroimaging hardware.
