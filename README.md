# 📹 ShopGuard: AI-Powered Shoplifting Detection

This project utilizes a deep learning model to detect shoplifting activities in real-time video streams. By combining a Convolutional Neural Network (CNN) for feature extraction and a Recurrent Neural Network (RNN) for analyzing temporal patterns, ShopGuard can accurately distinguish between regular shoppers and individuals exhibiting shoplifting behaviors.

---

## 📜 Table of Contents

- [About The Dataset](#-about-the-dataset)
- [Model Architecture](#-model-architecture)
- [Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#-usage)
- [Results](#-results)
- [Contributing](#-contributing)
- [License](#-license)
- [Acknowledgments](#-acknowledgments)

---

## 📊 About The Dataset

The model was trained on a custom dataset of videos categorized into two classes: "shoplifters" and "non-shoplifters." The dataset contains a variety of scenarios to ensure the model's robustness. The distribution of frames per video is as follows:

![Distribution of Frames per Video](https://i.imgur.com/7123jO6.png)

---

## 🧠 Model Architecture

The core of this project is a hybrid CNN-RNN model designed for video classification:

-   **CNN Base (MobileNetV2):** A pre-trained MobileNetV2 is used for efficient feature extraction from individual video frames. This model is lightweight and ideal for real-time applications.
-   **TimeDistributed Layer:** This wrapper allows the CNN to process each frame of a video sequence independently.
-   **GRU (Gated Recurrent Unit) Layer:** A GRU layer processes the sequence of features extracted by the CNN to capture temporal dependencies and patterns in the video.
-   **Dense Layers:** Fully connected layers at the end classify the video as either containing shoplifting activity or not.

---

## 🚀 Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites

You will need Python 3.x and the following libraries:

-   TensorFlow
-   OpenCV
-   scikit-learn
-   Matplotlib
-   NumPy

### Installation

1.  Clone the repo
    ```sh
    git clone https://github.com/your_username/ShopGuard.git
    ```
2.  Install Python packages
    ```sh
    pip install tensorflow opencv-python scikit-learn matplotlib numpy
    ```

---

## 🏃‍♀️ Usage

To use this model, you can run the `Untitled9.ipynb` notebook in a Jupyter or Colab environment. The notebook contains all the code for:

1.  Loading and preprocessing the video data.
2.  Building and compiling the CNN-RNN model.
3.  Training the model on the dataset.
4.  Evaluating the model's performance.

---

## 📈 Results

The model achieves a high accuracy of approximately **99.42%** on the test set.

### Accuracy and Loss History

The training history shows that the model learns effectively, with the validation accuracy tracking the training accuracy closely and the validation loss decreasing consistently.

![Accuracy and Loss History](https://i.imgur.com/G5g2m8r.png)

### Confusion Matrix

The confusion matrix demonstrates the model's excellent performance in distinguishing between the two classes, with very few misclassifications.

![Confusion Matrix](https://i.imgur.com/1F6v7yL.png)

---

## 🙌 Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

---

## 🙏 Acknowledgments

-   Hat tip to anyone whose code was used
-   Inspiration
-   etc.
