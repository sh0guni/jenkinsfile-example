pipeline {
  agent any

    stages {
      stage('Build') {
        steps {
          echo 'Building..'
        }
      }
      stage('Test') {
        steps {
          echo 'Testing..'
        }
      }
      stage('Deploy') {
        steps {
          echo 'Deploying....'
            @sshagent (credentials: ['deploy-dev']) {
              sh 'ssh 127.0.0.1 uname -a'
            }
        }
      }
    }
}
