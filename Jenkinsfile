
pipeline {
  agent any
  
  stages {
    stage('Build'){
      steps{
        build 'PES1UG22CS700-1'
        sh 'g++ -o output sample.cpp'
        echo "Build Successful"
      }
    }
    
    stage('Test'){
      steps{
        sh './output'
        ec "Test Successful"
      }
    }
    
    stage('Deploy'){
      steps{
        echo "Deployment Successful"
      }
    }
  }
  
  post{
    failure{
      echo "Pipeline Failed"
    }
  }
}
   

