 # MNIST Handwritten Digit Classifier

A simple Deep Learning project that trains a Neural Network on the MNIST dataset and uses it to predict custom handwritten digits from images.

## Features
* **Dataset:** Uses the classic MNIST database of handwritten digits (60,000 training images, 10,000 test images).
* **Model:** Built with TensorFlow/Keras using a Sequential Feedforward Neural Network.
* **Custom Inference:** Includes an image preprocessing pipeline to test your own handwritten digit images (`.png`).

## Requirements
Ensure you have Python installed, then install the required dependencies:
```bash
pip install tensorflow matplotlib pillow numpy
```

## Project Structure
* `main.py` - The main Python script containing model training and inference.
* `digit.png` - A custom handwritten digit image (28x28 pixels, black background, white text preferred) used for custom predictions.

## How to Run

1. **Clone the Repository:**
   ```bash
   git clone <your-repository-url>
   cd <your-repository-folder>
   ```

2. **Prepare a Custom Image:**
   Place a handwritten digit image named `digit.png` in the root directory. 

3. **Execute the Script:**
   ```bash
   python main.py
   ```

## Code Walkthrough
* **SSL Fix:** Includes an SSL workaround to bypass certificate verification issues when downloading the MNIST dataset.
* **Normalization:** Scales pixel values from `[0, 255]` to `[0.0, 1.0]` for optimal model training.
* **Architecture:** 
  * Flatten Layer (converts $28 \times 28$ grid into a 784-element vector)
  * Dense Layer (128 units, ReLU activation)
  * Output Layer (10 units, Softmax activation for classification)
* **Preprocessing Pipeline:** Converts custom input images to grayscale, inverts the colors to match MNIST formatting, resizes them to $28 \times 28$ pixels, and normalizes them.
