# 🧾 Paper Defect Detection & Classification

> *"Quality control is only as strong as its weakest inspection point — let’s make it smarter."*

This project automates **defect localization in paper manufacturing** by combining **classical feature extraction** with **modern machine learning models**. It demonstrates how techniques like **HOG, Gabor filters, Canny edge detection, and Wavelet transforms**, when paired with models like **SVMs, Logistic Regression, and CNNs**, can transform defect detection in industrial pipelines.

🔗 **Pre-trained Models**: [Hugging Face Repository](https://huggingface.co/AbdullahImran/Paper-Defect-Detection)
📝 **Articles**:

* [Defect Detection in Papers & Model Comparison](https://medium.com/@abdullahimranarshad/defect-detection-in-papers-model-comparison-a0a44a4bafa6)
* [Feature Extraction & Data Preprocessing in Computer Vision](https://medium.com/@abdullahimranarshad/feature-extraction-and-data-preprocessing-in-computer-vision-53066a812a96)

---

## ⚙️ Workflow Summary

The complete pipeline is available in the **master branch** along with the report.
Here’s how the workflow was structured:

### 🔍 Data Exploration

* ✅ **Image Loading & Verification**
* 📊 **Class Distribution** analysis (balanced dataset ensured)
* 🧹 **Preprocessing** for consistent inputs

### 🖼️ Feature Extraction

* 🎨 **Color Histograms & Binning** → minimal impact
* 🧭 **HOG (Histogram of Oriented Gradients)** → highly effective
* 🌌 **Gabor Filters** → captured fine-grained patterns
* ✂️ **Canny Edge Detection** → sharp defect localization
* 🌊 **Wavelet Transform** → insights across resolutions
* ⚪ **Local Binary Patterns** → limited by blur

### 📉 Dimensionality Reduction

* Built a **feature set** from HOG, Gabor, Canny, and Wavelets
* Applied **PCA** → reduced dimensions while retaining **90% variance**

### 🤖 Model Building & Results

* **Logistic Regression** → 99% train | 79% test
* **Naive Bayes (Gaussian)** → comparable to LR after tuning
* **SVM (Support Vector Machines)** → 86% train | 80% test
* **CNNs** → struggled (38% test accuracy, optimization needed)
* **Ensemble (SVM + LR + NB)** → **90% train | 81% test**

📌 Key takeaway → *Classical + ensemble methods outperformed deep CNNs for this dataset.*

### 🖼️ Defect Localization

* Generated **visual heatmaps** of detected defects on sample paper images
* Enhanced interpretability of classification results

---

## 📂 Repository Structure

```
📦 Paper-Defect-Detection
┣ 📜 README.md
┣ 📜 requirements.txt
┣ 📂 notebooks        # EDA, feature extraction, model training
┣ 📂 models           # Trained ML models & Hugging Face links
┣ 📂 data             # Sample datasets
┗ 📂 visualization    # Defect visualization outputs
```

---

## 🧰 Tech Stack

* **Languages & Libraries**: Python (NumPy, Pandas, Scikit-learn, TensorFlow/Keras)
* **Feature Extraction**: OpenCV, skimage (HOG, Gabor, Canny, Wavelets, LBP)
* **Modeling**: Logistic Regression, Naive Bayes, SVM, CNN, Ensemble Learning
* **Visualization**: Matplotlib, Seaborn

---

## ⚠️ Notes & Insights

* 🚫 Only **optimized code sections** included for clarity
* 🛠️ **Redundant/less effective** parts omitted
* 🔮 **Improvement Potential** → CNN architectures & hyperparameter tuning
* 📊 Data visualizations available in full report, trimmed here for brevity

---

## 🎯 Future Work

* 🔧 Improve CNN training with **data augmentation & better architectures**
* 🧠 Integrate **explainable AI** (Grad-CAM, SHAP) for defect interpretability
* 📈 Deploy as an **industrial quality-control dashboard**

---

## 🤝 Contribution

Your insights, feedback, and suggestions for model improvement are welcome!
Feel free to fork, experiment, and share results.

---

🔥 With this pipeline, **industrial paper defect detection becomes faster, more accurate, and more explainable.**

---

Do you want me to also **design a visual architecture diagram** (like feature extraction → PCA → models → results) so it looks even more polished for GitHub?
