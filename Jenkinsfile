pipeline {
  agent {
    docker {
      image 'node:18-alpine'
    }
  }

  stages {
    stage('Checkout') {
      steps {
        echo '📥 Code checked out'
      }
    }

    stage('Run App') {
      steps {
        sh 'node app.js'
      }
    }
  }

  post {
    success {
      echo '🎉 Jenkins pipeline ran successfully!'
    }
    failure {
      echo '❌ Pipeline failed'
    }
  }
}
