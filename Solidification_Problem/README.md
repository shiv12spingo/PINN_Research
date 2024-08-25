This folder contains codes of my attempts at solving a solidification problem of benchmark complexity using physics-informed AI. The research initiated with reading up existing literature on Physics-Informed Neural Networks and coding began along the line of implementation by [Blechschmidt](https://github.com/janblechschmidt/PDEsByNNs). You can read all details of my research in my master's thesis DDP2_Thesis_180110076.pdf and view my presentation [here](https://shiv12spingo.github.io/aids/). You can also check out the pdf of my research poster. You can head to the previous [folder](https://github.com/shiv12spingo/PINN_Research/) to get some grasp of the topic by seeing simpler problems.

Most codes were created in Tensorflow 2.10.0 version and checked to be running in TFv 2.15.0 which is compatible with T4 GPU on Google Colab.

<li>First, I attempt to solve the problem using the standard PINN approach in Solidification_PINN.ipynb</li>
<li>As the loss function in the standard approach is complex to optimise, I use weights for different loss terms and apply the technique of adaptive weighting in Adaptive_WLF.ipynb</li>
<li>As the standard approach fails at temporal learning, I apply the technique of causal training in Causal_Training.ipynb</li>
<li>I implement causal training with 5 networks, one for each property-phase combination in Causal_Training_2.ipynb</li>
<li>In Causal_Training_3.ipynb, I experiment with multiple learning rates and varying causality parameter values for the causal training approach with 3 networks, getting the best results for constant learning rate = 0.01 and increasing value of causality parameter while training for 1000 epochs</li>
<li>I apply causal training with a modified sampling strategy and network structure in Causal_Training_4.ipynb</li>
<li>In Causal_Training_5.ipynb, I experiment with causal training for solving a simpler problem now having smaller peaks in composition profile</li>
<li>Simultaneous application of causal training and adaptive weighting can be found in CT_with_AW.ipynb</li>
<li>In CT+AW.ipynb I load models which have been causal trained and follow it up with adaptive weighting, thereby applying them alternately</li>
<li>I apply an efficient methodology based on my experiments with various strategies and achieve the best results in Final_Code.ipynb</li>
<li>As the above program didn't have pre-defined seeds everywhere, so another run can be found in Code_Run_2.ipynb</li>
