node{
  stage( 'scm checkout'){
    tool name: 'maven3', type: 'maven'
  git 'https://github.com/rishireddyg/myweb'
  }
  stage('compile-package'){
  sh 'mvn package'
  }
}
