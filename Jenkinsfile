node {
    stage("code checkout")
    {
        git credentialsId: '7af3f3d0-5f15-42ec-addf-1213081fd23a', url: 'https://github.com/DevOps-Traning/Maven-web-project.git'
    }
    stage("maven")
    {
        def mvnHOME = tool name: 'Windows-Maven', type: 'maven'
        bat "${mvnHOME}/bin/mvn clean deploy"
    }
    stage("tomcat")
    {
        bat label: '', script: 'copy C:\\Users\\Nandihal\'s\\.jenkins\\workspace\\Oct-Pipeline-Project\\target\\*.war C:\\devops\\apache-tomcat-9.0.12\\webapps\\'
    }

}
