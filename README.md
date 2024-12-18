
GenAI-for-Heavy-Ion-Collision
=======

 Predicting Final State in Heavy-Ion Collisions: Fine-tuned 4 ML models on GPU to predict 
 final state distributions of Baryon, Charge, and Proton from 3D hydrodynamics data of Au-Au collisions.
 • Innovation in Approach: Implemented a Multi-Head Attention Transformer in PyTorch framework, surpassing
 traditional methods in handling noisy data, which led to more robust predictions than Neural Networks.
 • Impact: As the sole ML expert, reduced experimental time and resources by over 100 times, providing a scalable
 AI alternative to lab experiments and advancing the integration of Generative AI into the field of Nuclear Physics.

Models:
1. 3 nuclei model is a transformer trained on Ru, Zr, and Au nuclei
2. Au model is a transformer trained on Au collisions but predicting Final state of all possible energies
3. Histogram.ipynb contains visualizations of the heavy ion collisions
