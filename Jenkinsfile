node{
  stage( 'scm checkout'){
  git 'https://github.com/rishireddyg/myweb'
  }
  stage('compile-package){
  sh 'mvn package'
  }
}
