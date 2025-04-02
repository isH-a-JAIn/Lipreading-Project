# Lipreading-Project- GRU Model for Video-Based Speech Recognition 

# Lipreading with GRU – Video-Based Sentence Prediction  
*August 2024 – Present*

## **Overview**  
This project explores **lipreading using deep learning**, specifically focusing on *predicting full sentences* from silent video footage of speakers. Unlike traditional approaches that focus on individual word classification, this work captures *temporal and contextual patterns* across sequences of frames to decode entire sentences.

I contributed to this project by developing and refining **GRU models** trained on the **GRID corpus**, building on prior work to enhance sentence-level prediction through temporal feature extraction.

---

## **Project Contents**  
Due to GPU constraints on free-tier Google Colab, training was split across multiple notebook versions and run on different accounts.

- **`master/sandbox_GRU_8.ipynb`**  
  Final notebook containing the trained GRU model, evaluation results, and a few sample predictions.  
  *Achieved minimum validation loss of 3.42.*

- **`notebooks/`**  
  Earlier training notebooks (`gru_model_v1.ipynb` to `gru_model_7.ipynb`) showing:
  - Model development progression  
  - Preprocessing steps  
  - Intermediate experiments and tuning efforts  

---

## **Dataset – GRID Corpus**  
- Over *28 hours* of audiovisual recordings  
- Structured *six-word sentences* spoken by multiple speakers  
- Includes aligned video frames and sentence labels  

The dataset was preprocessed into image sequences and sentence-level labels for supervised learning.  
*Only the visual modality (video) was used for training.*

---

## **Tools & Frameworks**  
- **Python 3.9+**  
- **TensorFlow / Keras**  
- **OpenCV** – for video frame extraction  
- **Google Colab** – used for GPU training (across multiple accounts to bypass time limits)  

---

## **Model Summary – GRU**  
The GRU model architecture consists of:

- `TimeDistributed` **CNN layers** to extract spatial features from each frame  
- **Bidirectional GRU layers** to capture sequential and contextual relationships  
- **Dense + Softmax layer** for final sentence classification  

The final model achieved a **validation loss of 3.42**.  
Refer to the `sandbox_GRU_8.ipynb` notebook for sample predictions and evaluation details.

---

## **Acknowledgments**  
Grateful to the team for the Bi-LSTM implementation and shared code resources.  
Special thanks to **Google Colab** for enabling GPU-based training throughout the project.
