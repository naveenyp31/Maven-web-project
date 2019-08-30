node {
    stage("git checkout")
    {
        git credentialsId: '7af3f3d0-5f15-42ec-addf-1213081fd23a', url: 'https://github.com/DevOps-Traning/Maven-web-project.git'
    }
	stage("Maven")
	{
	 if (isUnix())
	 {
	 "sh mvn clean package"
	 }
	 else 
	 {
	 "bat mvn clean package"
	 }
	}
	stage("Artifactory-repo")
	{
	"bat mvn deploy"
	}
}
