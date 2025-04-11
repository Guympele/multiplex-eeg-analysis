# Multiplex Network-Based EEG Functional Connectivity Analysis During Motor Execution

## 🧠 Project Summary
This project aims to analyze and reveal the brain's functional connectivity during motor movement by modeling EEG signals as multiplex networks. Using spectral analysis (STFT) and complex network theory, the study identifies the most active frequency bands and detects communities in brain regions responsible for movement execution.

## 📁 Dataset
- **Source**: EEG data from 109 healthy volunteers
- **Sampling rate**: 160 Hz
- **Channels**: 64 electrodes (10–20 system)
- **Experimental Task**: Visual motor task involving hand movement with resting intervals

## 🧪 Methodology
### 1. **Preprocessing**
- Filtering EEG data (0.5–40 Hz)
- Epoch extraction around movement stimulus

### 2. **Spectral Decomposition**
- Short-Time Fourier Transform (STFT)
- Extraction of power in 5 standard EEG frequency bands:
  - Delta (0.5–4 Hz)
  - Theta (4–8 Hz)
  - Alpha (8–13 Hz)
  - Beta (13–30 Hz)
  - Gamma (30–40 Hz)

### 3. **Network Construction**
- Create a graph for each frequency band
- Use Pearson correlation between EEG channels as edge weights
- Combine all 5 graphs into a single **multiplex network**

### 4. **Analysis**
- Compute centrality metrics (PageRank, Betweenness, etc.)
- Detect communities using Louvain algorithm
- Identify dominant brain areas and bands related to motor execution

## 💻 Technologies Used
- Python 3.10+
- NumPy, SciPy, MNE, NetworkX, Matplotlib, Seaborn
- Jupyter Notebook

## 📊 Results (Summary)
- **Delta** and **Theta** bands showed strongest inter-regional connectivity during movement
- Central and parietal regions exhibited high centrality values
- Multiplex structure improved interpretability compared to single-layer networks

## 🚀 How to Use
1. Clone the repo:
   ```bash
   git clone https://github.com/your-username/multiplex-eeg-analysis.git
   cd multiplex-eeg-analysis
   ```

2. Set up the environment:
   ```bash
   pip install -r requirements.txt
   ```

3. Run notebooks in order:
   - `01_preprocessing_eeg.ipynb`
   - `02_stft_analysis.ipynb`
   - `03_multiplex_network.ipynb`
   - `04_community_detection.ipynb`

4. Check `/results/` folder for plots and exports

## 📌 Folder Structure
```
multiplex-eeg-analysis/
├── data/                 # Raw and processed EEG data
├── notebooks/            # Step-by-step Jupyter notebooks
├── src/                  # Python scripts for modular processing
├── results/              # Outputs, plots, and figures
├── requirements.txt      # Python dependencies
└── README.md             # This file
```

## 🔍 Future Work & PhD Ideas
- Real-time BCI systems using multiplex graph dynamics
- Predictive models for early detection of motor disorders
- Personalization of neurofeedback based on EEG network profiles
- Application in neuro-rehabilitation and exoskeleton control

## 📄 License
This work is shared under the MIT License.

---
> Research originally conducted by **Guy Rostand Mpele Singoa** at AIMS Cameroon (2021–2022).
