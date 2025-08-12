pipeline {
    agent { linux-node }

    options {
        timestamps()
        ansiColor('xterm')
    }

    stages {
        stage('Checkout') {
            steps {
                echo "🔄 Checking out source code..."
                git branch: 'main', credentialsId: 'SHA256:+3Ny4k7cdyBYQBQHx3ct5AyB6x2lvGrdtY8zqM1OASU', url: 'https://github.com/hyph-enated/node-webapp-bredel.git'
            }
        }

        stage('Build') {
            steps {
                echo "🚀 Running Build stage..."
                sh 'docker build -t image-2 .'
            }
        }

        stage('Test') {
            steps {
                echo "🚀 Running Test stage..."
                echo "No commands specified for Test stage"
            }
        }
    }

    post {
        always {
            echo "🧹 Cleaning up workspace..."
            cleanWs()
        }
        success {
            echo "✅ Pipeline completed successfully!"
        }
        failure {
            echo "❌ Pipeline failed. Please check the logs."
        }
    }
}
