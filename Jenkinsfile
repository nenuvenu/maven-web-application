node{

def mavenHome = tool name: "maven-3.8.5"

//checkoutcode
stage('CheckoutCode'){
git branch: 'development', credentialsId: 'c8efd36d-354b-4076-b3b7-2232ce6d5b2d', url: 'https://github.com/nenuvenu/maven-web-application.git'
}

//build stage
stage ('Build'){
sh "$mavenHome/bin/mvn clean package"
}

/*
//generate SonarReports
stage ('SonarqubeReport'){
sh "$mavenHome/bin/mvn sonar:sonar"
}

//Deploy app into tomcat server
stage ('Deploy'){
sshagent(['a02c5db2-9868-47e6-9d81-548f16d804cf']) {
sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@34.238.38.17:/opt/apache-tomcat-9.0.59/webapps"
}
}

*/  
}
