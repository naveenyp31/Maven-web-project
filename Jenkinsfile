node
{
    stage("code Checkout")
    {
      git credentialsId: 'a7ab2b21-67cb-43aa-8113-7466bb3bf4fc', url: 'https://github.com/DevOps-Traning/Maven-web-project.git'  
    }
    stage("Maven")
    {
        def mvnHOME = tool name: 'Windows-Maven', type: 'maven'
        bat "${mvnHOME}/bin/mvn clean deploy"
    }
    stage("deployment")
    {
     bat label: '', script: 'copy C:\\Users\\Nandihal\'s\\.jenkins\\workspace\\myfirstpipelinejob\\target\\*.war D:\\DevOpsTools\\apache-tomcat-9.0.12\\webapps'   
    }
}
