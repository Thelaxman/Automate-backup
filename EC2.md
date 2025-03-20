# EC2 Instances
EC2 instances are virtual servers that run on AWS cloud. 

## Setting up EC2 Instances

- Launch instance uisng AMI
  - Has several options to choose from with Operating System such as:
    - Ubuntu, Windows, RHEL, Amazon Linux ,etc.
  - Each Instance can be launched using AMIs. You can create your own AMI or choose one from the AWS marketplace uisng Quick Start option.
  - Choose a preffered instance type from a list of available Instance types.
    - t2.micro, t2.small, t2.large, etc.
    - Each instance type comes with different CPU and memory.  
- Select the key pair if it exists or create a new one and save it locally.
- Select the network and subnet where you want to launch your virtual server.
- Select a Security group.
- Select the number of instances that you would like to launch with the configurations that you chose and then select "Launch Instance".
