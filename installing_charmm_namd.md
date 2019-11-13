# Discussion on using BRIDGE with CHARMM / NAMD

There are several options - use the prebuilt image from DockerHub, build a Docker image yourself (using GitHub ), and we are investigating making the free CHARMM version available at [Galaxy CompChem ZA server on ilifu](https://galaxy-compchem.ilifu.ac.za/) (Work in Progress).

## 1. Use image from DockerHub

```
docker pull scientificomputing/bridge
docker run -d -p 8080:80 scientificomputing/bridge
```
Use `docker ps` and get the id of this BRIDGE docker, we'll refer to this as ${docker_id}. Whenever you see this use your id.

Login to the docker container
```
docker exec -it ${docker_id} /bin/bash
```
### CHARMM install
Copy your CHARMM source and compile it in the Docker (we have found executables compiled outside are an issue). 
Copy the CHARMM executable which must be called ```charmm``` to /galaxy-central/tools/bridge/executables/bin/CHARMM/. 

### NAMD install
This is made available by default by using the NAMD conda package and should be setup by default. If there are issues can you raise them at https://github.com/scientificomputing/bridge-docker/issues
It may take a while to be setup on the first instance the tool is called but will work quickly afterwards. 
# 2. Build image from GitHub source
- Clone: `git clone https://github.com/scientificomputing/bridge-docker.git`
- Setup executables: Copy into executables/bin/CHARMM or as needed, see below.
- Build: `docker build -t bridge .`
- Run: `docker run -d -p 8080:80 --rm bridge` # the --rm flag will automatically remove the container when it exits
- Use: Open in your web browser at http://localhost:8080

### CHARMM install
Copy the CHARMM executable which must be called ```charmm``` to executables/bin/CHARMM/. In the build phase it will be copied into the Docker container. 
If issues build your CHARMM in the Docker container, copy it out and then repeat the build. Alternatively share your Galaxy mountpoint with other compute resources via NFS and run CHARMM via a queueing system.

### NAMD install
This is made available by default by using the NAMD conda package and should be setup by default. If there are issues can you raise them at https://github.com/scientificomputing/bridge-docker/issues
It may take a while to be setup on the first instance the tool is called but will work quickly afterwards. 



# 3. Galaxy EU
[BRIDGE tools live on Galaxy](https://cheminformatics.usegalaxy.eu/)
NAMD and CHARMM are not available, however GROMACS is available as well as analysis tools (MDAnalysis, Bio3D, MDTraj, VMD hydrogen bonding etc.).

# 4. Use ilifu
[Overview of Galaxy CompChem ZA](https://galaxycomputationalchemistry.github.io/usegalaxy-za/), [Galaxy CompChem ZA server on ilifu](https://galaxy-compchem.ilifu.ac.za/)
This is a work in progress and we may have CHARMM available later this year.


