# vicken-ghoubiguian.github.io

This project consists to create my personal online portfolio as a simple static website...

## Contents

1. [Introduction](#introduction)

2. [Deployment on a web server](#deployment_on_a_web_server)

3. [Deployment by Docker](#deployment_by_docker)...

	* [By the Dockerfile](#deployment_by_docker_dockerfile)
	* [By Docker Hub](#deployment_by_docker_docker_hub)

4. [How to consult my online portfolio](#consultation) ?

5. [Conclusion](#conclusion)

<a name="introduction"></a>
## Introduction

This project consists to develop my online portfolio.

So he will address itself to:

*
*
*
*
*

My online portfolio contains:

* **Presentation**: I introduce myself very briefly,
* **My achievements**: I present what i have done and especially those of which i am proud,
* **My skills**: I say what I can do,
* **My key words**: I present my values,
* **My career**: I present to you the different jobs that i exercised,
* **My training course**: I deliver my school path with my diplomas,
* **Spoken languages**: I tell which languages i speak with the level for each of them
* **My hobbies**: I present what I do in my free time,
* **Contact me**: I deliver all the secrets to call me or send me a message,
* **Thanks**: I thank those who advise me and support me in my process

<a name="deployment_on_a_web_server"></a>
## Deployment on a web server

<a name="deployment_by_docker"></a>
## Deployment by Docker...

You can also use Docker to deploy my online portfolio. There are 2 methods of deploying my online portfolio by Docker:

* by the Dockerfile of these project,
* by the pulled image on Docker hub

Both are exhibited here.

<a name="deployment_by_docker_dockerfile"></a>
### By the Dockerfile

A Dockerfile is available in the project root, and you can consult it [here](https://github.com/Vicken-Ghoubiguian/vicken-ghoubiguian.github.io/blob/master/Dockerfile). To deploy this web app by the Dockerfile, please follow these commands in order:

```bash
# Cloning the the 'vicken-ghoubiguian.github.io' project from GitHub...
git clone https://github.com/Vicken-Ghoubiguian/vicken-ghoubiguian.github.io

# Placing in the 'vicken-ghoubiguian.github.io' GitHub project's folder...
cd vicken-ghoubiguian.github.io

# Creating the 'vicken-ghoubiguian.github.io' Docker image...
docker build . -t vicken-ghoubiguian.github.io:latest

# Running the 'vicken-ghoubiguian.github.io' Docker image as a Docker container to deploy this portfolio online...
docker container run -d --name vicken-ghoubiguian.github.io -p 80:80 vicken-ghoubiguian.github.io:latest

# Checking the IP address of the Docker container of the vicken-ghoubiguian.github.io application...
docker inspect --format='{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' vicken-ghoubiguian.github.io
```

Congratulations, now my online portfolio is working. To access this application, type the following address in the bar of your browser: [http://localhost/](http://localhost/).

<a name="deployment_by_docker_docker_hub"></a>
### By Docker Hub

A Docker image is available on Docker hub just [here](https://hub.docker.com/r/wicken/vicken-ghoubiguian.github.io). To deploy my online portfolio by the image on Docker hub, please follow these commands in order:

```bash
# Pulling the 'vicken-ghoubiguian.github.io' from Docker hub in the current machine...
docker pull wicken/vicken-ghoubiguian.github.io:latest

# Running the 'vicken-ghoubiguian.github.io' Docker image as a Docker container to deploy this portfolio online...
docker container run -d --name vicken-ghoubiguian.github.io -p 80:80 wicken/vicken-ghoubiguian.github.io:latest

# Checking the IP address of the Docker container of the vicken-ghoubiguian.github.io application...
docker inspect --format='{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' vicken-ghoubiguian.github.io
```

Congratulations, now my online portfolio is working. To access this application, type the following address in the bar of your browser: [http://localhost/](http://localhost/).

<a name='consultation'></a>
## How to consult my online portfolio ?

To consult my online portfolio, please [click here](https://vicken-ghoubiguian.github.io/).
You can also consult my online portfolio's Git repos and official Docker image respectively on:

* [GitHub](https://github.com/Vicken-Ghoubiguian/vicken-ghoubiguian.github.io),
* [Docker Hub](https://hub.docker.com/r/wicken/vicken-ghoubiguian.github.io)

So don't hesitate to take a look.

<a name='conclusion'></a>
## Conclusion
