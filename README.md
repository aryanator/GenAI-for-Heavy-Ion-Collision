
GenAI-for-Heavy-Ion-Collision
=======

 Predicting Final State in Heavy-Ion Collisions: Fine-tuned 4 ML models on GPU to predict 
 final state distributions of Baryon, Charge, and Proton from 3D hydrodynamics data of Au-Au collisions.
 • Innovation in Approach: Implemented a Multi-Head Attention Transformer in PyTorch framework, surpassing
 traditional methods in handling noisy data, which led to more robust predictions than Neural Networks.
 • Impact: As the sole ML expert, reduced experimental time and resources by over 100 times, providing a scalable
 AI alternative to lab experiments and advancing the integration of Generative AI into the field of Nuclear Physics.

Goal: In 3D Hydro collisions, we wanted to see if there exists a critical point or not in the collisons of the heavy ions. 
However, the limitation was that the data was limited to work with. ANd to find the critical point, a lot more data is required but performing such lab experiments takes a lot of time and resources.
Thus, the goal was to leverage the predictive power of Machine Learning to generate data on a latrge scale and check for the existence of such a critical point.

Here I have the initial state of 3D Hyrdrdynamic collisions of nuclei of Gold(Au), Ruthenium(Ru), and Zurkonium(Zr) at different energy levels.
The goal is to predict the final state and important to note that the data contains lots of noise.
This includes predicting the final Charge distribution, Proton distribution, Baryon Distribution, Neutron Distribution, etc.

Tried the following models:
1. Linear Regression
2. MultiLayer Perceptron
3. Ridge Regression
4. Polynomial Ridge Regression
5. Two neural network models
6. The Multi attention Transformer

The Transformer model worked the best because of the sequential and noisy nature of data. Leveraging the attention mechanism preserves the context of the evolution in the collision and successfuly ignores the noise altogether through positional encondings.
Summary of the techniques used-
1. Finetuning the model on multiple parameters including the model architecture
2. Tried multiple loss functions and Huber loss gave the best results
3. Designed a custom Guassian filter to remove the random noises in data
4. Tried techniques like standarzing the data and then deconvoluting or inversing the predictions to obtain the accurate results
And a lot of other minor hacks to gradually improve the result

Code:
1. Ru_Zr_Au model is a transformer trained on Ru, Zr, and Au nuclei
2. Au model is a transformer trained on Au collisions but predicting Final state of all possible energies
3. Data Visualization.ipynb contains visualizations of the heavy ion collisions, very vital for this task to get an overview of energy conservation

Besides, a lot of other undocumented work and attempts were made. If curious or want to see what went wrong visit- https://www.kaggle.com/work/collections/14401886
