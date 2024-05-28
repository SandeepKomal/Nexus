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
#### you can acess the nexus on http://publicip of server :8081 

### Place these below script in the pom.xml file 

```
<distributionManagement>
  <repository>
    <id>maven-releases</id>
    <!-- CHANGE HERE by your team Nexus server -->
    <url>http://3.138.169.221:8081/repository/maven-releases/</url>
  </repository>
  <snapshotRepository>
    <id>maven-snapshots</id>
    <!-- CHANGE HERE by your team Nexus server -->
    <url>http://3.138.169.221:8081/repository/maven-releases/</url>
  </snapshotRepository>
</distributionManagement>
```

```
  <repository>
  <id>maven-releases</id>
  <name>maven-releases</name>
  <url>http://3.138.169.221:8081/repository/maven-releases/</url>
  </repository>
```


