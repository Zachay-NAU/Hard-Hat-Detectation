# Hard Hat Detectation

In this github, I will show you how to run the Hardhat Detectation with Jetson Nano.

Here are 2 ways to run this demo. 

**Method 1:** (for those who want to run the demo directally) Prepare a SD card larger than 16 GB and flash the image file into your device

**Method 2:** (for those who donnot want to waste time to download image and have access to google.com) Use command line to install dependencies

All the methods can let you fully experience Edge Impulse if you want to use your own account and project.

## Method 1

This is the system image file for Jetson nano created by SeeedStudio with necessary environment.

Everyone can download this file which is for personal study use only.

The whole tutorial of hard hat detectation can be learn from this link: https://wiki.seeedstudio.com/HardHat/#deploy-the-ml-model-through-linux-python-sdk

### Step 1. Downoad the image file

Click here to download the image file: https://drive.google.com/file/d/13rl93ZB3LOu0jbArKETDJ9V-N7MJw0uK/view?usp=sharing

### Step 2. Flash this image file into your SD card or Jetson Nano's eMMC

### Step 3. Log in with the username and password below:

    username:jetson-nano

    password:nvidia
    
### Step 4. Open the terminal and put in the command below:

    python3 hard_hat_detectation.py /home/seeedstudio/modelfile.eim
     
     
## Method 2

### Step 1. Install python3.7.5

    sudo apt-get update
    sudo apt install software-properties-common
    sudo add-apt-repository ppa:deadsnakes/ppa
    sudo apt install python3.7
    
    
Update python 3 point to python3.7

    sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.6 1
    sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.7 2
    sudo update-alternatives --config python3
    
Press **Enter** and choose **2**
    
### Step 2. Upgrage pip3
    
    python3 -m pip install --upgrade pip
    
### Step 3. Install some dependencies
    
    sudo pip3 install scikit-build
    sudo pip3 install cython
    
### Step 4. Install Linux Python SDK from Edge Impulse

Please follow this official link: https://docs.edgeimpulse.com/docs/linux-python-sdk
    
### Step 5. (Optional for those who want to use their own project and model) Deploy your Jetson to your project
    
Please follow this official link: https://docs.edgeimpulse.com/docs/nvidia-jetson-nano
    
### Step 6. Install the command line output plugin
    
    sudo apt install toilet
    
### Step 7. Download my modefile and python demo (```modelfile.eim``` ```hardhat_detectation.py``` ```device_patches.py```) and then run it with:
    
    python3 hard_hat_detectation.py /home/<your_device_name>/modelfile.eim
    
 PS: If you donnot want to use my model, you can download your own model to the location: ```/home/<your_device_name>```
    
    edge-impulse-linux-runner --download modelfile.eim
    
 then repeat the command ```python3 hard_hat_detectation.py /home/<your_device_name>/modelfile.eim```
    
 ## Have Fun !
    
    
