node {
    stage('code checkout')
    {
        git credentialsId: 'a6e80d27-3557-4c7d-b8de-0108b302726a', url: 'https://github.com/DevOps-Traning/Maven-web-project.git'
    }
	stage('Maven')
	{
	bat 'mvn clean deploy'
	}
	stage('Nexus')
	{
	bat 'mvn sonar:sonar'
	}
}
