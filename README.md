# Lipreading-Project- GRU Model for Video-Based Speech Recognition 

Overview
This project explores lipreading using deep learning, specifically focusing on predicting sentences from silent video footage of speakers. Unlike traditional approaches that focus on individual word classification, this work aims to capture temporal and contextual patterns across sequences of frames to decode entire sentences.

I contributed to this project by developing and refining GRU models trained on the GRID corpus. The work builds on existing research and enhances sentence-level accuracy using temporal feature extraction.

Project Contents
Due to GPU constraints on free-tier Google Colab, training was split across multiple notebook versions and run on different accounts.

master/sandbox_GRU_8.ipynb: Final notebook with trained model and results, including sample predictions. Achieved a minimum validation loss of 3.42.

notebooks/: Contains earlier training notebooks (gru_model_v1.ipynb to gru_model_7.ipynb) showing the model development process, preprocessing steps, and intermediate tuning efforts.

Dataset
GRID Corpus

Over 28 hours of audiovisual recordings

Structured six-word sentences spoken by multiple speakers

Dataset includes aligned video frames and sentence labels

The dataset was preprocessed into image sequences and sentence-level labels for supervised learning. Only the visual modality (video) was used in training.

Tools & Frameworks
Python 3.9+

TensorFlow / Keras

OpenCV for video frame extraction

Google Colab (multiple accounts used to work around GPU time limits)


Model Summary – GRU
The model architecture includes:

TimeDistributed CNN layers for extracting spatial features from individual frames

Dense + Softmax layer for classifying entire sentences

The final GRU model reached a validation loss of 3.42, and the sandbox_GRU_8.ipynb notebook includes examples of predictions.


Acknowledgments
Thanks to the team for Bi-LSTM work and shared resources. Special thanks to Google Colab for enabling GPU-based training throughout this project.
