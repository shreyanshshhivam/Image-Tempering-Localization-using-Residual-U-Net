# Image-Tempering-Localization-using-Residual-U-Net
----------------------------------
 NOTE: THIS GITHUB REPOSITORY DOES NOT CONTAIN THE DATASET ON WHICH THIS MODEL IS TRAINED DUE TO LIMITED SPACE OBLIGATION OF GITHUB. 
 -----APOLOGIES FOR THE SAME----
  
 
 
 Overview of the Project

This project focuses on detecting and localizing tampered regions in digital images using a Residual U-Net segmentation model.
The goal is to identify manipulated areas such as splicing, copy-move, or object insertion with pixel-level accuracy.

The model is trained on the Realistic Tampering Dataset, containing pristine images, tampered images, and ground-truth masks.


---

 Features

 Pixel-level tampering localization

Residual U-Net architecture for deeper feature extraction

Dice + BCE loss for accurate segmentation

 Data augmentation (flips, resizing)

 GPU-accelerated training support

 Evaluation metrics – IoU & Dice Score

 Saves best, latest, and final trained model weights

 Modular dataset loader for real-world tampering datasets



---

 Technologies / Tools Used

Python 3.10+

PyTorch

Torchvision

NumPy

Pillow (PIL)

TQDM

Matplotlib (optional for visualization)

Realistic-Tampering-Dataset (Canon, Nikon, Sony models)


