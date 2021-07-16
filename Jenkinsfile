pipeline{
  agent any
  stages{
    stage('build'){
      steps{
          sh 'cd /home/slave2/workspace/Testpipeline'
          sh 'docker build -t "maven" .'
        }
    }
    
    stage('push'){
      steps{
      sh 'docker tag maven:latest 369191473161.dkr.ecr.ap-south-1.amazonaws.com/dockerrepo:latest'
      sh 'docker push 369191473161.dkr.ecr.ap-south-1.amazonaws.com/dockerrepo:latest'  
      }
    }
  }
}
