
pipeline {
  agent { label 'linux-node' }

    stage('Dockerize') {
      steps {
        docker.build('image').run('-p 3000:3000')
      }
    }
  }
}
