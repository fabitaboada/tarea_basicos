# 1.
docker pull ubuntu:latest   -   comando para descargar la imagen
docker images    -   para comprobar que está decargada
# 2. 
docker run ubuntu    -   el contenedor no está arrancado
el nombre del contenedor es heuristic_merkle
# 3.
docker run -it --name ubu1 ubuntu bash    -  crear contenedor
docker -it exec ubu1  -  acceder a contenedor