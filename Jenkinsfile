node{
  stage( 'scm checkout'){
   
  git 'https://github.com/rishireddyg/myweb'
  }
  stage('compile-package'){
    //get maven home path
    def mvnHome = tool name: 'maven3', type: 'maven'
    sh "${mvnHome}/bin/mvn package"
  }
  stage('Email Notification'){
    mail bcc: '', body: '''hi there ,
rishi here, there was a results from jenkins.''', cc: 'rishireddy.12345@gmail.com', from: '', replyTo: '', subject: 'test mail from jenkins', to: 'rishi.g4777@gmail.com
}
