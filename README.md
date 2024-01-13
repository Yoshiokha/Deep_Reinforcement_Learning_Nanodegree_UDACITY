[//]: # (Image References)
Projet 1 Navigation

[image1]: https://user-images.githubusercontent.com/10624937/42135619-d90f2f28-7d12-11e8-8823-82b970a54d7e.gif "Trained Agent"

This project trains an agent to interact with Udacity's Bananas World such that it learns to pickup the yellow banans (+1) and ignore the blue bananas (-1) within each episode.

The code is written in PyTorch and Python 3.

## Environment
The below is a paraphrasing from the Udacity course's repo regarding this project's environment:

The goal of the agent is to collect as many yellow bananas (+1) within a given time while avoiding blue bananas (-1). The goal is to get an average score of +13 over 100 consecutive episodes.

According to Udacity: "The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around agent's forward direction." The agent is able to select from four discrete actions:

* 0 - move forward.
* 1 - move backward.
* 2 - turn left.
* 3 - turn right.

## Getting Started

After following the instructions defined here for downloading and installing: https://github.com/udacity/deep-reinforcement-learning/tree/master

My installation was based on 
* Windows 10 x64-based PC
* Python 3.6.13 :: Anaconda, Inc.

# Download the Unity Environment
For this project, you will not need to install Unity - this is because we have already built the environment for you, and you can download it from one of the links below. You need only select the environment that matches your operating system:
* Windows (64-bit):https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip
* Windows (32-bit):https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip
* Linux:https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip
* Mac OSX:https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip

Then, place the file in your Projet1_Bananas / folder, and unzip (or decompress) the file.

# Clone the Course Repository

```bash
# Instructions from Deep RL course for environment setup
conda create --name DRL_udacity_cpu python=3.6 
conda activate DRL_udacity_cpu

# after creating new conda python environment
cd <path/to/dev/directory>
git clone https://github.com/udacity/deep-reinforcement-learning.git
git clone https://github.com/Yoshiokha/Deep_Reinforcement_Learning_Nanodegree_UDACITY/Projet1_Bananas.git
pushd Projet1_Bananas

# HACK: Modify requirements.txt to download torch==0.4.0 using the link provided below. Standard installation methods using pip or conda do not work for this specific version. Please note, this link is only compatible with Windows systems. For other versions or operating systems, visit PyTorch's previous versions page to find the appropriate download link.https://pytorch.org/get-started/previous-versions/
pip install https://download.pytorch.org/whl/cpu/torch-0.4.0-cp36-cp36m-win_amd64.whl

# Consider updating the file path for unityagents in your requirements.txt file, which was originally cloned from Udacity. This adjustment will ensure that the correct version of unityagents is referenced, matching the specific needs of your project.
pip install -r requirements.txt

# Create an IPython kernel for the DRL_udacity_cpu environment
python -m ipykernel install --user --name DRL_udacity_cpu --display-name "Python 3.6 (DRL_udacity_cpu)"

popd
pushd Projet1_Bananas
```

## Usage

In order to run the code, we run it straight via python instead of using jupyter notebooks.

As depicted in the Report.pdf, you can change the paramters in dqn_agent.py and main.py to get different results. Otherwise, you can run the code as-is to get the same results assuming a random seed = 0. 

```python
# run from 'udacity-agent-is-bananas' directory
python main.py
```

