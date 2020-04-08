Docker is a kind of jail that is doing its job on top of the kernel. So in a VM the kernel is of its own but in the docker the kernel is shared

Docker isolates the processing of nodes in their own environment. So u will see that in every docker only one process with very limited number of processes which are required to run the process the docker is build for.

Docker will be loaded as an image in your system. Every docker image will be then ran to create the container. So container can be treated as a running instance of docker.

To execute a docker creation process using the file
docker build --tag vssm-gx-builder -f ./Dockerfile .

To pull a docker from repository inside a docker file
FROM docker.adtran.com:5000/mosaic-os-service-kit-debian8:latest

To login to an already running container
docker exec -it <container ID> bash

Option to mount your system directory to the docker
-v /home/adtran/StackCodebase/test/:/root/package/:rw


To remove all the docker containers
docker rm $(docker ps -a -q)

To start a docker container
sudo docker run -it <contatiner id> /bin/bash


Configuration file for setting up the docker inside the centos VM
/etc/sysconfig/docker
add option
OPTIONS='--selinux-enabled --log-driver=journald --signature-verification=false --dns 8.8.8.8 --insecure-registry cn-docker.adtran.com:5000'


Docker also makes sure that the various people are using the same build environment and the automated systems like the jenkins is also using the same build environment.


There is a problem that we are trying to figure out. In this the diameteer libraries are build in the debian environment and when we are trying to link it on the alpine docker the problem is comming that the symbols internal to the diamter stack so files are not getting resolved. This happened because the alpine docker is making use of the muscl c++. the standard glibc compatible libraries are not available in the alpine and the


sudo docker run -v /home/adtran/StackCodebase/test/:/root/package/:rw -it <contatiner id> /bin/bash

docker cp <containerId>:/file/path/within/container /host/path/target



docker exec -it dfn sh -c "/usr/bin/supervisorctl start DFN"  This is the command to execute the DFN inside the docker when it is already running. This will run the command inside that docker and then it will come out.

 docker start
docker stop
docker exec –it <container name> bash