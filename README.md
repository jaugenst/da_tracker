# da_tracker
## Automated workflow for high throughput single cell and single phagosome tracking in infected cells. 
The material here is associated to the publication here: https://doi.org/10.1242/bio.060555

This workflow is intended to run on time-lapse, z-stacks, multi-channel images and on most image formats. 
It requires to install pyimagej (https://py.imagej.net/en/latest/ , https://github.com/imagej/pyimagej) and Cellpose (https://github.com/MouseLand/cellpose). It is also recommended to install locally Fiji (https://imagej.net/software/fiji/downloads) and configure the updates websites to add Trackmate and the affiliated plugins such as Trackmate cellpose: https://imagej.net/plugins/trackmate/detectors/trackmate-cellpose.

For a ready-to-use installation to run the notebook, a container is provider as a DEF file. This is used by the software singularity to build a container and will also run it. This will result in the opening of jupyter-lab, allowing to open the notebook as well. Running fiji in interactive mode should be working without any further installation. 
To run this container, the user must be using Linux or a VM running Linux. For windows users, to install linux as a subsystem, please follow these easy to follow instructions: https://learn.microsoft.com/en-us/windows/wsl/install
I would recommend to install Ubuntu 22.04 or 24.04. Once this is done, download and install singularity (file: singularity-ce_4.2.1-jammy_amd64.deb) from the release page here: https://github.com/sylabs/singularity/releases
The container file already build can be found here: incoming URL soon.
Download the da_tracker.def file from the container folder here, place it in the ubuntu VM (or use it directly if already using Linux) and type ```sudo singularity build da_tracker.sif da_tracker.def``` in the terminal, in the folder containing the file. This will create the container. To run it, type ```./da_tracker.sif``` in the terminal and this should attempt to open jupyter-lab in the browser. If working from a VM, use Ctrl + left click on the link starting with "http://localhost:8888/" displayed in the terminal to open jupyter-lab in your local browser.
To be able to link the container to the data you'd like to analyze, or to another notebook you created, start the container using the command ```singularity run --bind /path/to/the/data:/data da_tracker.sif```. This will create a directory called 'data' inside the container that will be bound the folder of your choice and will display its content. The data in the folder can be analyzed and written. 

This work was done in collaboration with Ashton T. Belew (https://github.com/abelew) and Anushka Poddar (https://github.com/apoddar76). 
It also derived from a more "by-hand" workflow we worked on: https://github.com/abelew/fiji_tracker

