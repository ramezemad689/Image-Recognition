# Image Recognition using MobileNetV2

This project is a simple yet powerful Python script that demonstrates how to use **Deep Learning** for image recognition and classification. It leverages the pre-trained **MobileNetV2** model, trained on the famous **ImageNet** dataset, to detect objects within images with high accuracy.

---

## Features

* **Lightweight & Efficient:** Uses `MobileNetV2`, a highly optimized convolutional neural network designed for speed and efficiency.
* **Automated Image Fetching:** Automatically downloads a sample image (a dog) directly from a remote URL.
* **Image Preprocessing:** Resizes, expands dimensions, and scales the image to match the precise input requirements of the model.
* **Top-3 Predictions:** Decodes and displays the top 3 predicted classes along with their confidence scores.
* **Visual Output:** Displays the analyzed image using `matplotlib` right before printing the predictions.

---

##  Requirements

Make sure you have Python installed, then install the required dependencies using the following command:

```bash
pip install tensorflow numpy matplotlib requests
## How it Works & Usage
Model Loading: The script initializes the MobileNetV2 architecture pre-loaded with imagenet weights.

Image Download: It fetches a sample image from a GitHub repository using TensorFlow's utility tools.

The Prediction Pipeline (predict_image):

The image is loaded and resized to 224x224 pixels.

It gets converted into a NumPy array and reshaped to include the batch dimension: (1, 224, 224, 3).

The array is normalized using preprocess_input.

The model processes the image, generates predictions, and decodes them into human-readable labels.

To run the script, simply execute:

Bash
python image_recognition.py
 Expected Output
When you run the file, a window will pop up showing the image, and your terminal/console will print out the top classification results like this:

Plaintext
Top Predictions:
1. Samoyed → 0.8540
2. Arctic_fox → 0.0123
3. Pomeranian → 0.0089
(Note: Exact confidence scores may vary slightly based on the framework version or the specific image used).

 Customization
If you want to test the script with your own images, simply replace the url variable in the script with a direct link to any image online:

Python
url = "[https://your-custom-image-link.com/image.jpg](https://your-custom-image-link.com/image.jpg)"
