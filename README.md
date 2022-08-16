# Vagrant + Docker-compose with LEMP & WordPress

Hello Everyone! I created a Docker-compose file with LEMP and WordPress as well as a VagrantFile that already has Docker and Docker-compose installed.

- 3 Containers for LEMP-Wordpress (MySQL, WordPress+PHP-FPM, Nginx)
- 2 Volumes (MySQL, WordPress)
- 1 Network (wp-net)

If you are new to Docker check out the docker [documentation](https://docs.docker.com/) for more information.

## Requirements
- [Vagrant](https://www.vagrantup.com/downloads)
- Virtual Machine ([Oracle VBox](https://www.virtualbox.org/wiki/Downloads) or [VMware](https://www.vmware.com/in/products/workstation-pro/workstation-pro-evaluation.html))
- [Docker](https://docs.docker.com/get-docker/)

> You can checkout [play with Docker](https://labs.play-with-docker.com/) which already has compose and docker installed. It is made of Alpine OS and has a terminal-like appearance. Since it is just used for educational purposes, you may use the 4 hours of the session without any additional installation.

## Usage

I created two types of VagrantFile
- [VagrantFile](https://github.com/sarath-pm/Vagrant-DockerCompose-LEMP-Wordpress/tree/main/VagarantFile%20to%20Install%20Docker) ---> Ready to use VagrantFile with Wordpresss and LEMP containers deployed.
- [VagrantFile](https://github.com/sarath-pm/Vagrant-DockerCompose-LEMP-Wordpress/tree/main/VagrantFile%20to%20deploy%20wordpress%20%2B%20LEMP) ---> Docker installed and configured. We need to manually configure the Docker.


For manually docker deployment, follow the instructions below:

_Note: Ensure Docker is installed and configured before  running this command._

```sh
git clone https://github.com/sarath-pm/Vagrant-DockerCompose-LEMP-Wordpress.git
cd Vagrant-DockerCompose-LEMP-Wordpress
docker-compose up -d  # Create containers, network & volume ("-d"  running container in detached mode)
```
_please refer to this docker commands which you can see the installed container, network, volume details_
```sh
docker-compose ps         # List Process status (Please note that this command only works with the installation directory)
docker network ls         # List Network
docker volume ls          # List volume
docker-compose down -v    # Remove all containers & volumes using these commands (Please note that this command only works with the installation directory)
```
 

### Docker-Compose Command Cheat sheet
![Docker Command Cheat Sheet](https://i.ibb.co/D7LHWMx/docker-compose-cheat-sheet-ryan-prater.png)


## License
This project is [unlicensed](https://github.com/sarath-pm/Vagrant-DockerCompose-LEMP-Wordpress/blob/main/LICENSE)

## Author
[Sarath P M](sarath-pm.github.io)

## Connect With Me
<p align="center">
<a href="https://www.linkedin.com/in/sarath-p-m/" target="blank"><img align="center" src="https://i.pinimg.com/originals/de/b4/6f/deb46f02a59e3b3a2aa58fac16290d63.gif" alt="sarath-p-m" height="40" width="45" /></a>
&nbsp;<a href="https://dev.to/sarath_pm" target="blank"><img align="center" src="https://res.cloudinary.com/practicaldev/image/fetch/s--0UiMFgbU--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_66%2Cw_880/https://thepracticaldev.s3.amazonaws.com/i/0vbfzhjcsjs0u716x88o.gif" alt="sarath_pm" height="40" width="47" /></a>  
&nbsp;<a href="mailto:sarath.pm@outlook.com" target="blank"><img align="center" src="https://user-images.githubusercontent.com/86669668/171339003-ef5b5c96-eac8-478c-a9cc-318ca9477fce.gif" alt="sarath.pm@outlook.com" width="40" /></a>      
&nbsp;<a href="https://www.hackerrank.com/sarath_pm" target="blank"><img align="center" src="https://user-images.githubusercontent.com/86669668/171338019-50f8c8de-e1ac-4651-b2cf-1901eceb2e51.gif" alt="sarath_pm" height="40" width="45"></a>
&nbsp;<a href="https://stackoverflow.com/users/19234611" target="blank"><img align="center" src="https://user-images.githubusercontent.com/86669668/171333456-ac1d5e66-bd90-468b-a1bf-c030ba6a1fed.gif" alt="19234611" width="40" /></a>
</p> 
