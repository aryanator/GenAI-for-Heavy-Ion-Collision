
# **GenAI-for-Heavy-Ion-Collision**

## **Project Overview**
This project focuses on predicting the final state distributions (Baryon, Charge, Proton, etc.) in heavy-ion collisions using 3D hydrodynamics data from Au-Au collisions. By leveraging machine learning, the goal is to generate large-scale data to investigate the existence of a critical point in heavy-ion collisions, reducing the need for time-consuming and resource-intensive lab experiments.

### **Key Achievements**
- **Innovation in Approach**: Implemented a **Multi-Head Attention Transformer** in PyTorch, which outperformed traditional methods (e.g., Neural Networks) in handling noisy data, leading to more robust predictions.
- **Impact**: As the sole ML expert, reduced experimental time and resources by **over 100 times**, providing a scalable AI alternative to lab experiments and advancing the integration of Generative AI into Nuclear Physics.

---

## **Problem Statement**
In 3D hydrodynamics collisions, the goal is to determine whether a critical point exists in heavy-ion collisions. However, the limited availability of experimental data poses a significant challenge. Conducting lab experiments to gather sufficient data is time-consuming and resource-intensive. This project aims to address this limitation by using machine learning to predict final state distributions and generate large-scale data for analysis.

---

## **Data Description**
The dataset consists of the initial state of 3D hydrodynamic collisions for nuclei of:
- Gold (Au)
- Ruthenium (Ru)
- Zirconium (Zr)

The collisions occur at various energy levels, and the data contains significant noise. The goal is to predict the final state distributions, including:
- Charge distribution
- Proton distribution
- Baryon distribution
- Neutron distribution

---

## **Approach**
### **Models Tested**
1. Linear Regression
2. MultiLayer Perceptron (MLP)
3. Ridge Regression
4. Polynomial Ridge Regression
5. Neural Networks (2 variants)
6. **Multi-Head Attention Transformer** (Best Performing Model)

### **Why the Transformer Worked Best**
The Transformer model excelled due to its ability to handle sequential and noisy data. The attention mechanism preserves the context of the collision evolution and effectively ignores noise through positional encodings.

---

## **Techniques Used**
1. **Model Fine-Tuning**: Optimized model architecture and hyperparameters for better performance.
2. **Loss Functions**: Experimented with multiple loss functions; **Huber loss** yielded the best results.
3. **Noise Reduction**: Designed a custom Gaussian filter to remove random noise from the data.
4. **Data Preprocessing**: Standardized the data and applied deconvolution techniques to improve prediction accuracy.
5. **Other Improvements**: Implemented various minor optimizations to gradually enhance results.

---

## **Code Overview**
The repository contains the following key components:
1. **Ru_Zr_Au Model**: A Transformer trained on Ru, Zr, and Au nuclei collisions.
2. **Au Model**: A Transformer trained exclusively on Au collisions, predicting final states across all energy levels.
3. **Data Visualization.ipynb**: Contains visualizations of heavy-ion collisions, crucial for understanding energy conservation and data patterns.

---

## **Additional Work**
Several undocumented experiments and attempts were made during the project. For more details or to explore what didn’t work, visit:  
[Kaggle Work Collection](https://www.kaggle.com/work/collections/14401886)

---

## **Future Work**
- Expand the dataset to include more nuclei and energy levels.
- Explore advanced architectures (e.g., Graph Neural Networks) for better representation of collision dynamics.
- Improve noise reduction techniques to further enhance prediction accuracy.

---

### **Summary**
This project demonstrates the successful application of machine learning, particularly Transformers, to predict final state distributions in heavy-ion collisions. By reducing reliance on lab experiments, it paves the way for scalable and efficient data generation in nuclear physics research.

---

### **Key Takeaways**
- Transformers are highly effective for sequential and noisy data in physics applications.
- Machine learning can significantly reduce experimental time and resource requirements.
- This work contributes to the growing integration of AI in scientific research.

---
