# pemplate
A template for creating projects with nbdev.

# Usage
## Setup
After cloning the repo:
> cd <repo-directory>
> mkdir nbdev-env/loper
> docker-compose --file nbdev-env/docker-compose.yml --project-directory . run setup

## Running
Run the below command to launch jupyter lab and start developing:
> docker-compose --file nbdev-env/docker-compose.yml --project-directory . up
