# 🚀 **Generative Modelling with GANs: From Synthetic Distributions to Real-World and Creative Applications**

### 🧠 Adversarial Learning Across Modalities | Images • Tabular • Synthetic Data | PyTorch

<p align="center">
  <img src="https://img.shields.io/badge/Deep%20Learning-GANs-e53935?style=for-the-badge&logo=pytorch">
  <img src="https://img.shields.io/badge/Domains-Multimodal-1e88e5?style=for-the-badge">
  <img src="https://img.shields.io/badge/Data-Toy%20%7C%20Medical%20%7C%20Tabular%20%7C%20Sketch-43a047?style=for-the-badge">
  <img src="https://img.shields.io/badge/Evaluation-FID%20%7C%20PCA%20%7C%20Stats-ff6f00?style=for-the-badge">
</p>

---

## 📌 **Project Overview**

This project delivers a **systematic, multi-domain evaluation of Generative Adversarial Networks (GANs)** to understand how well they learn real-world data distributions under increasing complexity.

Unlike typical GAN demos, this work focuses on:

* 📊 **Real-world data challenges (tabular + medical)**
* 🧠 **Model limitations (mode collapse, instability)**
* 📉 **Evaluation beyond accuracy (FID, PCA, distributions)**

> 💡 The goal is not just to generate data — but to **critically assess when GANs actually work and when they fail.**

---

## 🎯 **Core Objectives**

* Evaluate GAN performance across **different data modalities**
* Analyse **distribution learning vs structural learning**
* Identify **failure points in real-world datasets**
* Provide **practical insights for model selection**

---

## 🧠 **Experimental Design**

| Part         | Domain          | Dataset      | Focus                 |
| ------------ | --------------- | ------------ | --------------------- |
| **Part 1**   | Toy Data        | Sine, Spiral | Learning behaviour    |
| **Part 2.1** | Medical Imaging | BloodMNIST   | Realism + stability   |
| **Part 2.2** | Tabular Data    | CICIDS 2017  | Distribution learning |
| **Part 2.3** | Creative AI     | QuickDraw    | Visual structure      |

---

## ⚙️ **Models & Approach**

### 🔹 GAN Architecture

* **Generator:** Noise → Synthetic data
* **Discriminator:** Real vs Fake classification
* **Training:** Adversarial minimax optimisation

---

### 🔹 Architecture Selection (Key Design Decision)

| Data Type      | Model   | Reason               |
| -------------- | ------- | -------------------- |
| Toy Data       | MLP     | Low-dimensional      |
| Medical Images | DCGAN   | Spatial learning     |
| Tabular Data   | MLP GAN | No spatial structure |
| Sketch Images  | DCGAN   | Pattern recognition  |

👉 This demonstrates **model–data alignment**, a key real-world ML skill.

---

## 📊 **Evaluation Strategy**

| Data Type | Method                               |
| --------- | ------------------------------------ |
| Toy Data  | Visual + Statistical comparison      |
| Images    | **Fréchet Inception Distance (FID)** |
| Tabular   | PCA + Distribution analysis          |

---

# 📈 **Key Results & Insights**

## 🔹 **1. Toy Data — Learning vs Structure**

### ✅ Sine Wave

* Near-perfect learning of distribution
* Captures both **function + noise**

### ⚠️ Spiral Dataset

* Baseline GAN → good statistics, poor structure
* Modified GAN → improved geometry

👉 **Insight:**

> GANs can match distributions **without learning true structure**

---

## 🧬 **2. Medical Imaging — BloodMNIST**

* 📦 Dataset: **11,959 images (8 classes)**
* 📉 FID: **~210.65 (high → poor alignment)**

### Observations:

✔ Learns:

* colour distribution
* basic cell shapes

❌ Fails:

* fine texture
* biological realism

👉 **Insight:**

> GAN struggles with **high-frequency, high-detail data**

---

## 🌐 **3. Tabular Data — CICIDS (Critical Insight)**

* 📦 **~691K samples | 68 features**
* Highly complex: **multi-modal, heavy-tailed, correlated**

### 🚨 Key Failure

| Feature       | Real      | Generated |
| ------------- | --------- | --------- |
| Flow Duration | 2.8 × 10⁷ | 7.1 × 10⁶ |

➡️ ~**75% underestimation**

### Issues:

* Variance collapse
* Missing extreme values
* Distribution compression

### PCA:

* Real → wide spread
* Generated → compressed

👉 **Insight (VERY IMPORTANT):**

> Standard GANs **fail on tabular data** — a critical real-world limitation

---

## 🍕 **4. QuickDraw — Best Case Scenario**

* 📦 **130,371 images (28×28)**
* 📉 FID: **41.75 (strong performance)**

### 🔥 Improvement:

> ~**80% better than medical images**

### Learns:

✔ shape structure
✔ segmentation patterns

👉 **Insight:**

> GAN performs best when **data is simple, structured, and consistent**

---

# 🧩 **Core Takeaways (Recruiter Gold)**

### 🔹 1. Data Complexity Drives Model Performance

* Simple → excellent
* Images → moderate
* Tabular → poor

---

### 🔹 2. GAN Limitations in Practice

* ⚠️ Mode collapse → low diversity
* ⚠️ Instability → training imbalance
* ⚠️ Poor tail learning → misses rare events

---

### 🔹 3. Evaluation Matters More Than Model

* Statistics alone → misleading
* Visual inspection → essential
* FID → useful but incomplete

---

# 🏁 **Final Conclusion**

GAN performance is **highly dependent on data structure and complexity**.

* ✅ Strong on simple distributions
* ⚠️ Moderate on images
* ❌ Weak on tabular data

> 💡 *The key lesson: choosing the right model for the data is more important than the model itself.*

---

# 🔮 **Future Improvements**

* Conditional GANs → controlled generation
* WGAN-GP → improved stability
* CTGAN → tabular data modelling
* StyleGAN → high-resolution images
* Hybrid GAN + Diffusion → next-gen models

---

# 🧰 **Tech Stack**

* Python
* PyTorch
* NumPy / Pandas
* Matplotlib / Seaborn
* GPU Acceleration

---

# 📁 **Project Structure**

```bash
Generative-Modelling-Case-Study/
│
├── Notebook/
├── Data/
├── Outputs/
│   ├── Part1_outputs/
│   ├── Part2_outputs/
│       ├── bloodmnist/
│       ├── cicids/
│       └── quickdraw_pizza/
│
└── README.md
```

---

# 💼 **Why This Project Stands Out**

✔ Demonstrates **real-world data challenges (not toy-only)**
✔ Shows **deep understanding of model limitations**
✔ Uses **appropriate evaluation methods (advanced level)**
✔ Covers **multiple domains (CV + tabular + generative AI)**
✔ Reflects **research-level thinking + practical insight**

---

# 🎯 **What This Proves About Me**

* I don’t just build models — I **analyse when they fail**
* I understand **data → model → evaluation alignment**
* I can work with **complex, real-world datasets**
* I think like a **Data Scientist, not just an ML engineer**
