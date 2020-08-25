node
{
    stage("code checkout")
    {
       git credentialsId: '60cc77a0-54b9-4c9f-93d2-adee34ca800f', url: 'https://github.com/DevOps-Traning/Maven-web-project.git' 
    }
	stage("maven")
	{
	def mvnHOME = tool name: 'Windows-maven', type: 'maven'
	bat "${mvnHOME}/bin/mvn clean package"
	}
	stage("sonar")
	{
	def mvnHOME = tool name: 'Windows-maven', type: 'maven'
	bat "${mvnHOME}/bin/mvn sonar:sonar"
	}
		stage("Wildflydeployment")
	{
     bat label: '', script: 'copy C:\\Users\\Nandihal\'s\\.jenkins\\workspace\\myfirstpipelinejob\\target\\*.war D:\\DevOpsTools\\wildfly-14.0.1.Final\\standalone\\deployments\\'
	}
}
