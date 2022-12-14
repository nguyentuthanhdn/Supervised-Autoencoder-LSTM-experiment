# Supervised-Autoencoder-LSTM-experiment

Supervised Autoencoder<sup>(1)</sup> definitely helps improve the performance of a fully connected network. I wonder if this technique will generalise and improve the performance of an LSTM model in a timeseries context.

# Dataset
The Dataset was prepared by Zimming Xu (ziming4@ualberta.ca), containing 729 wells, each well's data contain 157 timesteps, and each timestep contains Height, Permeability, Length, Bottom hole Pressure, Gas Production, Water Production and Oil Production. Height, Permeability and Length are static data, while Pressure, Gas, Water and Oil Production are time-series quantities. 
The goal is to predicit the production rate of gas, water and oil over 157 timesteps using Height, Permeability, Length and Pressure.

# Results
Both the normal LSTM and Supervised Auto-encoder LSTM models can learn the trend of production quite well. However, SAE LSTM achieves a very slightly better result in terms of loss (Loss 170.7 for SAE LSTM and 175.6 for Traditional LSTM)

Significantly, when the Pressure is high, the production rates drop to 0 in both models, which is the expected behaviour in real-life applications. 

# Packages/Denpencies Requirements
- GPU for training
- Pytorch cuda 
- Numpy 
- Torchinfo
- Matplotlib
- Tensorboard 
- tqdm


# Citations
<sup>(1)</sup>Le, Lei, Andrew Patterson, and Martha White. "Supervised autoencoders: Improving generalization performance with unsupervised regularizers." Advances in neural information processing systems 31 (2018).
