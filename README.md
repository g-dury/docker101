#Docker 101

## Docker theory

* What is Docker ?
* [https://www.docker.com/resources/what-container] (https://www.docker.com/resources/what-container)
* Notions:
	* container
	* image
	* registry
	* Dockerfile

## Docker practice

Install docker on your machine

Use my repository: [https://github.com/g-dury/docker101] (https://github.com/g-dury/docker101)

Latest Docker version: 18.09.2

1. Build a docker image helloworld
	* FROM (choose from docker hub)
	* ADD
	* RUN
	* and then CMD/ENTRYPOINT
	* go into the `helloworld` folder
	* `docker build -t helloworld:1 .`

2. Launch a hello world service with docker

	* Know your docker commands:
		* `docker ps -a`
		* `docker pull` 
		* `docker run -d --name=hello helloworld:1`
		* `docker logs -f <CONTAINER>`
		* `docker stop`
		* `docker rm -f <CONTAINER>`

3. How to expose a container to the host

	* Use the -p argument
	* Understand the network notions of docker:
		* bridge
		* host
		* others

4. Make two containers communicate with each other

	* launch a mongodb docker container [https://hub.docker.com/_/mongo] (https://hub.docker.com/_/mongo)
	* use another docker container to write to it and detail the network configuration you used

5. Make data of docker container persistent: volumes
