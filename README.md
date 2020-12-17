# Hybrid-Quantum-Classical-Neural-Network
Using two qubits to predict one of three digits - 0, 1, or 2.

The IPYNB file may not open, so use the following link:
https://nbviewer.jupyter.org/github/ZakariaPZ/Hybrid-Quantum-Classical-Neural-Network/blob/master/HybridNet.ipynb

Note: Code is still being cleaned. 

  This program was an effort to explore how classical machine learning can be used in conjunction with quantum computing. The classical network on its own does a much better job at classifying MNIST digits compared to this hybrid network, but it is nonetheless interesting to see how the two fields cooperate. 
  
  First, there is a classical node to process the visual data which is then fed into a quantum layer. The quantum layer then takes the classical output and uses it in a rotation gate. The gate is applied to the qubits (I am working on making multiple unique rotation gates - one for each qubit). The qubits collapse to a state after measurement. In the code posted here, I use two qubits which collapse to 00, 10, 01, and 11. I am experimenting with the effect of using more qubits in relation to how many digits are effectively predicted. The probabilities of each state are used to predict numbers from 0-3. Ideally, the fourth digit (3) is never predicted. Two things I believe I can improve are 1) increase the size of the training data and 2) provide a classical input for each gate. In any case, with the current setup, two qubits allow for the prediction of three digits. Any suggestions are welcome! 
  
  Backpropagation for the quantum layer is done via the [parameter shift rule](https://arxiv.org/pdf/1905.13311.pdf). This allows for the calculation of the gradient to tweak the classical network on the basis of the entire network's behaviour. 
  
  
  
   
  
