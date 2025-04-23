# Waste_Segregation_Using_Deep_Learning_CNN

# Model Training and Evaluation Report

## 📊 Data Analysis

- Two pre-trained CNN models were tested: **ResNet** and **VGG16**.
- Initial evaluation results on the dataset:

| Model   | Test Loss | Test Accuracy |
|---------|-----------|---------------|
| ResNet  | 2.1379    | 24.46%         |
| VGG16   | 1.4356    | 46.42%         |

- **Observation**:  
  VGG16 performed significantly better than ResNet in both loss and accuracy.  
  Therefore, **VGG16** was selected for further model development.

---

## ⚙️ Model Training Results

### 1. **Transfer Learning Phase**
- Only the top layers were trained while keeping VGG16 base layers frozen.
- Results:
  - **Test Loss**: `0.8024`
  - **Test Accuracy**: `71.34%`

### 2. **Fine-Tuning Phase**
- Unfroze deeper layers of VGG16 and re-trained to improve feature extraction.
- Results:
  - **Test Loss**: `0.6061`
  - **Test Accuracy**: `79.27%`

- **Observation**:  
  Fine-tuning significantly improved the model performance compared to basic transfer learning.

---

## 📈 Training and Validation Curves

Training curves for accuracy and loss clearly showed improved convergence after fine-tuning.

- **Training Accuracy** and **Validation Accuracy** improved steadily.
- **Training Loss** and **Validation Loss** decreased as expected without overfitting.
  
  ### **Sequential Model**
  ![SequentialModel](https://github.com/user-attachments/assets/a57b8097-f201-437b-a699-49471c722389)

  ### **Sequential Model After Image Augmentation**
  ![SequentialModelAfterAugmentation](https://github.com/user-attachments/assets/db0aa740-53cc-476b-b642-8b99c02d35f7)

  ### **VGG16 Transfer Learning**
  ![VGG16_TransferLearning](https://github.com/user-attachments/assets/e854e7d0-0d7f-4bcd-8350-91ae8b548f24)

  ### **VGG16 Fine Tuning**
  ![VGG16_FineTuning](https://github.com/user-attachments/assets/b22fa1c2-363c-4130-8a6c-e42993703d16)





---

## 📋 Conclusion

- **VGG16** with **fine-tuning** achieved the best performance.
- Final **Test Accuracy** achieved: **79.27%**.
- Fine-tuning made a significant improvement of nearly **8%** over basic transfer learning.
- **ResNet** was not selected due to poor initial performance on the dataset.

---

## 👌 Created By

**Shashidhar Pattar**

