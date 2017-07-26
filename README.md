# jenkins
To allow Docker based builds through a Docker running Jenkins Server

```
> docker run --rm -p 8080:8080 -p 4040:4040 -v /var/run/docker.sock:/var/run/docker.sock -v $PWD/jenkins_home:/var/jenkins_home logimethods/jenkins
```

```
> docker run --rm -p 8080:8080 -p 4040:4040 -v /var/run/docker.sock:/var/run/docker.sock -v $PWD/blueocean_home:/var/jenkins_home logimethods/blueocean
```

```
> docker build . -t docker-jenkins

> docker run --name=jenkins -p 8080:8080 -p 50000:50000 --restart always -v /var/run/docker.sock:/var/run/docker.sock -v /srv/jenkins:/var/jenkins_home docker-jenkins
