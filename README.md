# KassiopeiaBinder
Repository to use MyBinder with the pre-built Kassiopeia images.

Kassiopeia is a package for electric and magnetic field calculation and particle tracking. Here is the main repository: https://github.com/KATRIN-Experiment/Kassiopeia .

## Explanation

Binder always builds Dockerfiles from scratch. Waiting for Kassiopeia to compile takes too long, so we use pre-built images instead. That requires a second (this) repository which contains the glue code in form of a `Dockerfile` that just uses our pre-built images as base image.

The `Dockerfile` is automatically updated by a GitHub Action that runs every half an hour and checks for changes. 

This has also been discussed here: https://discourse.jupyter.org/t/use-published-docker-image-for-binder/10333  
There also exists an open issue for a simpler solution: https://github.com/jupyterhub/binderhub/issues/1298
