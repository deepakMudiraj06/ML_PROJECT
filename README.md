 Wildlife Species Classification using Audio (BirdCLEF)

 Project Overview

This project focuses on identifying wildlife (bird species) from audio recordings using Deep Learning. It is inspired by the Kaggle BirdCLEF competition, which aims to automate biodiversity monitoring using acoustic data.

The model converts audio signals into Mel Spectrograms and uses a pretrained EfficientNet model to classify species.

---
  Objectives

* Convert raw audio into spectrograms
* Build a deep learning model for classification
* Improve accuracy using transfer learning
* Handle noisy real-world audio data



  Dataset

* Source: Kaggle BirdCLEF Dataset
* Contains:

  * Audio files (.ogg)
  * Metadata (CSV)
* Used top 20 most frequent classes for better performance

---

  Technologies Used

* Python
* PyTorch
* Librosa
* NumPy, Pandas
* Scikit-learn
* Matplotlib, Seaborn

---

  Project Workflow

 1️⃣ Data Preprocessing

* Loaded audio using Librosa
* Split audio into 5-second segments
* Handled silent/noisy segments
* Encoded labels

 2️⃣ Feature Extraction

* Converted audio into **Mel Spectrograms**
* Normalized spectrogram values
* Resized input to 224×224

 3️⃣ Model Architecture

* Used **EfficientNet-B0 (pretrained)**
* Applied **Transfer Learning**
* Fine-tuned last layers

 4️⃣ Training Strategy

* Multi-segment learning (3 segments per audio)
* Class balancing using weights
* Optimizer: Adam
* Loss: CrossEntropyLoss
* Epochs: 5

---

  Results

*  Accuracy: ~70% – 85%
*  Training loss decreased steadily
*  Classification report generated

---

  Visualizations

* Audio Waveform
* Mel Spectrogram
* Training Loss Curve
* Confusion Matrix

---

 Challenges Faced

* Class imbalance
* Noisy environmental audio
* Variable audio lengths
* Multiple species in one recording

---

 Improvements Made

* Used pretrained EfficientNet
* Implemented multi-segment learning
* Applied class weighting
* Optimized preprocessing pipeline

---

 Applications

* Wildlife conservation
* Biodiversity monitoring
* Environmental research
* Smart ecological systems

---

 Future Work

* Multi-label classification (real BirdCLEF scenario)
* Real-time audio detection
* Web/Mobile deployment
* Larger dataset training

---

 Project Structure

```
├── data/
│   ├── train_audio/
│   ├── train.csv
│
├── notebooks/
│   └── model.ipynb
│
├── models/
│   └── efficientnet_model.pth
│
├── README.md
```

---

 How to Run

```bash
# Clone repository
git clone https://github.com/your-username/your-repo-name.git

# Install dependencies
pip install -r requirements.txt

# Run the notebook / script
```

---

 Acknowledgements

* Kaggle BirdCLEF Competition
* Librosa Documentation
* PyTorch Community

---

 Conclusion

This project demonstrates how deep learning can be applied to real-world environmental challenges. By leveraging audio data and transfer learning, we can build efficient models for wildlife monitoring.

---

 Contact

For any queries or collaboration:

* Name: ATTEM DEEPAK MUDIRAJ
* Email: attemdeepakmudiraj@gmail.com
