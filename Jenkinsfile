pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'this is the build job'
        sh 'npm install'
      }
    }

    stage('Test') {
      steps {
        echo 'this is the npm test'
        sh 'uptime'
      }
    }

    stage('Package') {
      steps {
        echo 'this is the Package job'
        sh 'npm test'
      }
    }

    stage('archive') {
      steps {
        archiveArtifacts '**/distribution/*.zip'
      }
    }

  }
  tools {
    nodejs 'nodejs'
  }
  post {
    always {
      echo 'this pipeline has completed...'
    }

  }
}