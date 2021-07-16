pipeline{
  agent any
  stages{
    stage('build'){
      steps{
          sh 'cd /home/slave2/workspace/Testpipeline'
          sh 'docker build -t "maven" .'
        }
    }
}
}
