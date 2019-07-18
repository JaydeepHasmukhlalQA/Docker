# How to use

## Building the image

To build the image. Use the command `docker build -t nameofimage .`

## Running the image

To run the image. Use the command `docker run -d -p 4200:4200 --name nameofprojectwhilerunning nameofimage`

This will run the image with the name of what you gave it, but also open the ports on 4200 in the container.

## Stopping the container

To stop the container do, `docker stop $(docker ps -qa)`

## Removing the containers

To remove the containers do, `docker rm $(docker ps -qa)`
