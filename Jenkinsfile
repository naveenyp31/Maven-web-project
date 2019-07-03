node {
    stage("Code checkout")
    {
     git credentialsId: 'f60575b0-73ab-45f4-b8f7-7010e4fbcd40', url: 'https://github.com/DevOps-Traning/Maven-web-project.git'   
    }
    stage('Maven')
    {
        bat "mvn clean deploy"
    }
}
