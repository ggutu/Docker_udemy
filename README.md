# Docker_udemy

 docker run --name nginxcon -d -p 8000:80 httpd
 To acess on web browser
 
 Explain
   ======================================================
localhost (IP address) → identifies your computer (the host).

8000 (host port) → the “door” on your computer to access the container.

Inside the container, Node listens on port 80 — another “door” for the app service.
===================================
-p 8000:80 → Map host port 8000 → container port 80
port number is logical endpoint on device.
This container apache webserver runinig on port 80



