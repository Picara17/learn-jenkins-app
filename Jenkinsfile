pipeline {
    agent any

    stages {
        stage('Hello') {
        agent {
            docker {
                image 'node:18-alpine'
                reuseNote true
                }
        }
            steps {
                sh """
                ls -la
                node --version
                npm --version
                npm ci
                npm run build
                ls -la
                """
            }
        }
        stage("test by yanan") {
            steps {
                echo "Hello yanan"
                }
        }
    }
}