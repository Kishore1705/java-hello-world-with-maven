pipeline{
  stages{
    stage('build'){
      steps{
          sh 'cd java-hello-world-with-maven'
          sh 'docker build -t "maven" .'
        }
    }
}
}
