# mvn-jfrog-setup

1. create a simple maven project 

mvn archetype:generate -DgroupId=com.mycompany.app -DartifactId=my-app -DarchetypeArtifactId=maven-archetype-quickstart -DarchetypeVersion=1.4 -DinteractiveMode=false

cd my-app

mvn clean package 

<code>
java -jar my-app-1.0-SNAPSHOT.jar

output:  Hello World!
<code>
 
 
publish artifact to jfro
https://medium.com/@anusha.sharma3010/integrating-jenkins-with-artifactory-6d18974d163d
add maven-deploy-plugin

mvn clean package deploy 


<code>
   
output:
Uploading to snapshots: http://localhost:8081/artifactory/libs-snapshot/com/mycompany/app/my-app/1.0-SNAPSHOT/my-app-1.0-20190621.162258-8.jar
   
Uploaded to snapshots: http://localhost:8081/artifactory/libs-snapshot/com/mycompany/app/my-app/1.0-SNAPSHOT/my-app-1.0-20190621.162258-8.jar (2.6 kB at 841 B/s)

Uploading to snapshots: http://localhost:8081/artifactory/libs-snapshot/com/mycompany/app/my-app/1.0-SNAPSHOT/my-app-1.0-20190621.162258-8.pom

Uploaded to snapshots: http://localhost:8081/artifactory/libs-snapshot/com/mycompany/app/my-app/1.0-SNAPSHOT/my-app-1.0-20190621.162258-8.pom (2.1 kB at 729 B/s)

<code>


<code>  
 mvn clean package sonar:sonar -Dsonar.host.url=http://localhost:9000    -Dsonar.login=XXXXXXXXXXXXXXXXXXX
<code>
