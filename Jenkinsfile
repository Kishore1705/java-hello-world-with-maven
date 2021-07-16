pipeline{
  agent any
  stages{
    stage('push'){
      steps{
      sh 'docker tag maven:latest 369191473161.dkr.ecr.ap-south-1.amazonaws.com/masterrepo:latest'
      sh 'docker push 369191473161.dkr.ecr.ap-south-1.amazonaws.com/masterrepo:latest'  
      }
    }
  }
}
