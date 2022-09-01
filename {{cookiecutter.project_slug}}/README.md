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

    $ docker-compose exec jupyter start.sh

If you have to run a command as a root,

    $ docker-compose exec --user root -e GRANT_SUDO=yes jupyter start.sh

To destroy the container you launched,

    $ docker-compose down


### remote-container extension
Run VScode and type the following in the command pallet

     Remote-Containers: Open Folder in Container
     
Consult [the official document](https://code.visualstudio.com/docs/remote/containers) for details.

## back up and restore data volume

To back up the volume:

    $ docker run --rm --volumes-from <a container whoes volume will be backed up> -v $(PWD):/backup ubuntu tar cvf /backup/backup.tar /home/jovyan/data-volume

To restore the backup:

    $ docker run --rm --volumes-from <a container to which the data will be restored> -v $(pwd):/backup ubuntu bash -c "cd /home/jovyan/data-volume && tar xvf /backup/backup.tar --strip 3"

## Jupyter Notebook Container
For information on Jupyter Docker Stacks, consult the followings:
  * [Documentation on ReadTheDocs](https://jupyter-docker-stacks.readthedocs.io/en/latest/index.html)
  * [Repository on github](https://github.com/jupyter/docker-stacks)
  * [Jupyter on Docker Hub](https://hub.docker.com/u/jupyter/)

## VScode extensions
* [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
    * [github repository](https://github.com/Microsoft/vscode-python)
* [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)
    * [github repository](https://github.com/James-Yu/LaTeX-Workshop/)
* [HTML Preview](https://marketplace.visualstudio.com/items?itemName=tht13.html-preview-vscode)
    * [github repository](https://github.com/tht13/html-preview-vscode)

## Docker
* [Document](https://docs.docker.com/)