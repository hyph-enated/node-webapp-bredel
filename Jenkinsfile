    pipeline {
        agent any

        stages {
            stage('Checkout Code') {
                steps {
                    git https://github.com/hyph-enated/node-webapp-bredel.git
                }
            }
            stage('Build Docker Image') {
                steps {
                    script {
                        docker.build("image-1")
                    }
                }
            }
        }
    }
