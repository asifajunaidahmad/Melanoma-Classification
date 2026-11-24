# Melanoma-Classification
Skin cancer is the most prevalent type of cancer. Melanoma, specifically, is responsible for 75% of skin cancer deaths, despite being the least common skin cancer.\
Currently, dermatologists evaluate every one of a patient's moles to identify outlier lesions or “ugly ducklings” that are most likely to be melanoma. In this code, i tried to identify melanoma in images of skin lesions. In particular, I use images within the same patient and determine which are likely to represent a melanoma. Using patient-level contextual information to development of image analysis tools, which could better support clinical dermatologists.

# Dataset
This set consists of 2357 images of malignant and benign oncological diseases, which were formed from The International Skin Imaging Collaboration (ISIC).\
All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant
# Model
A 9-class image classifier built on an ImageNet-pretrained ResNet50 (224×224 RGB, convolutional base only), followed by global average pooling and a 9-way softmax layer. It is trained with binary cross-entropy with label smoothing and tracked by accuracy; the extra dense, dropout and batch-norm layers are commented out.
