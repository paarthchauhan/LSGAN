# LS-GAN (Least Squares Generative Adversarial Network)

This repository contains a PyTorch implementation of the **Least Squares GAN (LS-GAN)**, which is a variant of the standard GAN that replaces the binary cross-entropy loss with least squares loss to stabilize training and generate higher quality images.

---

## 📌 About LS-GAN

LS-GAN was proposed to address the vanishing gradients and instability issues commonly seen in traditional GANs. It uses **least squares loss** for the discriminator and generator instead of the standard binary classification loss.

This leads to:

- **Smoother gradients**
- **More stable training**
- **Higher quality generated images**

**Paper:** [LS-GAN: Least Squares Generative Adversarial Networks](https://arxiv.org/abs/1611.04076)

---

## 🧠 Model Architecture

- **Generator:** A neural network that maps a random noise vector (latent space) to a synthetic image.
- **Discriminator:** A neural network that distinguishes between real images from the dataset and fake images from the generator.

Both models are implemented using simple `nn.Sequential` blocks in PyTorch for clarity and modularity.

---

## 🚀 How to Run

1. **Clone this repo:**

   ```bash
   git clone https://github.com/khushiarora0208/LSGAN.git
   cd LSGAN
   ```

2. **Install Dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

3. **Train the model:**

   ```bash
   python train.py
   ```

   - Default training uses the **MNIST** dataset.
   - Generated images will be saved to the `generated_images/` directory.

---

## 🖼️ Sample Outputs

Generated images during training are saved every 10 epochs. You can visualize how the model improves over time in the `generated_images/` folder.
![image](https://github.com/user-attachments/assets/b7787e5c-1b8a-4d54-9bbc-dee8c2ae9891)

---

## 📁 Project Structure

```
LS_GAN/
│
├── datasets/               # Dataset loading and preprocessing
├── models/                 # Generator and Discriminator models
│   ├── discriminator.py
│   └── generator.py
│
├── utils/                  # Helper functions
│   └── utils.py
│
├── generated_images/       # Output directory for generated samples
├── train.py                # Training script
├── requirements.txt
└── README.md
```

---

## 📚 Requirements

- Python 3.8+
- PyTorch
- torchvision
- numpy
- matplotlib

Install all dependencies with:

```bash
pip install -r requirements.txt
```

---

## 🤝 Contributing

Pull requests are welcome! If you find a bug or want to add features (e.g. different dataset support, model enhancements), feel free to open an issue or PR.

---


```

---
