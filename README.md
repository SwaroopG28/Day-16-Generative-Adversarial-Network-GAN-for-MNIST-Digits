# Handwritten Digit Generation with GANs

## **Overview**
This project demonstrates how to use a **Generative Adversarial Network (GAN)** to generate realistic handwritten digits similar to the ones in the **MNIST dataset**. The GAN consists of two networks:
- **Generator**: Creates fake handwritten digits.
- **Discriminator**: Determines whether an image is real or fake.

By training these networks together, the GAN learns to generate convincing handwritten digits.

---

## **Dataset**
### MNIST Dataset
- Contains 60,000 grayscale images of handwritten digits (0-9).
- Each image is 28x28 pixels.
- The dataset is widely used in machine learning and computer vision tasks.

---

## **How GANs Work**
1. **Generator**:
   - Takes a random noise vector as input.
   - Outputs a 28x28 pixel image.
   - Learns to create realistic images that resemble real handwritten digits.

2. **Discriminator**:
   - Takes an image as input (either real from the dataset or fake from the generator).
   - Outputs a probability (`1` for real, `0` for fake).
   - Learns to distinguish between real and fake images.

3. **Training Process**:
   - The generator and discriminator compete against each other:
     - The **generator** tries to create images that fool the discriminator.
     - The **discriminator** tries to correctly classify images as real or fake.
   - Over time, the generator becomes better at creating realistic images.

---

## **Project Workflow**
1. **Data Preparation**:
   - Loaded the MNIST dataset.
   - Normalized pixel values to the range `[-1, 1]` for better generator performance.

2. **Model Architecture**:
   - **Generator**:
     - A fully connected network that reshapes noise vectors into 28x28 images.
   - **Discriminator**:
     - A fully connected network that classifies images as real or fake.

3. **Training**:
   - Trained the GAN for 5000 epochs.
   - Saved generated images at regular intervals to visualize the progress.

4. **Results**:
   - The generator produces realistic handwritten digits after training.

---

## **Generated Results**
### Example Output
- At the beginning of training: Images look like random noise.
- After a few thousand epochs: Images start resembling digits.
- At the end of training: Images are nearly indistinguishable from real MNIST digits.
