# Copyright Ryo Ikota
ARG BASE_CONTAINER={{cookiecutter.base_image}}:{{cookiecutter.tag_name}}
FROM $BASE_CONTAINER

# USER root
# RUN apt-get update \
#  && apt-get install less
# COPY --chown=$NB_USER:$NB_GID <a file you want to copy> $HOME/ 
USER $NB_UID
COPY requirements-conda.txt /tmp/
RUN conda install --yes --file /tmp/requirements-conda.txt && \
    fix-permissions $CONDA_DIR && \
    fix-permissions /home/$NB_USER
WORKDIR $HOME/work/src

# Uncomment the following lines 
# if you want to give the sudo permission to jovyan
#
# USER root
# ENV GRANT_SUDO=yes

CMD ["start.sh", "jupyter", "notebook", "--port={{cookiecutter.jupyter_port}}"]

# Uncomment the following line
# if you want to launch Jupyter without token
# 
# CMD ["start.sh", "jupyter", "notebook", "--port={{cookiecutter.jupyter_port}}", "--NotebookApp.token=''"]
