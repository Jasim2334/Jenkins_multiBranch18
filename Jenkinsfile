node('built-in') 
{
    stage('Continuous Download_master') 
	{
    git 'https://github.com/sunildevops77/maven.git'
	}
    stage('Continuous Build_master') 
	{
    sh label: '', script: 'mvn package'
	}
	stage('Continuous Download_master')
	{
    scp /home/ubuntu/.jenkins/workspace/MultiBranchPipeline_master/webapp/target/webapp.war ubuntu@172.31.33.226:/var/lib/tomcat8/webapps/qaenv.war
        }
}
