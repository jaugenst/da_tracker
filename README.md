# da_tracker
Automated workflow for high throughput single cell and single phagosome tracking in infected cells

This workflow is intended to run on time-lapse, z-stacks, multi-channel images and on most image formats. 
It requires to install pyimagej (https://py.imagej.net/en/latest/ , https://github.com/imagej/pyimagej) and Cellpose (https://github.com/MouseLand/cellpose). It is also recommended to install locally Fiji (https://imagej.net/software/fiji/downloads) and configure the updates websites to add Trackmate and the affiliated plugins such as Trackmate cellpose: https://imagej.net/plugins/trackmate/detectors/trackmate-cellpose.

This work was done in collaboration with Ashton T. Belew (https://github.com/abelew) and Anushka Poddar (https://github.com/apoddar76). 
It also derived from a more "by-hand" workflow we worked on: https://github.com/abelew/fiji_tracker

