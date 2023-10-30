docker -v   				<< Version pata chalta h
docker --version 			<< Same version pata chalta h
docker pull {image_name}
docker ps    				<<Kitna container run ho rha h
docker ps -a				<< Sab dikhta h running + Stop
docker stop {container_id or container_name}
docker rm {container_name}		<< Remove container
docker rmi {image_name}
docker images				<< Kitna image h pata chalta h
docker exec -it {container_name}

docker run {image_name}			<< attach mode
docker run -d {image_name}		<< detach mode, dikhega nhi
docker attach {container_id}

docker rm {multiple_id with space}
docker run nginix:latest		<< tags of the Version
docker run -it {image_name}		<< interactiv mode is mei terminal h=bhi open hota ho
docker run -p 80:5000			<< idhr 80 jisko map krna h aur 5000 dckr cntr ka


vi /root/app_name/Dockerfile    << To see thee Docker file

Build a Docker file.

docker build -t myapp .

docker run python:3.6 cat /etc/*release*        << To get the os of the image

## Docker Inspect

docker inspect <container-name> | grep -A 10 Env

docker run -p 38282:8080 --name blue-app -e APP_COLOR=blue -d kodekloud/simple-webapp

docker run -d --name=clickcounter --link redis:redis -p 8085:5000 kodekloud/click-counter