
# 23 -Sep  
## Docker machine :  
They are the docker engine running in the host
### To list them  
docker-machine ls  
### To create a new  
docker-machine create <new-machine-name>
docker-machine create sgfirst  
### Other  
docker-machine --help  

### To Change default
eval $("C:\Program Files\Docker Toolbox\docker-machine.exe" env <new-machine-name>)  
Eg:
eval $("C:\Program Files\Docker Toolbox\docker-machine.exe" env sgfirst)  

### To check Configuration
docker-machine env sgfirst  

## Docker Client
### To load the image from local tar file
docker load image_name

### To Save image as tar file
docker save image_name

## To get into the os 
docker container attach <container-id>


## Mounts
Types:  
&nbsp;&nbsp;&nbsp;&nbsp;Volume  - Space maintained by Docker by creating inside docker  
&nbsp;&nbsp;&nbsp;&nbsp;Bind  - connecting docker machine host file system to container  
&nbsp;&nbsp;&nbsp;&nbsp;Temporary File System - tmpfs - To store on memory  

NAS path is mounted to docker-container system which is then mounted to container through "bind"  

### Bind
To login into docker machine   
docker-machine ssh sgfirst  

Create a image and mount the above to it  
docker run -it --name bind_test --mount type=bind,source=/storage,target=/data ubuntu /bin/bash  
