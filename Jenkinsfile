node{
def mavenHome = tool name: "maven3.8.4"

stage('CheckoutCode'){
git branch: 'development', credentialsId: 'aa98d351-6fa5-414a-9d38-3f0f58e51b34', url: 'https://github.com/sureshgundluru62/maven-web-application.git'
}
stage('Build'){
sh "${mavenHome}/bin/mvn clean package"
}
/*
stage('ExcuteSonarQubeReport'){
sh "${mavenHome}/bin/mvn sonar:sonar"
}
stage('UploadArtifactsIntoNexus'){
sh "${mavenHome}/bin/mvn deploy"
}
stage('DeployAppintoTomcatServer'){

sshagent(['08231cb3-e51f-4328-9168-c922f877aedc']) {
  sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@13.233.159.191:/opt/apache-tomcat-9.0.54/webapps/"
}

}
stage('SendEmailNotification'){
emailext body: '''Build Over

Thanks,
Suresh''', subject: 'Build Over', to: 'sureshgundluru62@gmail.com'
}
*/
}
