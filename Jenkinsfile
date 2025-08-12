pipeline {
  agent { label 'linux-node' }
  stages{
    stage('Dockerize') {
      steps {
        script {
          docker.build('image').run('-p 3000:3000')
        }
      }
    }
  }
}
