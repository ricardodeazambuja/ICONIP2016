# Experiments used for the paper ~~submitted to~~ presented at [ICONIP2016](http://www.iconip2016.org)
# Graceful Degradation under Noise on Brain Inspired Robot Controllers
## Abstract
How can we build robot controllers that are able to work under harsh conditions, but without experiencing catastrophic failures? As seen on the recent Fukushima's nuclear disaster, standard robots break down when exposed to high radiation environments. 
Here we present the results from two arrangements of Spiking Neural Networks, based on the Liquid State Machine (LSM) framework, that were able to gracefully degrade under the effects of a noisy current injected directly into each simulated neuron. 
These noisy currents could be seen, in a simplified way, as the consequences of exposition to non-destructive radiation.
The results show that not only can the systems withstand noise, but one of the configurations, the Modular Parallel LSM, actually improved its results, in a certain range, when the noise levels were increased. Also, the robot controllers implemented in this work are suitable to run on a modern, power efficient neuromorphic hardware such as SpiNNaker.
### (this work is based on [github.com/ricardodeazambuja/IJCNN2016](https://github.com/ricardodeazambuja/IJCNN2016))

1. The trajectories are generated using a simulated BAXTER robot inside V-REP:
    - BEE_Simulator_ArmControl_VREP_trajectories-generator_v1-SQUARE.ipynb
    - /VREP_scenes/Baxter_IK_felt_pen_pick-and-place_learning_ICONIP2016.ttt

2. Training data (output spikes) are generated using the notebook:
    - BEE_Simulator_ArmControl_VREP_LSM_DATA-GENERATOR.ipynb

3. After the generation of the training data, it is necessary to train the readouts. This is done by:
    - BEE_Simulator_ArmControl_VREP_LSM_LINEAR_REGRESSION-Parallel_Maass.ipynb
    - BEE_Simulator_ArmControl_VREP_LSM_LINEAR_REGRESSION.ipynb

4. With all the readout weights defined, it's possible to verify the system using only the LSMs:
    - BEE_Simulator_ArmControl_VREP_LSM_DATA-TESTER-VREP.ipynb


## OBS:  

### BEE SNN simulator:  
https://github.com/ricardodeazambuja/BEE  

### Dynamic Time Warping (DTW):  
https://github.com/ricardodeazambuja/DTW

### Python scripts in general:  
https://github.com/ricardodeazambuja/Python-UTILS

### V-REP simulator:  
http://www.coppeliarobotics.com/downloads.html  
  
### Preprint version:  
https://github.com/ricardodeazambuja/ICONIP2016/blob/master/ICONIP2016_preprint.pdf

### Bibtex citation:
https://github.com/ricardodeazambuja/ricardodeazambuja.github.io/raw/master/public/citations/azambuja_graceful_2016.bib  

### Final Springer Link version:  
http://link.springer.com/chapter/10.1007/978-3-319-46687-3_21

### Related works:  
https://github.com/ricardodeazambuja/IJCNN2016  
https://github.com/ricardodeazambuja/IJCNN2017  
https://github.com/ricardodeazambuja/IJCNN2017-2  
https://github.com/ricardodeazambuja/I2MTC2017-LSMFusion


