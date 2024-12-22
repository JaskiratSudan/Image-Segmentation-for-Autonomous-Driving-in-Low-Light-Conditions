# Image Segmentation for Autonomous Driving in Low-Light Conditions

### Project Overview

This project aims to enhance autonomous vehicle perception by improving image segmentation in challenging environments, particularly in low-light and adverse weather conditions. The goal is to develop robust models capable of accurately distinguishing vehicles from their surroundings, thereby enhancing safety and reliability in autonomous driving systems.

### Key Features

- Utilizes the BDD100K dataset, featuring diverse driving scenarios
- Implements transfer learning and fine-tuning techniques
- Focuses on two main architectures: MobileNetV2 U-Net and Xception U-Net
- Addresses challenges in nighttime and adverse weather conditions

### Models

#### MobileNetV2 U-Net

- **Architecture**: Lightweight model designed for real-time applications
- **Pre-training**: ImageNet
- **Fine-tuning**: BDD100K dataset, with emphasis on nighttime images
- **Performance**: 
  - Accuracy: 90.4%
  - Binary Cross-Entropy: 0.197
  - Dice Loss: 0.92

#### Xception U-Net

- **Architecture**: Custom model with Xception backbone
- **Training**: Fine-tuned on BDD100K dataset
- **Performance**:
  - Accuracy: 99.5%
  - Dice Coefficient: 0.8999
  - Binary Cross-Entropy: 0.0129
  - Dice Loss: 0.1001

### Methodology

1. **Data Preprocessing**:
   - Image resizing to 256x256
   - Normalization
   - Data augmentation (flipping, rotation, brightness adjustment)

2. **Training Process**:
   - Initial training on daytime images
   - Fine-tuning on nighttime imagery
   - Use of Dice loss and binary cross-entropy for optimization

3. **Evaluation Metrics**:
   - Accuracy
   - Intersection over Union (IoU)
   - Dice Coefficient
   - Precision and Recall

### Results

<img width="1478" alt="image" src="https://github.com/user-attachments/assets/90eb530e-66e1-4adc-98a9-e9931c1618ba" />

- Xception U-Net outperformed MobileNetV2, showing superior segmentation quality across diverse conditions
- MobileNetV2 demonstrated competitive accuracy with lower computational demands, suitable for resource-constrained settings
- Fine-tuning significantly improved performance, especially in low-light conditions

| Metric | MobileNetV2 (After FT)| Xception U-Net (After FT)|
|--------|-------------|----------------|
| Accuracy (%) | 90.40 | 99.50 |
| Dice Loss | 0.92 | 0.1001 |
| Binary Cross-Entropy | 0.197 | 0.0129 |
| Dice Coefficient | 0.08 | 0.8999 |

### Conclusions

- Xception U-Net proved most reliable for complex segmentation tasks in autonomous driving
- The study highlights the importance of model architecture, pre-trained models, and fine-tuning in enhancing segmentation performance
- Future work could explore additional environmental variables and novel architectures to further improve accuracy
