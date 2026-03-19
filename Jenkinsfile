pipeline {
    agent { label 'docker' }
    
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        
        stage('Build') {
            steps {
                echo "Building... ${env.GIT_BRANCH}"
                sh 'echo "Hola desde GitHub!"'
            }
        }
        
        stage('Test') {
            steps {
                echo "Running tests..."
                sh 'echo "Tests pasados ✅"'
            }
        }
    }
    
    post {
        success {
            echo "✅ Build exitoso!"
        }
        failure {
            echo "❌ Build falló"
        }
    }
}
