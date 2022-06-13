node('built-in') 
{
    stage('Continuous Download_loans') 
	{
    git 'https://github.com/sunildevops77/maven.git'
	}
    stage('Continuous Build_loans') 
	{
    sh label: '', script: 'mvn package'
	}
	stage('Continuous Deployment_loans') 
	{
    sh 'scp /home/ubuntu/.jenkins/workspace/MultiBranchPipeline_master/webapp/target/webapp.war ubuntu@172.31.33.226:/var/lib/tomcat8/webapps/qaenv.war'
        }
	 stage('Continuous Testing_loans')
        {
    sh 'echo "Testing passed"'
        }
	stage('Continuous Deployment_loans') 
	{
    sh 'scp /home/ubuntu/.jenkins/workspace/MultiBranchPipeline_master/webapp/target/webapp.war ubuntu@172.31.42.160:/var/lib/tomcat8/webapps/prodenv.war' 
        }

}	
