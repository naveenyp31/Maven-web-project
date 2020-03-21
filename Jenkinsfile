node{
    stage('code checkout')
    {
        git credentialsId: 'b3a120d4-9d56-4c69-b7b2-393491f49786', url: 'https://github.com/DevOps-Traning/Maven-web-project.git'
    }
    stage('maven')
    {
     def mvnHOME = tool name: 'windows-maven', type: 'maven'
     if (isUnix())
     {
         sh "${mvnHOME}/bin/mvn clean package"
     }
     else 
     {
       bat "${mvnHOME}/bin/mvn clean package"  
     }
    }
    stage('sonar')
    {
     def mvnHOME = tool name: 'windows-maven', type: 'maven'
     if (isUnix())
     {
         sh "${mvnHOME}/bin/mvn sonar:sonar"
     }
     else 
     {
       bat "${mvnHOME}/bin/mvn sonar:sonar"  
     }
    }
    stage('tomcat')
    {
        bat label: '', script: 'copy C:\\Users\\Nandihal\'s\\.jenkins\\workspace\\myfirstpipelinejob\\target\\*.war D:\\DevOpsTools\\apache-tomcat-9.0.12\\webapps\\'
    }
}
