# Devops-task
Ansmake Technologies LLP
```bash
1. Create a network interface for flask and Nginx Application
   Command => docker network create flask_nginx
2. Move inside the flask dir and build the image for flask app
   Command => docker build -t flask_app .
3. Similarly move inside the nginx dir and build the nginx app
   Command => docker build -t nginx_app .
4. Finally we need to start both the container 
   Command => 1. docker run -d -p 5000:5000 --name flask_app --network flask_nginx flask_app 
              2. docker run -d -p 5001:80 --name nginx_app --network flask_nginx nginx_app
5. In browser just hit => http://localhost:5001 

```
#### Note
> To connect the flask_app to nginx_app we need to create a bridge network <br />
> ENV can be modify for `FLASK_APP_HOST` inside nginx Dockerfile but it should be = flask app name ( while launching ) 
