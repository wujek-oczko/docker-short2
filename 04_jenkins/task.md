# Jenkins and autodeploy

- run Jenkins
```docker run -d -u root --name jenkins \
    -p 8080:8080 -p 50000:50000 \
    -v jenkins:/var/jenkins_home \
    -v /var/run/docker.sock:/var/run/docker.sock \
    jenkins/jenkins:alpine
```

- get jenkins password
```
docker exec -it jenkins cat /var/jenkins_home/secrets/initialAdminPassword
```

