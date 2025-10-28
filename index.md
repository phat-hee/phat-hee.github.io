# Welcome 
I'm **Mohammad Fathi**, a **Master's graduate in Data Mining** from **Kharazmi University** (GPA: 3.74/4.0).  
My research interests are **Artificial Intelligence, Data Mining, and Computational Neuroscience**, with a focus on **neuroimaging analysis**, **biomedical signal processing**, and **BCI**.

I completed my master's degree **ranked 2nd** in my program, conducting my thesis research at the **Kharazmi Cognitive and Brain Science Lab** under the supervision of **Dr. Mir Mohsen Pedram**. I developed a **temporal graph neural network (TGNN)** framework to classify **Mild Cognitive Impairment (MCI)** and **healthy controls (HC)** using **fNIRS** resting-state data, earning a perfect thesis grade of **20/20**.

## 🔬 Projects

### 🧠 fNIRS-based MCI Classification
Designed and implemented a **temporal graph neural network (GConvGRU)** to classify **Mild Cognitive Impairment (MCI)** and **Healthy Controls (HC)** from resting-state fNIRS data.  
[🔗 GitHub Repository](https://github.com/phat-hee/mci_fnirs_tgnn)  
I performed **all preprocessing and modeling steps** except for data acquisition.  
- Applied a **15-second sliding window** to segment preprocessed fNIRS signals.  
- Constructed temporal graphs representing functional connectivity dynamics.  
- Implemented and trained the **TGNN** architecture using PyTorch Geometric.  
- Evaluated model interpretability using graph-based feature importance analysis.  
This project formed the core of my **Master’s thesis**, earning a perfect grade (20/20).

---
### ⚡ EEG Temporal Graph Neural Network for AD and FTD  
[🔗 GitHub Repository](https://github.com/phat-hee/eeg__temporalgraph_ad_ftd_hc)

Developed and implemented a **temporal graph neural network (TGNN)** framework to classify **Alzheimer’s Disease (AD)**, **Frontotemporal Dementia (FTD)**, and **Healthy Controls (HC)** from resting-state EEG data.  
I was responsible for **all stages of the technical development**, including data handling, model design, and full code implementation, while collaborating with a **team of researchers** who focused on report writing and documentation.  

- Processed pre-cleaned EEG data and generated **temporal functional connectivity graphs** using **Granger causality** for interpretability.  
- Designed, coded, and optimized the entire **PyTorch-based pipeline**, including **graph generation**, **feature extraction**, **model architecture**, and **training procedure**.  
- Experimented with multiple GNN architectures and finalized a **GraphSAGE + LSTM** hybrid model with **attention-based fusion** across **alpha** and **beta** frequency bands.  
- Performed both **whole-brain** and **lobe-level** analyses to identify which regions were most relevant for each impairment type.  
- Demonstrated that **attention mechanisms** improved interpretability by highlighting the contribution of frequency bands and brain regions.  

This project extended the framework I developed in my **Master’s thesis** (based on fNIRS data) to EEG, showing the **cross-modality potential** of temporal graph neural networks for neurodegenerative disease classification.


---

### 🧩 ABIDE fMRI Graph Analysis
Automated **temporal graph generation** and **sliding-window functional connectivity modeling** using graph neural networks with explainability.  
We employed **causality-based graph construction** to build dynamic brain graphs from resting-state fMRI data and used **Captum** to identify key nodes and features contributing to classification performance.  

---

## 📚 Publications
### 🧠 Under Review
- **A Novel Hybrid Method Based on Deep Learning for Alzheimer's Disease Diagnosis**  
  *M. Fathi, M. Faramarzi, M. Gholami, M.M. Pedram*  
  [_Applied Intelligence_]  
- **Predicting Cognitive Impairment and Dementia in the Health and Retirement Study of America: A Machine and Deep Learning Approach**  
  *N. Alipour, M. Faramarzi, M. Gholami, M. Fathi, N. Deravi*  
  [_Acta Neurologica Belgica_]

---

### ⚙️ Work in Progress
- **Classification of Healthy Controls vs. Alzheimer's and Frontotemporal Dementia Using Temporal Graph Neural Networks: A Resting-State EEG Study**  
  *M. Fathi, M. Faramarzi, M. Gholami, M.M. Pedram*
   🔗 [GitHub Repository](https://github.com/phat-hee/eeg__temporalgraph_ad_ftd_hc)
- **Graph Neural Networks with Explainability for Classifying Autism Spectrum Disorder in the ABIDE-I Resting-State fMRI Dataset**  
  *M. Fathi, M. Faramarzi, M. Gholami, M. Pakravan*

---

## 🎓 Teaching & Outreach
- **Teaching Assistant (Machine Learning Course):** Designed assignments, mentored students, and supported coursework at Kharazmi University.  
- **Workshop Speaker:** Led a university seminar on *AI in Neuroscience*, discussing applications in **BCI**, **neuroimaging**, and **cognitive research**.  
- **Research Assistant:** Acquired and preprocessed fNIRS/EEG data, and trained students to operate neuroimaging hardware.
