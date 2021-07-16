pipeline{
  agent any
  stages{
    stage('push'){
      sh 'docker tag maven:latest 369191473161.dkr.ecr.ap-south-1.amazonaws.com/masterrepo:latest'
    }
  }
}
