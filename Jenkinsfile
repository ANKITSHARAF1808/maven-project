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
Stage ('deploy to tomcat'){

step {
  sshagent (credentials: ['deploy to tomcat']) {
    sh 'scp -o StrictHostKeyChecking=no **/*.war ec2-user 172.31.44.96:/var/lib/tomcat/webapp'
  }
}
}
}
}
