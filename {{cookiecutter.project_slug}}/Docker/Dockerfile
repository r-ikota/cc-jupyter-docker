# Copyright Ryo Ikota
ARG BASE_CONTAINER={{cookiecutter.base_image}}:{{cookiecutter.tag_name}}
FROM $BASE_CONTAINER

USER root
RUN apt-get update \
 && apt-get install less
# COPY --chown=$NB_USER:$NB_GID <a file you want to copy> $HOME/ 
USER $NB_UID
ENV PYTHONPATH=$HOME/work
WORKDIR $HOME/work


CMD ["start-notebook.sh"]
