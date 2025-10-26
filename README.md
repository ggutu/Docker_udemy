# Docker_udemy

 docker run --name nginxcon -d -p 8000:80 httpd
 
 To acess on web browser
 http://localhost:8000  ----> which is not secure -

 
 Explain
   ======================================================
localhost (IP address) → identifies your computer (the host).

8000 (host port) → the “door” on your computer to access the container.

Inside the container, Node listens on port 80 — another “door” for the app service.
===================================
-p 8000:80 → Map host port 8000 → container port 80

port number is logical endpoint on device.

This container  Apache web server runinig on port 80

docker run --name container -it -d -p 8080:80 httpd ,only explain -it
============================
Flag	Meaning	Purpose
-i	Interactive	Keeps STDIN (keyboard input) open, even if not attached.

-t	TTY (teletype terminal)	Allocates a terminal interface so you can interact with the container like a shell.

docker run --name <contpd> -it -d -p 8033:80 httpd

Use docker exec -it <container_name> /bin/bash to enter and interact with your running container.
   /usr/local/apache2/htdocs#
  Change file index.html and refresh browser.
    2  cd htdocs   then install apt update then install vim or nano
    3  ls
    4  vim index.html
    5  apt update && apt install -y vim 
    7  vim index.html

docker logs <nginxcon1> container name
is used to view the output (logs) from a running or stopped Docker container — in this case, the container named nginxcon1.

This includes:

Web server access logs (like HTTP requests)

Error messages

Startup information

Console output from the app












