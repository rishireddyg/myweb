node{
  stage( 'scm checkout'){
   
  git 'https://github.com/rishireddyg/myweb.git'
  }
  stage('compile-package'){
    sh 'mvn package'
  }
}
   
