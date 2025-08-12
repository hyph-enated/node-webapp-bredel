
pipeline {
  agent { label 'linux-node' }

    stage('Dockerize') {
      steps {
        script {
          docker.build('image').run('-p 3000:3000')
        }
      }
    }
  }
