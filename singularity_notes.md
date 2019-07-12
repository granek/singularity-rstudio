# Build, Sign, and Push
cd ~/project_repos/singularity-rstudio
sudo singularity build --force ~/container_images/singularity-rstudio.sif Singularity.3.6.0
singularity sign ~/container_images/singularity-rstudio.sif
singularity push ~/container_images/singularity-rstudio.sif library://granek/default/singularity-rstudio:3.6.0

# Run From Sylabs Cloud
singularity run library://granek/default/singularity-rstudio:3.6.0
