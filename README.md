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

Use docker exec -it <container_name> /bin/bash to enter and interact with your running container.

docker logs <nginxcon1> container name
is used to view the output (logs) from a running or stopped Docker container — in this case, the container named nginxcon1.

This includes:

Web server access logs (like HTTP requests)

Error messages

Startup information

Console output from the app



# 🐳 Docker_Udemy

### Run a simple Apache (HTTPD) web server container

```bash
docker run --name nginxcon -d -p 8000:80 httpd
Then open your browser and go to:
👉 http://localhost:8000 — (note: not secure, just for local testing)

⚙️ Explanation
🔹 localhost
Refers to your own computer (the host machine). It’s a special hostname that maps to the IP address 127.0.0.1.

🔹 8000 (Host Port)
Represents the “door” on your computer used to access the containerized app.

🔹 Inside the Container
Inside the container, Apache (or Node) listens on port 80, which is another “door” — but this one exists inside the container.

🔹 -p 8000:80
Maps host port 8000 → container port 80
So, when you visit localhost:8000, Docker forwards your request to port 80 inside the container.

🧩 Summary:
A port number is simply a logical endpoint on a device that allows network communication.

🌐 Running the Apache Server
This container runs an Apache web server listening on port 80 inside the container.

Example 2 — Interactive Container
bash
Copy code
docker run --name container -it -d -p 8080:80 httpd
Explanation of Flags
Flag	Meaning	Purpose
-i	Interactive	Keeps STDIN (keyboard input) open, even if not attached
-t	TTY (teletype terminal)	Allocates a terminal interface so you can interact with the container like a shell

🧠 Accessing the Running Container
To open a shell inside the container:

bash
Copy code
docker exec -it <container_name> /bin/bash
Example:

bash
Copy code
docker exec -it nginxcon /bin/bash
This lets you enter and interact with the running container’s terminal.

🪵 Viewing Container Logs
To view the logs (output) of a running or stopped container:

bash
Copy code
docker logs <container_name>
Example:

bash
Copy code
docker logs nginxcon1
You’ll see logs such as:

Web server access logs (HTTP requests)

Error messages

Startup information

Console output from the app

✅ In summary:
Docker makes it easy to run, manage, and inspect web servers in isolated containers — mapping ports, running interactively, and viewing logs as needed.

yaml
Copy code

---

Would you like me to format it with a **table of contents** and **section links** (like GitHub’s clickable headers)?






You said:
make it short



ChatGPT said:
Sure — here’s a short and clean version of your README.md:

markdown
Copy code
# 🐳 Docker_Udemy

## Run Apache (HTTPD) Web Server
```bash
docker run --name nginxcon -d -p 8000:80 httpd
Access in browser: http://localhost:8000

Explanation
localhost → your computer (host)

8000 → host port (door to container)

80 → container port (Apache listens here)

-p 8000:80 → maps host port 8000 → container port 80

Interactive Container Example
bash
Copy code
docker run --name container -it -d -p 8080:80 httpd
Flag	Meaning	Purpose
-i	Interactive	Keeps input open
-t	TTY	Allocates a terminal

Access Container
bash
Copy code
docker exec -it <container_name> /bin/bash




