# DevOps Intro
## Development Environment 

- What is DevOps?

Combination of processes, tools and methodologies to increase an organisations ability to deliver applications and services at greater speed and quality. Traditionally siloed teams in Development and Operations are brought together promoting more collaboration which leads to more greater quality and faster deliver. A set of practices are established to automate processes and build CI/CD pipelines. 

- Why DevOps

Greater collaboration between teams

Shorter development cycles meaning products/services are sent to production quicker

Automation optimises productivity and efficiency 

Greater focus on testing and maintenance leads to more reliable products

Greater value created for customers and businesses

- 4 Pillars of DevOps

Communication

Collaboration

Automation

Monitoring

- Risks


**Linux Commands**

- `sudo apt-get update -y`

```
# Creating a virtual machine with Linux Ubuntu 16.04
# ubuntu/xenial64

Vagrant.configure("2") do |config|


 # Choose the os/box/distro
 config.vm.box = "ubuntu/xenial64"
 config.vm.network "private_network", ip: "192.168.10.100"
 # vagrant destroy
 # vagrant up
 # vagrant reload

end

```

- Who am I `uname - a` 
- Where am I `pwd`
- list dir or all `ls` or `ls -a`
- Copy file `cp filename destination`
- Cut or rename `mv filename destination`
- Create a file `touch filename`
- create a folder `mkdir foldername`
- how to navigate - `cd foldername` return step back `cd ..
- Deleting file folders `rm -rf foldername`

> Task: create a folder called test, create a file called text.txt inside the text folder then copy the text.txt to your home location `/home/vagrant`

**File Permissions**
- Read `r`, Write `w` and `x`
- how to check permission `ll`
- change permission `chmod permission filename`

- find out all processes running `top`
- how to `kill` a process 


### Automate everything we have done manually
- provision the steps for updating, upgrading and nginx

> vagrant up again
- redo all the steps
- install nginx and load it in the browser


# Pipes and Filters
A pipe can pass the standard output of one operation to the standard input of another, but a filter can modify the stream. A filter takes the standard input, does something useful with it, and then returns it as a standard output.

- Display first two lines in a file `cat file | head -2`
- Display last 2 lines in a file `cat file | tail -2`