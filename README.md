# Impact-of-additive-noise-on-MNIST-digit-classification-using-a-simple-neural-network

## **Overview**
This notebook explores the impact of additive noise on MNIST digit classification using a simple neural network.

---

## **Objectives**
- Load and inspect the MNIST dataset  
- Introduce varying levels of Gaussian noise to training and test images  
- Build a dense neural network (128-unit hidden layer) with Adam optimizer  
- Evaluate model accuracy on clean and noisy inputs  
- Analyse noise-robustness by varying training/test noise levels

---

## **Methodology**
- **Data Preparation:**  
  - Download MNIST; visualise sample images  
  - Define functions to add noise at specified amplitude  

- **Model Architecture:**  
  - Dense → ReLU → Dense → Softmax  
  - Loss: `SparseCategoricalCrossentropy`, Optimizer: Adam  

- **Experiments:**  
  - Baseline training on clean data (target ≥ 95% accuracy)  
  - Loop over noise levels (0–300) to retrain and evaluate  
  - Plot test accuracy vs. noise amplitude  

---

## **Key Results**
- **Baseline:** Achieved > 95% accuracy on clean test set  
- **Noisy Training:** Improved performance on noisy test images compared to baseline  
- **Noise Sensitivity:** Accuracy degrades as noise increases if model trained only on clean data  

---

## **Limitations & Future Work**
- Model limited to one hidden layer; consider CNNs for spatial features  
- Only additive noise tested; explore occlusions and blur  
- Investigate data-augmentation strategies for further robustness

