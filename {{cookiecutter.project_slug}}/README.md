# {{cookiecutter.project_name}}
{{cookiecutter.project_short_description}}

## License
BSD

## How to launch
You can launch a container with docker-compose or with the remote-container extension in VScode.

### docker-compose
To launch a container at the project root, 

    $ docker-compose up

To stop and remove the container,

    $ docker-compose down
    
To execute a shell,
    $ docker-compose exec python start.sh

If you have to run a command as a root,
    $ docker-compose exec --user root -e GRANT_SUDO=yes python start.sh

To destroy the container you launched,
    $ docker-compose down

### remote-container extension
Run VScode and type the following in the command pallet

     Remote-Containers: Open Folder in Container
     
Consult [the official document](https://code.visualstudio.com/docs/remote/containers) for details.

## Jupyter Notebook Container
For information on Jupyter Docker Stacks, consult the followings:
  * [Documentation on ReadTheDocs](https://jupyter-docker-stacks.readthedocs.io/en/latest/index.html)
  * [Repository on github](https://github.com/jupyter/docker-stacks)
  * [Jupyter on Docker Hub](https://hub.docker.com/u/jupyter/)
