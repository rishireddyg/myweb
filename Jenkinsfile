node{
  stage( 'scm checkout'){
   
  git 'https://github.com/rishireddyg/myweb'
  }
  stage('compile-package'){
    //get maven home path
    def mvnHome = tool name: 'maven3', type: 'maven'
    sh "${mvnHome}/bin/mvn package"
  }
}
