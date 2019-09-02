node{
  stage('SCM Checkout'){
    git 'https://github.com/jarkkop/CI_Demo'
  }
  stage('Compile-Package'){
    //Get maven home path
    def mvnHome = tool name: 'Maven_3.6.0', type: 'maven'
    bat "${mvnHome}/bin/mvn package"     //Windows
//    sh "${mvnHome}/bin/mvn package"    //Linux
//    bat 'mvn package'                 //Windows
  }
  stage('eMail notification'){
    mail bcc: '', body: '''Hi
This is jenkins mail notification
Regards 
Jarkko''', cc: '', from: '', replyTo: '', subject: 'Jenkins mail', to: 'jarkko.sw.pesonen@gmail.com'
  }

//  stage('Slack') {
//    slackSend channel: '#jenkins-pipeline-demo', 
//      color: 'good', 
//      message: 'Welcome to jenkins. Here is mesage to you Slack', 
//      tokenCredentialId: 'slack-pipedemo'
//  }
  
}
