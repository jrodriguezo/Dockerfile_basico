# Dockerfile_basico

```dockerfile
		
    FROM ubuntu:18.04 
    RUN apt-get update
    RUN apt-get install apache2 -y 
    EXPOSE 80 
    CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]

    sudo docker build -t jesus/jesus .

    sudo docker run -d --name web -p 80:80 jesus/jesus
