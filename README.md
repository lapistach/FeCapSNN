# FeCapSNN

A Spiking Neural Network (SNN) framework with learnable membrane time constants represented by analog ferroelectric capacitances. 
This repository contains the origin codes and TensorBoard logs for the paper [TBD](https://fr.wikipedia.org/wiki/TBD). The code was adapted from [this original work](https://github.com/fangwei123456/Parametric-Leaky-Integrate-and-Fire-Spiking-Neuron/) by Fang et al. where all installation and network training informations can be found. In this work, all the code is implemented in Jupyter Notebooks on Google Colab and was run on the A100 GPUs offered by Colab.

## Installation

This code relies on an old version of [SpikingJelly](https://github.com/fangwei123456/spikingjelly/). The installation is **already implemented** in the Colab notebooks of the `code` folder. In the case where the user wants to retrieve the depencies in his own virtual environment he can download them as follows:
````
git clone https://github.com/fangwei123456/spikingjelly.git
cd spikingjelly
git reset --hard 73f94ab983d0167623015537f7d4460b064cfca1
python setup.py install
````

## Example

After creating a dataset folder as explained [here](https://github.com/fangwei123456/Parametric-Leaky-Integrate-and-Fire-Spiking-Neuron/tree/main#datasets) you can :
- run `Training.py` to train the SNN.
- run `PostProcessing.py` to find the parameters that yield the highest accuracy.
- run `Inference.py` to perform inference with the selected best parameters apart from the membrane time constants which are readapted to the capacitance values of your choosing.
