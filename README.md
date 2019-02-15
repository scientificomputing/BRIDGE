# BRIDGE 
**:bridge_at_night: Biomolecular Reaction and Interaction Dynamics Global Environment**

# What is BRIDGE  ? 
**BRIDGE** developed on the [Galaxy platform](https://usegalaxy.org/) makes possible fundamental molecular dynamics of proteins through workflows and pipelines via commonly used packages such as [NAMD](https://www.ks.uiuc.edu/Research/namd/), [GROMACS](http://www.gromacs.org/) and [CHARMM](https://www.charmm.org/charmm/). **BRIDGE** can be used to set up and simulate biological macromolecules, perform conformational analysis from trajectory data and conduct data analytics of large scale protein motions using statistical rigor.

# Availability


- **[BRIDGE tools and source code](https://github.com/galaxycomputationalchemistry/galaxy-tools-compchem)** :books: :wrench:
  - First developed at the [Scientific Computing Research Unit](http://www.scientificomputing.com/), the source code is developed and managed in collaboration with the [Galaxy computational chemistry team](https://github.com/galaxycomputationalchemistry) and is available [here](https://github.com/galaxycomputationalchemistry/galaxy-tools-compchem).
-  **[BRIDGE tools live on Galaxy](https://cheminformatics.usegalaxy.eu/)** :rocket::star:
   - In collaboration with [Björn Grüning](https://github.com/bgruening) and the [Galaxy computational chemistry team](https://github.com/galaxycomputationalchemistry), these tools are available on [Galaxy Europe](https://cheminformatics.usegalaxy.eu/) under the Chemical Toolbox section.
   - :computer: [Import the example history which contains output from a short molecular dynamics simulation of a fungal hydrolase (7CEL)](https://usegalaxy.eu/u/tsenapathi/h/example-md-dataset---cellulase) and then [analyse the trajectory using a bio3d inspired workflow  (includes PCA, RMSD and RMSF analysis)](https://usegalaxy.eu/u/tsenapathi/w/md-analysis-using-bio3d).
- **BRIDGE in a 'box'** :package:
	- Docker ready to pull (`docker pull scientificomputing/bridge; docker run -d -p 8080:80 --rm scientificomputing/bridge
`,  then browse to localhost:8080). [See here for more details on starting up a Docker.](https://github.com/bgruening/docker-galaxy-stable)
	- A Docker file ready to build, [see this repository](https://github.com/scientificomputing/BRIDGE_MD_share).
