# DeepF-fNet: A Physics-Informed Neural Network for Vibration Isolation Optimization
State-of-the-art double-network PINN architecture to estimate the optimal structural parameters to block any wanted frequency within few cents of a second from the input request. The network, divided into <i>Inverse Eigenvalue Problem Solver</i> (IEPS) and <i>Wave Equation Solver</i> (WES), is applied to a Locally Resonant Metamaterial via a prediction/correction algorithm called SICE4.

This folder contains all the main codes to train and validate the <i>Deep Functional-Function Network</i>, with also a benchmark to test the SICE4 algorithm. In <strong>training</strong> DeepF-fNet_training.py is the main script (the dataset generated by data_generation.m is required), in <strong>validation</strong> DeepF-fNet_validation.py is the main script (a connection with Comsol&reg; via LiveLink&reg; server is required), in <strong>SICE4_benchmark</strong> two simulations of real-world use of the trained network are present: single_target_simulation.py analyzes the behavior of the algorithm with a single target frequency (also using Comsol&reg; for validation), while time_series_simulation.py simulates a varying noisy signal and how the optimal parameters change accordingly.

The required Comsol&reg; model for training and validation (<i>Direct_Band-gap_Problem2D.mph</i>) and the already validated dataset and IEPS and WES models can be found at this link: <a>https://drive.google.com/drive/folders/1EG6eaLHTpa6xni0hvZ0e7s8gPXKfa5Fb?usp=sharing</a>
