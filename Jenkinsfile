node {
    stage("Code checkout")
    {
     git credentialsId: '2dd0ef6a-ec89-415a-ba25-edb3a6bd5d4e', url: 'https://github.com/DevOps-Traning/Maven-web-project.git'   
    }
    stage('Maven')
    {
        bat "mvn clean deploy"
    }
}
