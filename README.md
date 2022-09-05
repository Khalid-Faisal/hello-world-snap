# hello-world-snap

Demonstration of a creating a snap

## Description
This repository is for completely beginner in ubuntu core, IoT, snapcraft world. This repo demonstrate the basicHello World snap.

## Steps
```
ubuntu@khalid:UbuntuCore$ mkdir hello-world
ubuntu@khalid:UbuntuCore$ sudo chmod -R 777 hello-world
ubuntu@khalid:UbuntuCore$ cd hello-world
ubuntu@khalid:hello-world$ sudo lxc exec <Linux-container-name> -- su ubuntu  #LXC is a ubuntu container
ubuntu@ubuntu20:/root$ cd
ubuntu@ubuntu20:~$ cd hello-world
ubuntu@ubuntu20:~hello-world$ snapcraft init
Created snap/snapcraft.yaml.
Go to https://docs.snapcraft.io/the-snapcraft-format/8337 for more information about the snapcraft.yaml format.
ubuntu@ubuntu20:~hello-world$ vi snap/snapcraft.yaml 
ubuntu@ubuntu20:~hello-world$ vi hello.sh
ubuntu@ubuntu20:~hello-world$ sudo chmod +x hello.sh 
ubuntu@ubuntu20:~hello-world$ snapcraft --destructive-mode
Pulling hello 
+ snapcraftctl pull
Building hello 
+ snapcraftctl build
+ cp --archive --link --no-dereference . /home/ubuntu/hello-world/parts/hello/install
Staging hello 
+ snapcraftctl stage
Priming hello 
+ snapcraftctl prime
Snapping |                                                                                               
Snapped hello-world-snap\_0.1\_amd64.snap
ubuntu@ubuntu20:~/hello-world$ sudo snap install hello-world-snap\_0.1\_amd64.snap --devmode --dangerous
hello-world-snap 0.1 installed
ubuntu@ubuntu20:~/hello-world$ hello-world-snap.hello 
**Hello World!!**
ubuntu@ubuntu20:~/hello-world$ sudo snap remove hello-world-snap 
hello-world-snap removed
```
