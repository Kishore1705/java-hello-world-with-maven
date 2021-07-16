pipeline{
  agent any
  stages{
    stage('build'){
      steps{
          sh 'cd /home/slave2/workspace/Testpipeline/java-hello-world-with-maven'
          sh 'docker build -t "maven" .'
        }
    }
}
}
