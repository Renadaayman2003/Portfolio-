# Real vs. Fake Faces Detection

This project aims to detect real and fake faces using convolutional neural networks (CNNs) and transfer learning with XceptionNet and ForensicTransfer models.

## Dataset

The dataset consists of 140,000 images, with 70,000 real faces from the Flickr dataset collected by Nvidia and 70,000 fake faces generated by StyleGAN. The images are resized to 256px and split into training, validation, and test sets.

- Training: 100,000 images (50,000 real, 50,000 fake)
- Validation: 20,000 images (10,000 real, 10,000 fake)
- Test: 20,000 images (10,000 real, 10,000 fake)

## Models

### CNN Model
The CNN model consists of several convolutional and pooling layers followed by fully connected layers. It achieves an accuracy of 97% on the test set.

### XceptionNet Model
The XceptionNet model is used with transfer learning, pre-trained on ImageNet, and fine-tuned on the dataset. It achieves an accuracy of 91% on the test set.

### ForensicTransfer Model
The ForensicTransfer model is based on XceptionNet and used with transfer learning. It achieves an accuracy of 68% on the test set.

## Results

### CNN Model
- Precision: 97%
- Recall: 97%
- F1-score: 97%

### XceptionNet Model
- Precision: 92%
- Recall: 91%
- F1-score: 91%

### ForensicTransfer Model
- Precision: 100% (real), 0% (fake)
- Recall: 68% (real), 0% (fake)
- F1-score: 81% (real), 0% (fake)

## Conclusion
The CNN model outperforms the XceptionNet and ForensicTransfer models in terms of overall accuracy, precision, recall, and F1-score. However, the XceptionNet model also provides a strong performance and is more efficient in terms of computational resources compared to the CNN model.
