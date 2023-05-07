
# Evaluating AWS Autoscaling group behavior on different metrics
This repository contains the implementation details of our project where we explored the functionality of AWS Autoscaling by simulating CPU loads on EC2 instances.

## Implementation Steps
To simulate CPU loads and test the effectiveness of AWS Autoscaling, we followed these steps:

- Deploying the CloudFormation templates in the order:
    Launch Template
    AWS Autoscaling group
    Scaling Policies
    Alarm
- After deploying the templates, we set the autoscaling group  instance count values as Max: 2, Min: 1 and Desired: 1.
- Accessed the instance through Secure Shell (SSH) using a key generated for the instance.
- Updated the instance using the command sudo apt-get update and installed Python 3 package manager (pip) using the command sudo apt-get install python3-pip.
- Cloned the CPULoadGenerator repository from Github using the command git clone https://github.com/GaetanoCarlucci/CPULoadGenerator.git. It's important to note that SSH cloning will not work unless you have set up SSH keys properly.
- Checked out the 'Python3' branch of the repository, which is recommended for higher versions of Python.
- Navigated to the CPULoadGenerator directory using the command cd CPULoadGenerator.
- Installed all the necessary dependencies for the scripts to execute using the command pip install -r requirements.txt. This ensured that all required dependencies were present and enabled us to execute the scripts.
- Simulated CPU loads on the instance by increasing and decreasing them at different paces, both steep and gradual, using the CPULoadGenerator scripts. This allowed us to test the effectiveness of the AWS Autoscaling service in automatically adjusting the capacity of the instance based on demand.
- Repeated the same process on a t3.micro instance in a different region where t3.micro is available for free, specifically in the Bahrain region. However, since the t3 instance family is built to handle occasional bursts of compute capacity by offering burstable performance that utilizes credits, the instances can manage heavy CPU workloads without experiencing failure or slowdown, even in the event of irregular workload spikes.

