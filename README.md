# pemplate
A template for creating projects with nbdev.

# Usage
After cloning the repo run:
> docker-compose --file nbdev-env/docker-compose.yml --project-directory . run setup


to initialize the project and then run:
> docker-compose --file nbdev-env/docker-compose.yml --project-directory . up

to launch jupyter lab and start developing.