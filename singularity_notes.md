# Build, Sign, and Push
cd ~/project_repos/singularity-rstudio
# sudo singularity build --force ~/container_images/singularity-rstudio.sif Singularity.3.6.0
singularity build --fakeroot ~/container_images/singularity-rstudio.3.6.1.sif Singularity.3.6.1
# singularity sign ~/container_images/singularity-rstudio.sif
singularity push -U ~/container_images/singularity-rstudio.3.6.1.sif library://granek/default/singularity-rstudio:3.6.1

# Run From Sylabs Cloud
singularity run library://granek/default/singularity-rstudio:3.6.0
