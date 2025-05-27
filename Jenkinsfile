pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/Prathmesh-502/project.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building Web App...'
                // For static apps, no actual build needed
            }
        }

        stage('Test') {
            steps {
                echo 'Running basic tests...'
                sh 'test -f index.html'  // check if index.html exists
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying to local HTTP server...'
                sh 'sudo cp -r * /var/www/html/'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
