# [Project OffWorld Gym](README-offworld.md)

<img height="30" src="https://www.gstatic.com/devrel-devsite/prod/v8fd805b581ccd4ea25bb3c9d6fd75d38ac1dfcb55016a4d660f139190a81898b/tensorflow/images/lockup.svg"/>

This project aims to benchmark [Soft Actor Critic](https://arxiv.org/abs/1812.05905) agent based reinforcement learning algorithm in [OffWorld-gym ](https://gym.offworld.ai/) 
real world environment using [TensorFlow Agents API](https://www.tensorflow.org/agents/api_docs/python/tf_agents/agents/SacAgent) 

This work is inspired by [Soft Actor-Critic Algorithms and Applications](https://sites.google.com/view/sac-and-applications/)


- [ ] Dependencies are not optimized
- [x] Sim accuracy 70 - 80 % achieved :tada:
- [X] Store and load replay buffer as a file
- [x] Model intermediate state is saved :+1:
- [x] Tensorboard reward and steps metrics
- [x] Tensorboard model metrics
- [x] 50k random and traind model accuracy comparison
- [x] 3D visualisation works
### Tested on hardware specs

- **Ubuntu 20.04.3 LTS**[^1] 
- Intel i9-11980HK (8c)
- 32 GB RAM & 128 GB Swap[^2] (total >70 GB needed)
- NVidia RTX 3080 GPU 16GB (driver 495.44)

[^1]: Windows 10 works only for real environment. Sim env doesn't work (xHost problem)! No info about macOS.

[^2]: [Creating a SWAP partition in Ubuntu, Linux Mint and derivatives](https://itectec.com/ubuntu/ubuntu-fallocate-fallocate-failed-text-file-busy-in-ubuntu-17-04/)
## Installation for Linux

This guide is for running **[SAC_example.ipynb](SAC_example.ipynb)** with **Jupyter Notebook**. Other example files in examples folder might need different environment and/or dependencies!

As the installation could get messy, here is a quick guide:

### Docker

- Install latest version from [Install Docker Engine on Ubuntu](https://docs.docker.com/engine/install/ubuntu/)

- Follow [Post-Installation](https://docs.docker.com/engine/install/linux-postinstall/) steps

### Conda

- Install Miniconda from [Installing on Linux](https://docs.conda.io/projects/conda/en/latest/user-guide/install/linux.html)

### Git

- [Install Git](https://github.com/git-guides/install-git#install-git-on-linux) 

### Download files from Git

`git clone https://github.com/Karl-Git-Hub/offworld-gym.git`

Run in project folder root:

`conda env create -f environment.yml`

All necessary dependencies should be installed

Now activate env

`conda activate offworld-karl`

## Running

To run Jupyter notebook

`jupyter notebook`

Open notebook **[SAC_example.ipynb](SAC_example.ipynb)** in Jupyter server

After running **Environment** block, there will be debug info message with a link to 3D visualization server (when sim env)

### Tensorboard

View different logs in terminal (open link from terminal):

For training results:

`tensorboard --logdir=logs`

For model losses:

`tensorboard --logdir=models`

**Enjoy training**
