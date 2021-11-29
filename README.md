# DevOps Intro
## Development Environment 

- Install Vagrant 
- Install Ruby

### What is DevOps?

Combination of processes, tools and methodologies to increase an organisations ability to deliver applications and services at greater speed and quality. Traditionally siloed teams in Development and Operations are brought together promoting more collaboration which leads to more greater quality and faster deliver. A set of practices are established to automate processes and build CI/CD pipelines. 

### Why DevOps

Greater collaboration between teams

Shorter development cycles meaning products/services are sent to production quicker

Automation optimises productivity and efficiency 

Greater focus on testing and maintenance leads to more reliable products

Greater value created for customers and businesses

### 4 Pillars of DevOps

- Communication

- Collaboration

- Automation

- Monitoring

### Risks

- Limited collaboration leading to longer cycles and release, less flexible to the market which can prove costly. Slower response to issues in production leading to products/services being offline longer


**Linux Commands**

- `sudo apt-get update -y`


# Common Linux Commands

- Who am I `uname - a` 
- Where am I `pwd`
- list dir or all `ls` or `ls -a`
- Copy file `cp filename destination`
- Cut or rename `mv filename destination`
- Create a file `touch filename`
- create a folder `mkdir foldername`
- how to navigate - `cd foldername` return step back `cd ..
- Deleting file folders `rm -rf foldername`



**File Permissions**
- Read `r`, Write `w` and `x`
- how to check permission `ll`
- change permission `chmod permission filename`

- find out all processes running `top`
- how to `kill` a process 

# Vagrant Commands
- `vagrant init` - creates a new vagrantfile in the directory
- `vagrant up` - will create and run the Virtual Machine
- `vagrant destroy` - will stop and destroy the VM (will need to reset to reuse)
- `vagrant reload` - will update the VM with anything new added (if it doesn't work do destroy then up)
- `vagrant ssh` - to get into the VM when it's running
- `vagrant status` - shows the status of VM (if it's running or not)
- `exit` - exits the VM
- `enter` - enters the VM
- `sudo su` - become admin and goes to root
- `systemctl status *package name*` - to see if installed properly
- `sudo systemctl restart *package name*` - if package doesn't run properly

# Setting up Virtual Machine

### 1. Create a Vagrantfile
With the below included in the file:
```
# Creating a virtual machine with Linux Ubuntu 16.04
# ubuntu/xenial64


This can be created in nano in bash or an IDE. Below is the content of the Vagrantfile

Vagrant.configure("2") do |config|


 # Choose the os/box/distro
 config.vm.box = "ubuntu/xenial64"
 config.vm.network "private_network", ip: "192.168.10.100"
 # vagrant destroy
 # vagrant up
 # vagrant reload

end

```

2. `vagrant up` (VirtualBox should now be running)
3. `vagrant status` - if everything worked above it should be running
4.  `vagrant ssh` - to go into the VM (name needs to be provided if using multiple machines)
5. `sudo apt-get update` - asks VM to connect to the internet and run updates
6. `sudo apt-get upgrade` - upgrades any missing packages
7. `sudo apt-get install nginx` - installs a web server
8. `systemctl status nginx` - checks if nginx is running 
9. Ensure you have selected an ip address to host your VM by including on Vagrantfile
10. `vagrant reload` if vagrantfile updated and then `vagrant ssh`



# Automate everything we have done manually

> vagrant up again

- 1. `touch` *filename.sh*
- 2. `nano` *filename.sh* - edit file as below:
```
#!/bin/bash
# update, upgrade, install nginx 

sudo apt-get update -y
sudo apt-get upgrade -y
sudo apt-get install nginx -y

```
- 3. ./*filename.sh* - runs file
- 4. `sudo chmod permission +x *filename.sh*` - if permission denied

# Pipes and Filters
A pipe can pass the standard output of one operation to the standard input of another, but a filter can modify the stream. A filter takes the standard input, does something useful with it, and then returns it as a standard output.

- Display first two lines in a file `cat file | head -2`
- Display last 2 lines in a file `cat file | tail -2`