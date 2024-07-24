# 🎯 Polyp Detection Using YOLOv9 and Augmentation

Welcome to the repository for polyp detection using the YOLOv9 model with various data augmentation techniques. This project demonstrates the effectiveness of the YOLOv9 model in detecting polyps in colonoscopy images and explores different augmentation methods to enhance model performance.

![Polyp Detection](https://raw.githubusercontent.com/your-repository/path/to/image_page1_0.png)

## 📋 Table of Contents
1. [Introduction](#introduction)
2. [YOLOv9 Architecture](#yolov9-architecture)
3. [Augmentation Techniques](#augmentation-techniques)
4. [Experiments](#experiments)
   - [Base YOLOv9](#base-yolov9)
   - [YOLOv9 with HSV](#yolov9-with-hsv)
   - [YOLOv9 with HSV, Shearing, Translation, and Rotation](#yolov9-with-hsv-shearing-translation-and-rotation)
5. [Conclusion](#conclusion)
6. [References](#references)

## 🌟 Introduction

Cancer is one of the leading causes of mortality worldwide. Colorectal cancer (CRC) is particularly deadly, with polyps being early indicators of potential malignancies. Early detection through endoscopy and advanced deep learning models can significantly improve treatment outcomes.

![Colonoscopy Process](https://raw.githubusercontent.com/your-repository/path/to/image_page3_0.png)

## 🧠 YOLOv9 Architecture

In the latest version of YOLOv9, modern deep neural networks incorporate deeper layers to enhance object detection accuracy. However, during the feedforward process, many informative features of the input may be lost. YOLOv9 addresses this issue with a new architecture named GELAN, designed to capture the most informative features and process them efficiently.

![YOLOv9 Architecture](https://raw.githubusercontent.com/your-repository/path/to/image_page5_0.png)

Reversible architectures, masked modeling, and deep supervision are three distinct methods used to enhance neural networks' capability to retain and manipulate meaningful information throughout training and inference processes. YOLOv9 introduces 'Programmable Gradient Information' (PGI), which adapts the main propagation technique originally used in deep supervision by programming it to enhance meaningful feature extraction.

## 🛠 Augmentation Techniques

Data augmentation is crucial for training deep neural networks, especially when the dataset is small. Here are some techniques used:

### 🔄 Geometric Transformations
- **Rotation**
- **Flipping**
- **Translation**
- **Shearing**
- **Zooming**

### 🎨 Color Space Transformations
- **Brightness Adjustment**
- **Contrast Adjustment**
- **Saturation Adjustment**
- **Hue Adjustment**

### ✂️ Random Erasing
- **Cutout**

### 📶 Noise Injection
- **Gaussian Noise**
- **Salt and Pepper Noise**

### 🌀 Filtering
- **Gaussian Blur**
- **Edge Enhancement**

### 🔀 Mixing Images
- **Mixup**
- **CutMix**

### 🔗 Transformation Chains
- **Sequential Augmentation**

![Augmentation Techniques](https://raw.githubusercontent.com/your-repository/path/to/image_page11_0.png)

## 🔬 Experiments

### Base YOLOv9

The pre-trained YOLOv9 model was fine-tuned on the Kvasir dataset. Initial training results showed promising improvements in polyp detection accuracy.

![Training Results](https://raw.githubusercontent.com/your-repository/path/to/image_page12_0.png)

| Class  | Precision | Recall | mAP 50 | mAP 50:90 |
|--------|-----------|--------|--------|-----------|
| All    | 0.829     | 0.85   | 0.87   | 0.563     |
| Labels | 0.833     | 0.942  | 0.897  | 0.683     |
| Polyps | 0.825     | 0.757  | 0.843  | 0.443     |

### YOLOv9 with HSV

By converting images from RGB to HSV color space, we observed better performance in detecting polyps due to improved handling of light reflections on polyp surfaces.

![HSV Transformation](https://raw.githubusercontent.com/your-repository/path/to/image_page13_0.png)

| Class  | Precision | Recall | mAP 50 | mAP 50:90 |
|--------|-----------|--------|--------|-----------|
| All    | 0.85      | 0.861  | 0.87   | 0.57      |
| Labels | 0.844     | 0.948  | 0.894  | 0.679     |
| Polyps | 0.856     | 0.773  | 0.857  | 0.471     |

### YOLOv9 with HSV, Shearing, Translation, and Rotation

Adding geometric transformations such as shearing, translation, and rotation did not significantly improve the model's performance. However, these experiments provided valuable insights into the effects of different augmentations.

![Geometric Transformations](https://raw.githubusercontent.com/your-repository/path/to/image_page14_0.png)

| Class  | Precision | Recall | mAP 50 | mAP 50:90 |
|--------|-----------|--------|--------|-----------|
| All    | 0.826     | 0.859  | 0.87   | 0.56      |
| Labels | 0.827     | 0.942  | 0.897  | 0.671     |
| Polyps | 0.825     | 0.777  | 0.843  | 0.448     |

## 📈 Conclusion

This study demonstrates the potential of using advanced deep learning techniques, specifically the YOLOv9 model, for polyp detection in colonoscopy images. Data augmentation techniques, particularly HSV adjustments, significantly enhance model accuracy and robustness.

## 📚 References

1. Asplund, J., et al. (2018) 'Survival trends in gastric adenocarcinoma: a population-based study in Sweden', Annals of Surgical Oncology, 25, pp. 2693-2702.
2. Gupta, M., Mishra, A. (2024) 'A systematic review of deep learning based image segmentation to detect polyp', Artificial Intelligence Review, 57(1), pp. 1-53.
3. Ali, S. (2022) 'Where do we stand in AI for endoscopic image analysis? Deciphering gaps and future directions', npj Digital Medicine, 5(1), pp. 184.
4. Ziegler, C.M., et al. (2004) 'Endoscopy: a minimally invasive procedure for diagnosis and treatment of diseases of the salivary glands', British Journal of Oral and Maxillofacial Surgery, 42(1), pp. 1-7.
5. Jha, D., et al. (2021) 'Real-time polyp detection, localization and segmentation in colonoscopy using deep learning', IEEE Access, 9, pp. 40496-40510.
6. Wang, C., Yeh, I., Liao, H.M. (2024) 'YOLOv9: Learning What You Want to Learn Using Programmable Gradient Information', arXiv preprint arXiv:2402.13616.
7. Khosla, C., Saini, B.S. (2020) 'Enhancing performance of deep learning models with different data augmentation techniques: A survey', IEEE, pp. 79.
8. Lalinia, M., Sahafi, A. (2024) 'Colorectal polyp detection in colonoscopy images using yolo-v8 network', Signal, Image and Video Processing, 18(3), pp. 2047-2058.
9. Qian, Z., et al. (2020) 'A new approach to polyp detection by pre-processing of images and enhanced faster R-CNN', IEEE Sensors Journal, 21(10), pp. 11374-11381.

Feel free to explore the repository and contribute to the project!
