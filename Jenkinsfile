pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Building..'
            sh 'chmod +x ./jenkins/build.sh'
          }
        }

        stage('Testing B') {
          steps {
            sh '''sleep 10
echo done'''
          }
        }

      }
    }

    stage('Test') {
      steps {
        echo 'Testing..'
        sh 'chmod +x ./jenkins/test-all.sh'
      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying....'
      }
    }

  }
}