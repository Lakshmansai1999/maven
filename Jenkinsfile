node('master') 
{
    stage('Continuous Download') 
	{
    git 'https://github.com/Lakshmansai1999/maven.git'
	}
    stage('Continuous Build') 
	{
    sh label: '', script: 'mvn package'
	}
    stage('Continuous Deployment') 
	{
sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war ssh -o StrictHostKeyChecking=no ubuntu@172.31.94.68:/home/ubuntu/tomcat/webappsqaenv.war'
	}   
}
