<font size="6">Bird song classification</font><br><br>

<font size="6"> Table of contents</font>

- [Installation and usage](#installation-and-usage)
- [The data](#the-data)
- [Usefull commands](#usefull-commands)

# Installation and usage

# The data

# Usefull commands

To use the repository, you will need to add images dataset (in DCOM or PNG format) in a folder `kaggle_dataset` at the root of the project.

We advise you to use the docker configuration, but if one prefers to work without it, you will need to install requirements with `pip3 install -r requirements.txt`.

Be carefull, the repository is built to give the possibility to use a GPU. If you don't have a GPU on your computer, please comment lines below _deploy_ in the docker-compose file or it won't work.

**Build the container**<br>

> `docker-compose build` <br>

**Up containers**<br>

> `docker-compose up -d` <br>

**Stop containers**<br>

> `docker-compose stop` <br>

**Open a shell inside the main container**<br>

> `docker-compose exec bird_song sh`

**Run jupyter lab from the container**<br>

> `jupyter lab --ip 0.0.0.0 --allow-root`

**If some issues with jupyter lab or port already on used on 8888**

> `lsof -i :8888` <br> > `kill -9 <PID>` <br>
> With PID being the process ID of python (for notebook)
