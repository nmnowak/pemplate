# pemplate
A template for creating projects with nbdev.

# Usage
## Setup
After cloning the repo:
1. cd *repo-directory*
2. mkdir nbdev-env/loper
3. docker-compose --file nbdev-env/docker-compose.yml --project-directory . run setup

## Running
Run the below command to launch jupyter lab and start developing:
- docker-compose --file nbdev-env/docker-compose.yml --project-directory . up
