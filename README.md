# High-energy physics Fast inference of Diffusion models LHC dataset 

## INTRODUCTION

Understanding Particle Showers: In high-energy physics, accurately simulating particle showers in calorimeters is critical for understanding particle interactions and designing experiments.
Geant4, while precise, is computationally intensive and often impractical for large-scale experiments.

Accelerating Simulations: Leverage generative models (VAE, VQ-VAE, and diffusion transformer models) to approximate calorimeter responses, significantly reducing simulation times.

Addressing Challenges in Diffusion Models: Although diffusion models are the most accurate generative models for simulating high-granularity calorimeter data, their slow inference is a major bottleneck.
The project focuses on optimizing inference speed without compromising accuracy.

## OBJECTIVE

Optimized Diffusion Models:Faster inference algorithms or architectural tweaks to existing diffusion transformers.

Comparative Analysis:Benchmarks comparing VAE, VQ-VAE, and diffusion models in terms of accuracy, speed, and computational efficiency.

## Understanding the High granularity dataset

### Dataset Overview
```
Composition:
Contains 4 HDF5 files:
	•	dataset_3_1.hdf5 and dataset_3_2.hdf5 for training.
	•	dataset_3_3.hdf5 and dataset_3_4.hdf5 for evaluation.
 Number of Samples:
	•	Each file contains 50k GEANT4-simulated showers of electrons.
 Energy Distribution:
	•	Electron energies are log-uniformly distributed between 1 GeV and 1 TeV, ensuring representation across a wide range of energies.
Detector Geometry:
	•	High-granularity calorimeter:
	•	45 layers, with each layer divided into:
	•	18 radial bins.
	•	50 angular bins.
	•	Total voxel count:  18 \times 50 \times 45 = 40,500 
Simulation Origin:
	•	Generated using the Par04 example from the Geant4 toolkit.
 
```
### Data Visualization

Visualization will help explore the dataset, identify patterns, and validate preprocessing steps.

Graphical Visualization


	1.	Energy Distribution:
	•	Plot histograms of electron energies (log-uniform distribution) for each dataset.
	•	Use tools like matplotlib or seaborn.
 
 
  <img width="708" alt="Screenshot 2024-12-30 at 9 23 40 PM" src="https://github.com/user-attachments/assets/af74980f-bf82-4afa-b78d-3da985132b0d" />
  
  
	2.	Voxel Activation:
	•	Visualize a single calorimeter layer or a slice of the 3D grid using heatmaps.
 
 
 <img width="696" alt="Screenshot 2024-12-30 at 9 23 57 PM" src="https://github.com/user-attachments/assets/91c3de35-9388-47f4-909e-c9bb4d7be9b3" />
 
 
	3.	Shower Profile:
	•	Plot longitudinal and transverse energy profiles across layers.
	4.	3D Shower Visualization:
	•	Use libraries like matplotlib (3D scatter plot) or plotly for interactive 3D voxel intensity visualization. 


<img width="761" alt="Screenshot 2024-12-30 at 9 22 11 PM" src="https://github.com/user-attachments/assets/115012d1-c514-43fa-a6b3-27c68fc290a0" />   


<img width="751" alt="Screenshot 2024-12-30 at 9 22 54 PM" src="https://github.com/user-attachments/assets/0d08d2db-1583-4009-96d2-67aee9ccd4d0" />
      

 

