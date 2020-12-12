node{
  stage( 'scm checkout'){
   
  git 'https://github.com/rishireddyg/myweb'
  }
  stage('compile-package'){
    //get maven home path
    def mvnHome = tool name: 'maven3', type: 'maven'
    sh "${mvnHome}/bin/mvn package"
  }
  stage('SonarQube Analysis'){
    def mvnHOme= tool name: 'maven3', type: 'maven'
    withSonarQubeEnv('sonar-6'){
      sh ="${mvnHome}/bin/mvn sonar:sonar"
    }
  }
    
  stage('Email Notification'){
    mail bcc: '', body: '''hi there ,
rishi here, there was a results from jenkins.''', cc: 'rishireddy.12345@gmail.com', from: '', replyTo: '', subject: 'test mail from jenkins', to: 'rishi.g4777@gmail.com
  }
  stage('slack Notification'){
    slackSend baseUrl: 'https://hooks.slack.com/services/', channel: '#integration-git-maven', color: 'good', message: 'hi welcome to rishi projects', tokenCredentialId: 'slack-demo', username: 'rrconsultants'
  }
}
