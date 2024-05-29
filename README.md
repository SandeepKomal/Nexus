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
#### you can acess the nexus on " http://publicip of server :8081 "

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

##### note : replace the url with the specific url ine above scripts


![nexus](https://github.com/SandeepKomal/Nexus/assets/99358567/ac0ac6ab-c62b-472f-a32d-1fe4d5b6bed6)

![nx2](https://github.com/SandeepKomal/Nexus/assets/99358567/4fd80cc8-2779-4588-8146-2fab86b5c3ed)

![nx3](https://github.com/SandeepKomal/Nexus/assets/99358567/6b274120-31fc-42e7-897f-f3cffe382d1b)

![nx4](https://github.com/SandeepKomal/Nexus/assets/99358567/adc4d5e1-ab80-482c-a368-74f441a0d5d2)

![nx5](https://github.com/SandeepKomal/Nexus/assets/99358567/1123fd9e-0387-4584-be3b-d8b60956dbeb)

![nx6](https://github.com/SandeepKomal/Nexus/assets/99358567/2ce0289b-d77d-4b4c-8861-8c2ff6f529e5)

![nx7](https://github.com/SandeepKomal/Nexus/assets/99358567/5d4c6464-57da-4248-8372-9cc10bdf7e25)

![nx8](https://github.com/SandeepKomal/Nexus/assets/99358567/047cc4f5-115d-44b9-a7d5-a87bc7d019ff)
