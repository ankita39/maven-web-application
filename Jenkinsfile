node
{

def mavenHome = tool name: "maven3.8.4"
stage ('CheckoutCode')
{
git branch: 'development', credentialsId: 'ae26eada-bd16-4a72-a760-aa9831bd3632', url: 'https://github.com/ankita39/maven-web-application.git'
}

stage ('build')
{
sh "${mavenHome}/bin/mvn clean package"
}
/*
stage ('SonarQubeReport')
{
sh "${mavenHome}/bin/mvn clean sonar:sonar"
}

stage ('UploadArtifacetoNexus')
{
sh "${mavenHome}/bin/mvn clean deploy"
}

stage ('DeployApplicationToTomcat')
{
sshagent(['f550c2ff-021a-428d-ba0a-0e3ba98cc975']) {
    sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@13.126.91.14:/opt/apache-tomcat-9.0.56/webapps/"
}
}
stage ('SendNotifications')
{
emailext body: '''Build Over

Regards
Ankita''', subject: 'Build Over', to: 'ankitapanda39@gmail.com'
}
*/
}
