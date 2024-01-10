pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building..'
        sh 'chmod +x ./jenkins/build.sh'
        archiveArtifacts(artifacts: 'target/*.jar', fingerprint: true)
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