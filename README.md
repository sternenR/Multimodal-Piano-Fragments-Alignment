# 🎹 Multimodal-Piano-Fragments-Alignment
This code was developed as part of my undergraduate thesis at Beijing University of Chemical Technology, titled "**THE CONSISTENCY OF EMBEDDING SPACE FOR MULTIMODAL MUSIC FEATURES**".

## 🎯 Overview
This project implemented a deep learning model based on contrastive learning to achieve the consistency of features shared between MIDI and audio data, thereby accomplishing cross-modal alignment.  

## 📂 Dataset
The dataset was processed based on **[MAESTRO v2.0.0](https://magenta.tensorflow.org/datasets/maestro)** before training.
The generated dataset used for training is totaling approximately 50GB in size, which includes:
- Training: 184,514 sample pairs
- Validation: 21,649 sample pairs
- Test: 23,611 sample pairs

## 🏗️ Model Architecture
Inspired by CLIP, the model uses
- **Encoders:** two ResNet-18 to extract features from Piano-Roll and Spectrogram modalities, initialized with pre-trained weights for efficient learning.
- **Projection:** built with a Multi-Layer Perceptron (MLP), projects the features into a shared embedding space, reducing dimensionality and enhancing discriminative power for contrastive learning. 

## 📜 Results
The entire training process took approximately 8 hours.  
The final model achieved an accuracy of 99.00% on the validation set and 98.92% on the test set.

## 🔧 Experimental Setup
The experiments were conducted on a system running Ubuntu 20.04, with the following configuration:

- PyTorch 1.11.0 (with Python 3.8)
- CUDA 11.3 for GPU acceleration
- GPU: NVIDIA RTX 3090 with 24GB VRAM

## 📌 License
This project is licensed under the Apache 2.0 License - see the [LICENSE](./LICENSE) file for details.

## 🔗 Citation
If you use this work in your research, please cite:
```
@misc{MultimodalPianoAlignment,
  author = {Ruijin Wang},
  title = {Multimodal Piano Fragments Alignment},
  year = {2024},
  url = {https://github.com/sternenR/Multimodal-Piano-Fragments-Alignment}
}
```
