# first-mission

# Installing ROS Noetic on Ubuntu 20.04 Using VirtualBox

first,  i set up a virtual machine using VirtualBox and installed ROS Noetic on Ubuntu 20.04.

## Step 1: Download and Install VirtualBox

1. **Download VirtualBox:**
   - I went to the [VirtualBox website](https://www.virtualbox.org/).
   - Navigate to the "Downloads" section.
   - and Choose the version for my operating system (Windows).
## Step 2: Download and Install Ubuntu 20.04

1. **Download Ubuntu 20.04:**
   - I went to the [Ubuntu website](https://ubuntu.com/download/desktop).
   - Then Download the Ubuntu 20.04 LTS ISO file.

2. **Create a New Virtual Machine:**
   - After downloading Ubuntu, I opened VirtualBox and clicked "New" to create a new virtual machine.
   - Named my virtual machine ("Ubuntu").
   - Set the Type to "Linux" and Version to "Ubuntu (64-bit)".
   - Allocate memory (RAM) to the virtual machine (at least 2048 MB recommended).
   - Create a new virtual hard disk (VDI) and allocate at least 25 GB of storage.

4. **Install Ubuntu 20.04:**
   - Started the virtual machine and selected the Ubuntu 20.04 ISO file as the startup disk.
   - then I Followed the installation process to install Ubuntu 20.04 on the virtual machine.
   - Once the installation was completed, I restarted the virtual machine and logged in to Ubuntu.

# Installing ROS Noetic on Ubuntu 20.04 Using VirtualBox

1. *Set Up Your Sources:*

   I opened a terminal in my Ubuntu VM and ran these commands :
  * Setup my sources.list*


   Setup my computer to accept software from packages.ros.org.
   

[sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list']

   

3. *Set up my keys*

[sudo apt install curl # if you haven't already installed curl]
[curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -]



   
   

   

4. *Install ROS Noetic:*

   I updated my package list again:

   
   [sudo apt update]
   

   And installed the ROS Noetic desktop-install version:

   [sudo apt install ros-noetic-desktop]
   

   

5. *Set Up Your Environment:*

   I added ROS environment variables to my bash session:

   sh
   echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
   source ~/.bashrc
   

6. *Install Dependencies for Building Packages:*

   Finally, I installed some commonly used dependencies:

   sh
   sudo apt install python3-rosinstall python3-rosinstall-generator python3-wstool build-essential
   

## Step 4: Verify Your Installation

Lastly, I made sure everything was working correctly.

1. *Test Your Installation:*

   I opened a new terminal and ran:


   roscore
   
<img width="959" alt="ros" src="https://github.com/user-attachments/assets/3dfd9244-6ee8-4cf5-a6f3-a6cdd528766d">

   
  
