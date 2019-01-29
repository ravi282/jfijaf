node('master') 
{
    stage('Cont_down-1.1')
    {
       git 'https://github.com/ravi282/rac.git'
    }
    stage('Cont_bui-2.1') 
    {
       sh label: '', script: 'mvn package'
    }
    stage('Cont_Deploy-3.1')
    {
       sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/multipipe/webapp/target/webapp.war ubuntu@172.31.84.116:/var/lib/tomcat7/webapps/qaenv.war' 
    }
}
