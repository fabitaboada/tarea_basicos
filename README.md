# 1.
docker pull ubuntu:latest   -   comando para descargar la imagen
docker images    -   para comprobar que está decargada
# 2. 
docker run ubuntu    -   el contenedor no está arrancado
el nombre del contenedor es heuristic_merkle
# 3.
docker run -it --name ubu1 ubuntu bash    -  crear contenedor
docker -it exec ubu1  -  acceder a contenedor
# 4.
instalamos las herramientas necesarias con los siguientes comandos:
sudo apt update
sudo apt-get install net-tools
sudo apt-get update && sudo apt-get install -y iputils-ping
comprobamos la ip con el comando: 
ifconfig
obtenemos: inet 172.17.0.1  netmask 255.255.0.0  broadcast 172.17.255.255
para realizar el ping escribimos:
ping google.com
# 5.
docker run -it --name ubu2 ubuntu bash   -  creamos contenedor
con ifconfig vemos la ip de ubu2
con el comando ping 172.17.0.3 hacemos ping de ubu1 a ubu2
# 6. 
Se cierra, pero no se borra el contenedor.
# 7. + 8.
docker stats para obtener la siguiente información:
0e7f14a3d5d0   ubu2      0.00%     880KiB / 15.61GiB   0.01%     2.91kB / 0B   123kB / 0B    1
b2b269696057   ubu1      0.00%     904KiB / 15.61GiB   0.01%     2.54kB / 0B   8.19kB / 0B   1