pipeline {
	agent any
	stages{
		stage ("scm checkout"){
git 'https://github.com/ANKITSHARAF1808/maven-project.git'
							  }
		  }
   {
stage ('Test stage')
withMaven(maven: 'Ankit_jenkins_Maven') {
   sh 'mvn test'
}
