# Note that there must be a tag
FROM pangeo/pangeo-ocean:2019.03.12

# for testing purposes
RUN pip install git+https://github.com/jhamman/jhamman/dask-kubernetes.git@default_tolerations

# https://mybinder.readthedocs.io/en/latest/tutorials/dockerfile.html#preparing-your-dockerfile
ENV NB_USER jovyan
ENV NB_UID 1000
ENV HOME /home/${NB_USER}

COPY . ${HOME}
USER root
RUN chown -R ${NB_UID} ${HOME}
USER ${NB_USER}
