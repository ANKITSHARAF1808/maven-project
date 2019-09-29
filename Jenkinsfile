pipeline {
	agent any
	
	
	stages
	{
		stage ("scm checkout")
		{
git 'https://github.com/ANKITSHARAF1808/maven-project.git'
		}
		}
   {
   
stage ('Test stage'){

steps {
withMaven(maven: 'Ankit_jenkins_Maven') 
{
   sh 'mvn test'
}
}
}
}

 {
   
stage ('create package'){

steps {
withMaven(maven: 'Ankit_jenkins_Maven') 
{
   sh 'mvn package'
}
}
}
}
 {
   
stage ('Install package'){

steps {
withMaven(maven: 'Ankit_jenkins_Maven') 
{
   sh 'mvn install'
}
}
}
}
{
stage ('deploy to tomcat')
	{

steps {
  sshagent (['172.31.47.249']) {
    sh 'scp -o StrictHostKeyChecking=no */target/*.war ec2-user@172.31.47.249:/var/lib/tomcat/webapps'
  }
}
}
}	
}
