pipeline {
  agent { 
    docker { 
      image 'python:3.7.2' 
      args '--user 0:0'  
    }
  }
  stages {
    stage('build') {
      steps {
        sh 'pip3 install -r requirements.txt'
      }
    }
    stage('test') {
      steps {
        sh 'python3 test.py'
      }   
    }
  }
}
