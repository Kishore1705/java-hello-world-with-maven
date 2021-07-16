pipeline{
  agent none
  stages{
    stage('build'){
      agent {
        label 'slave2'
      }
      steps{
          sh 'cd /home/slave2/workspace/Testpipeline'
          sh 'docker build -t "maven" .'
        }
    }
    
    stage('push'){
      agent {
        label 'slave2'
      }
      steps{
      sh 'docker tag maven:latest 369191473161.dkr.ecr.ap-south-1.amazonaws.com/dockerrepo:latest'
      sh 'docker push 369191473161.dkr.ecr.ap-south-1.amazonaws.com/dockerrepo:latest'  
      }
    }
    stage ('pull and run image'){
      agent {
        label 'slave3'
      }
      steps{
        sh 'docker pull 369191473161.dkr.ecr.ap-south-1.amazonaws.com/dockerrepo:latest'
        sh 'docker run -dt -p 8087:8080 369191473161.dkr.ecr.ap-south-1.amazonaws.com/dockerrepo:latest'
      }
    }
    
  }
}
