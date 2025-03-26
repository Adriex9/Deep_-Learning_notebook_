Dog and Cat Breed Classification with Deep Learning on The Oxford-IIIT Pet dataset
This project involves building a deep learning model for classifying dog and cat breeds using images. The model leverages the VGG16 architecture with transfer learning to achieve high accuracy on a dataset containing multiple dog and cat breeds.

Project Overview
Data Handling: The dataset consists of images of different dog and cat breeds. The initial challenge involved handling image data and working with byte strings, which was solved by using the PIL library.

Environment Setup: Initially, I worked without a powerful GPU, which led to memory issues and slow training. After upgrading to a T4 GPU on Google Colab, training performance significantly improved.

Model Architecture:

Started with a simple model and gradually improved it.
The model was based on VGG16 (pre-trained on ImageNet), and I fine-tuned it using data augmentation, Dropout and early stopping to avoid overfitting.


Final Results: After applying the above steps, the model achieved ~80% accuracy

Dependencies: 
-TensorFlow
-Keras
-NumPy
-Matplotlib
-scikit-learn
