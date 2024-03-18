# Mitigating Deep Reinforcement Learning Backdoors in the Neural Activation Space

## Running this code (ran on a Mac)

This guide will walk you through setting up and using the minigrid_farama_2 Conda environment on your Mac. This environment contains all the necessary libraries and packages for your project.

## Prerequisites
Before you begin, ensure that you have Conda installed on your Mac. If you do not have Conda installed, please follow the [official Conda installation guide for a Mac](https://docs.conda.io/projects/conda/en/latest/user-guide/install/macos.html). 

## Installation and Execution

Clone the Repository

Create the conda environment
```python
conda env create -f environment.yml
conda activate minigrid_farama_2
```
Set PYTHONPATH
```python
export PYTHONPATH= "/path/to/file/meta_rl/Minigrid"
echo $PYTHONPATH
```

Run the visualize file, and edit the "visualize.py" file and "crossings.py" code according to the data you want to collect (Non-triggered/Triggered, Goal in field of view, Trigger in field of view, Thresholding Detector Algorithm)(Trigger on/Non-Trigger off)
```python
python3 -m scripts.visualize --env MiniGrid-LavaCrossingS9N1-v0 --model DSLP_Crossings_Trigger_60k_256_neurons --episodes 1000
```

To run the training file from scratch , and edit the "visualize.py" file and "crossings.py" code according to the data you want to collect (Non-triggered/Triggered, Goal in field of view, Trigger in field of view, Thresholding Detector Algorithm)(Trigger on/Non-Trigger off)
```python
python3 -m scripts.train --algo ppo --env MiniGrid-LavaCrossingS9N1-v0  --model model_name --save-interval 10 --frames 60000000
```
