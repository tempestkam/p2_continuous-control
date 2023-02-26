[demo]: https://user-images.githubusercontent.com/10624937/43851024-320ba930-9aff-11e8-8493-ee547c6af349.gif "Trained Agent"

# Project 2: Continuous Control
Continuous Control is a project within the deep reinforcement learning that is udacity nanodegree.
Unity Machine Learning Agents (ML-Agents) is an open source Unity plug-in that allows games and simulations to be used as training environments for intelligent agents.
 
In this environment, a double-jointed arm moves against a target. The target turns around the arm. If the arm contacts the green sphere, it is rewarded 0.1 per step. The agent's goal is to contact the target sphere in as many steps as possible. The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocity. The action is a vector of 4 numbers corresponding to the torques applied to the two joints. The elements of the action vector must be numbers between -1 and 1.

There are two options, one with one agent and the other with 20 agents. I chose the one with 20 agents. The task is episodic, and the goal is to have an average score of 30 or higher over 100 consecutive episodes.


# Requirement

* box2d 2.3.10
* box2d-py 2.3.8
* gym 0.26.2
* ipython 7.16.3
* matplotlib 3.3.4
* numpy 1.19.5
* pip 21.3.1
* python 3.6.15
* pytorch 0.4.0 

# Installation

Not all of the following steps may be necessary.
My operation system is Windows 10 Pro 64bit.
 
1.Create (and activate) a new environment with Python 3.6.
 
```
conda create --name drlnd python=3.6 
activate drlnd
```
2.Download SWIG, including the pre-built executable, and unzip it somewhere on your PC. Use SWIG 3.0.12.
Add the SWIG directory containing Swig.exe to the system PATH environment variable.

(https://sourceforge.net/projects/swig/files/swigwin/)

3.Install Microsoft Visual C++ 14.0. Available in "Microsoft Visual C++ Build Tools".

(https://visualstudio.microsoft.com/downloads/)

4.Install the base Gym library.

```
pip install gym
pip install box2d
conda install -c conda-forge box2d-py
```

5.Upgrade pip.
see:https://github.com/ijl/orjson/issues/192

Since execution as is will result in an error, do the following.

```
pip install --upgrade pip
```

6.Clone the Course Repository.
see:(https://github.com/udacity/deep-reinforcement-learning/issues/13)

```
git clone https://github.com/udacity/Value-based-methods.git
cd Value-based-methods/python
```

Since execution as is will result in an error, do the following.

On windows,

Open Value-based-methods/python/requirements.txt
Remove the line torch==0.4.0

On anaconda,

```
conda install pytorch=0.4.0 -c pytorch
cd Value-based-methods/python/
pip install .
```

7.Create an IPython kernel for the drlnd environment.

``` 
python -m ipykernel install --user --name drlnd --display-name "drlnd"
```

8.Install matplotlib.

```
conda install matplotlib
```

9.Before running code in a notebook, change the kernel to match the drlnd environment by using the drop-down Kernel menu.

10.Download the Unity Environment.

Windows (64-bit):
(https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)

Then, place the file in the `p2_continuous-control/` folder in the course GitHub repository, and unzip (or decompress) the file.

# Instructions
 
Open the file `Continuous_Control.ipynb` (located in the `p2_continuous-control/` folder of the course GitHub repository).
Run through the cells, starting with the first cell.
Cells after "4.It's Your Turn!" are the implementation that uses a Python API to control the agent.
When the cell with the ddpg function is executed, training of the model begins.
To check agent behavior after training, run the cell after the ddpg function cell, load the weights after training, and run the ddpg function cell with the train_mode=False argument.
