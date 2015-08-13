Docker-Teamcity-Agent
=====================

You can build your TeamCity Agent with the following command : 

```
docker build -t davinkevin/docker-teamcity-agent https://github.com/davinkevin/docker-teamcity-agent.git
docker run -dt --link NAME_OF_YOUR_TEAMCITY_CONTAINER:teamcity --name teamcity-agent davinkevin/docker-teamcity-agent
```

For example, with a container named teamcity : 
```
docker run -dt --link teamcity:teamcity --name teamcity-agent davinkevin/docker-teamcity-agent
```

Mandatory parameters : 
* Your TeamCity Container have to run under the port 8080 in this container (not the mapped port)
