node {
stage("codecheckout")
{
git credentialsId: 'a22088e2-6170-4c11-bb28-fb920416a485', url: 'https://github.com/DevOps-Traning/Maven-web-project.git'
}
stage("maven")
{
def mvnHOME = tool name: 'linuxmaven', type: 'maven' 
sh "${mvnHOME}/bin/mvn clean deploy"
}
stage("tomcat")
{
sh 'cp /home/ec2-user/.jenkins/workspace/MyFirstPipelineJob/target/*.war /home/ec2-user/apache-tomcat-10.0.4/webapps/'
}
}
