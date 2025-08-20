# PawNet-U 🐾 Pet Image Segmentation with U-Net

Pixel-wise segmentation of cats & dogs into **background / pet / border** using a compact U-Net in Keras/TensorFlow on the **Oxford-IIIT Pet** dataset.

---

## 🔹 Project Overview
- Implemented a **U-Net architecture** for semantic segmentation  
- Used **Oxford-IIIT Pet dataset** with trimaps (3 classes: background, pet, border)  
- Built a custom data pipeline using `tf.keras.utils.Sequence`  
- Trained the model and evaluated results on unseen images  

---

## 🔹 Notebook Contents
1. **Dataset setup** — download & align images with trimap masks  
2. **Quick visualization** — sample image + mask  
3. **Data loader** — custom Sequence generator  
4. **U-Net** — encoder–decoder with skip connections  
5. **Training & metrics** — loss/accuracy, parameter count  
6. **Qualitative results** — predictions vs. ground truth  
7. **Notes & limitations** — strengths, struggles, improvements  

---

## 🔹 Results
Example prediction (left = input, middle = ground truth, right = U-Net prediction):

- Performs well on clean backgrounds & large pets  
- Struggles on fine details (fur edges, whiskers, cluttered scenes)  

---

## 🔹 What I Learned
- How to build efficient data pipelines with Keras `Sequence`  
- How U-Net combines global context and local details  
- Why loss functions like Dice/IoU are useful in segmentation  

---

## 🔹 How to Run
```bash
git clone https://github.com/asherbunny/PawNet-U.git
cd PawNet-U
pip install -r requirements.txt
