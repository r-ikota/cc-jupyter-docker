# {{cookiecutter.project_name}}
{{cookiecutter.project_short_description}}

## License
BSD


## Docker
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

## Jupyter Notebook Container
For information on Jupyter Docker Stacks, consult the followings:
  * [Documentation on ReadTheDocs](https://jupyter-docker-stacks.readthedocs.io/en/latest/index.html)
  * [Repository on github](https://github.com/jupyter/docker-stacks)
  * [Jupyter on Docker Hub](https://hub.docker.com/u/jupyter/)
