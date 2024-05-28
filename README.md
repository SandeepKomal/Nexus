# Nexus Installation Using Docker 


```
docker pull nexus3
```
```
docker run -d -p 8081:8081 --name nexus sonatype/nexus3c
```
```
docker exec nexus cat /nexus-data/admin.password
```
### you can acess the nexus on http://publicip of ec2 :8081 
