# 🎨 Fashion-MNIST Generator (GAN)

A Generative Adversarial Network built in PyTorch that learns to create realistic images of clothing from random noise.

## 🧠 Architecture
* **Generator:** Fully Connected layers mapping a 100-dim latent vector to a 28x28 image. Uses `Tanh` activation.
* **Discriminator:** Binary classifier distinguishing between Real (Dataset) and Fake (Generator) images. Uses `Sigmoid` activation.
* **Loss Function:** Binary Cross Entropy (Minimax Game).

## ⚠️ Challenges Solved
* **Mode Collapse:** Tuned batch size and learning rate to prevent the generator from producing the exact same image repeatedly.
* **Vanishing Gradients:** Implemented `LeakyReLU` (slope 0.2) in the Discriminator to allow weak gradients to flow back to the Generator.

## 🖼 Results
After 20 epochs, the model successfully hallucinates T-shirts, Shoes, and Bags that do not exist in the real world.
