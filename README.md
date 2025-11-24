# Image-Tempering-Localization-using-Residual-U-Net
 Overview of the Project

This project focuses on detecting and localizing tampered regions in digital images using a Residual U-Net segmentation model.
The goal is to identify manipulated areas such as splicing, copy-move, or object insertion with pixel-level accuracy.

The model is trained on the Realistic Tampering Dataset, containing pristine images, tampered images, and ground-truth masks.


---

 Features

🔍 Pixel-level tampering localization

🧠 Residual U-Net architecture for deeper feature extraction

📊 Dice + BCE loss for accurate segmentation

🔄 Data augmentation (flips, resizing)

🖥 GPU-accelerated training support

📈 Evaluation metrics – IoU & Dice Score

💾 Saves best, latest, and final trained model weights

📂 Modular dataset loader for real-world tampering datasets



---

🛠 Technologies / Tools Used

Python 3.10+

PyTorch

Torchvision

NumPy

Pillow (PIL)

TQDM

Matplotlib (optional for visualization)

Realistic-Tampering-Dataset (Canon, Nikon, Sony models)



---

🚀 Steps to Install & Run the Project

1️⃣ Clone or Download the Repository

git clone <your-repo-link>
cd tamper-localization

2️⃣ Install Dependencies

Create an environment and install required libraries:

pip install torch torchvision pillow numpy tqdm

(Optional GPU version)

pip install torch --index-url https://download.pytorch.org/whl/cu121

3️⃣ Download the Dataset

Place your dataset in this structure:

data-images/
   Nikon_D90/
      pristine/
      tampered-realistic/
      ground-truth/
   Canon_60D/
   Nikon_D7000/
   Sony_A57/

4️⃣ Run Training Script

python train.py

This will:

Train for 30 epochs

Save: best_resunet.pth, last_resunet.pth, final_resunet.pth


5️⃣ Inference on Test Image

python inference.py --img path/to/image.jpg --model final_resunet.pth


---

🧪 Instructions for Testing

1. After training, load the trained model:



model.load_state_dict(torch.load("best_resunet.pth"))

2. Pass your image through the preprocessing pipeline (resize → tensor → normalize)


3. Run:



pred = model(image_tensor.unsqueeze(0))

4. Apply threshold 0.5:



mask = (torch.sigmoid(pred) > 0.5).float()

5. Visualize the mask overlay.
6.
