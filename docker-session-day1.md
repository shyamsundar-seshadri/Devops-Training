
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
eval $("C:\Program Files\Docker Toolbox\docker-machine.exe" env sgfirst)  
