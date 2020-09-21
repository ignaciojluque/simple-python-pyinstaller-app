pipeline {
    agent {
        docker {
            image "python:3.7.2"
            args '--user 0:0'
        }
    }
    stages {
        stage('build') {
            steps {
                sh 'echo "user name: $_user"'
                sh 'echo "user name ID (UID): $_uid"'
                sh 'pip install flask'
                
            }
        }
        stage('test') {
            steps {
                sh 'python test.py'
            }
        }
    }
}
