In the current repository we have custom nginx configuration used to build our custom nginx image from the base image.
- default.conf   : This is the default configuration listening on port 80.
- gzip.conf      : This configuration file will provide content or mime type compression capabilities to fasten content rendering.
- secconfig.conf : This configuration file will provide all the secure configuration to harden the nginx server when exposed to the internet.

Building the custom nginx image
-------------------------------
docker build -t nginx_webserver -f ./Dockerfile_Nginx .

Run the custom nginx image
-------------------------
docker run -dit -p80:80 --name nginx_webserver nginx_webserver
