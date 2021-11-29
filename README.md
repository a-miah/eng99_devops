# DevOps Intro
## Development Environment 

- What is DevOps?

- Why DevOps

- 4 Pillars of DevOps

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
 