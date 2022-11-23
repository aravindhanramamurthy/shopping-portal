pipeline {
  agent any
  stages {
    stage('build-the-app-stage') {
      steps {
        echo 'this is the first job to build'
        sh 'npm install'
      }
    }

    stage('test-the-app-stage') {
      steps {
        echo 'this is the second job to test'
        sh 'npm test'
      }
    }

    stage('package-the-app-stage') {
      steps {
        echo 'this is the third job to package'
        sh 'npm run package'
      }
    }

    stage('archive-artefacts') {
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
      echo 'this 3 stage pipeline has completed...'
    }

  }
}