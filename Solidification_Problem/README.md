This folder contains codes of my attempts at solving a solidification problem of benchmark complexity using physics-informed AI. The research initiated with reading up Raissi's work on Physics-Informed Neural Network and coding began along the line of implementation by Blechschmidt.
<li>First, I attempt to solve the problem using the standard PINN approach in Solidification_PINN.ipynb</li>
<li>As the loss function in the standard approach is complex to optimise, I use weights for different loss terms and apply the technique of adaptive weighting in Adaptive_WLF.ipynb</li>
<li>As the standard approach fails at temporal learning, I apply the technique of causal training in Causal_Training.ipynb</li>
<li>I implement causal training with 5 networks, one for each property-phase combination in Causal_Training_2.ipynb</li>
