# Surveillance System Test Results

This directory contains test results for the real-time surveillance system, which is designed to detect violent activities using deep learning models. The system has been tested with three different versions of the model on various video samples.

## Model Versions

1. **0.81.h5 Model**  
   - An initial version of the violence detection model.
   - Provides basic detection capabilities with moderate accuracy.
   
2. **0.86.h5 Model**  
   - An improved version with better feature extraction and optimized training.
   - Higher accuracy and reduced false positives compared to the previous model.

3. **ViolenceModelFinal.keras**  
   - The most refined version with advanced deep learning techniques.
   - Utilizes enhanced training data for more reliable threat detection.
   - Designed for real-world deployment with the highest accuracy among the three.

## Test Results

The models were tested on multiple videos containing different scenarios of violent activities. The processed results for each model can be accessed using the links below:

- **Indian Street Fight**  
  - [Original](test_results/Indian%20street%20fight.mp4)  
  - [0.81.h5 Model](test_results/Indian%20street%20fight.mp4-0.81.h5.mp4)  
  - [0.86.h5 Model](test_results/Indian%20street%20fight.mp4-0.86.h5.mp4)  
  - [Final Model](test_results/Indian%20street%20fight.mp4-ViolenceModelFinal.keras.mp4)

- **Street Fight TKO 30 Seconds**  
  - [Original](test_results/Street%20fight%20tko%2030%20seconds.mp4)  
  - [0.81.h5 Model](test_results/Street%20fight%20tko%2030%20seconds.mp4-0.81.h5.mp4)  
  - [0.86.h5 Model](test_results/Street%20fight%20tko%2030%20seconds.mp4-0.86.h5.mp4)  
  - [Final Model](test_results/Street%20fight%20tko%2030%20seconds.mp4-ViolenceModelFinal.keras.mp4)

- **div-dip-test**  
  - [Original](test_results/div-dip-test.mp4)  
  - [0.81.h5 Model](test_results/div-dip-test.mp4-0.81.h5.mp4)  
  - [0.86.h5 Model](test_results/div-dip-test.mp4-0.86.h5.mp4)  
  - [Final Model](test_results/div-dip-test.mp4-ViolenceModelFinal.keras.mp4)

- **hem-dip-test**  
  - [Original](test_results/hem-dip-test.mp4)  
  - [0.81.h5 Model](test_results/hem-dip-test.mp4-0.81.h5.mp4)  
  - [0.86.h5 Model](test_results/hem-dip-test.mp4-0.86.h5.mp4)  
  - [Final Model](test_results/hem-dip-test.mp4-ViolenceModelFinal.keras.mp4)

- **local**  
  - [Original](test_results/local.mp4)  
  - [0.81.h5 Model](test_results/local.mp4-0.81.h5.mp4)  
  - [0.86.h5 Model](test_results/local.mp4-0.86.h5.mp4)  
  - [Final Model](test_results/local.mp4-ViolenceModelFinal.keras.mp4)

- **WWE**  
  - [Original](test_results/wwe.mp4)  
  - [0.81.h5 Model](test_results/wwe.mp4-0.81.h5.mp4)  
  - [0.86.h5 Model](test_results/wwe.mp4-0.86.h5.mp4)  
  - [Final Model](test_results/wwe.mp4-ViolenceModelFinal.keras.mp4)

### **Model Description: Long-term Recurrent Convolutional Network (LRCN) for Violence Detection**  

The violence detection model follows the **LRCN (Long-term Recurrent Convolutional Network) architecture**, combining **CNNs for spatial feature extraction** and **LSTMs for temporal sequence modeling**. This approach ensures effective video classification by learning both **frame-level features** and **sequential patterns** over time.  
- [Code Link](Models/Voilence_detection%20(1).ipynb)

#### **Model Structure**
1. **CNN Feature Extractor:**  
   - Uses **three convolutional layers** with **Batch Normalization** and **MaxPooling** to extract spatial features from individual frames.
   - The output is **flattened** and transformed into a sequence representation.  

2. **LSTM-based Temporal Modeling:**  
   - The extracted frame features are **repeated** across time steps to form a sequence.  
   - Two **stacked LSTM layers** process this sequence to learn temporal dependencies between frames.  

3. **Classification Layer:**  
   - Fully connected (`Dense`) layers refine the extracted features.  
   - A **Dropout** layer helps prevent overfitting.  
   - A **softmax layer** classifies the video as either **Violence (1) or Non-Violence (0)**.  

#### **Available Model Versions**
Three different trained models have been tested on various video samples, demonstrating their performance differences:
- **0.81.h5** – A model trained with an accuracy of **81%**, showing moderate reliability.  
- **0.86.h5** – A refined model achieving **86% accuracy**, improving detection capability.  
- **ViolenceModelFinal.keras** – The most optimized version, trained for better generalization and robustness.

