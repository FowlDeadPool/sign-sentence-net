# sign-sentence-net
# ASL Sentence Recognition using Pose Landmarks

This project implements an end-to-end American Sign Language (ASL) sentence recognition model using pose-based video input. It was originally developed for the [Google ASL Fingerspelling Kaggle competition](https://www.kaggle.com/competitions/asl-fingerspelling/overview).

The system takes video sequences of sign language and converts them into corresponding letter sequences using a hybrid Transformer-LSTM architecture.

---

## 🧠 Model Architecture

- **Encoder**: Modified Transformer-based encoder inspired by **SqueezeFormer**, processes sequences of pose landmarks extracted via MediaPipe.
- **Decoder**: A **2-layer LSTM** followed by a linear classifier for sequence prediction.
- **Input**: Preprocessed pose keypoints (hands, face, body) for each video frame.
- **Output**: Predicted sequence of characters (letters in ASL fingerspelling).

---

## 📁 Dataset

- Google ASL Fingerspelling Dataset  
- [Kaggle competition link](https://www.kaggle.com/competitions/asl-fingerspelling/data)  
- Contains annotated videos with finger-spelled English words by various signers.

---

## ⚙️ Pipeline Overview

1. **Data Extraction**  
   - Extract pose landmarks using MediaPipe (hands, pose, face).

2. **Preprocessing**  
   - Preprocessed ASL video data by extracting, resizing, normalizing, and padding 30 frames per video for consistent input shape.

3. **Model Training**  
   - Encoder: Modified SqueezeFormer blocks.  
   - Decoder: LSTM-based autoregressive decoder.

4. **Evaluation**  
   - Uses sequence-level accuracy, Levenshtein distance.

---

## 📊 Results

- Competitive performance with lightweight architecture.
- Achieved high validation accuracy on signer-independent split.

---



