pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git credentialsId: 'github-creds', url: 'https://github.com/Prathmesh-502/my-web-app.git'
            }
        }

        stage('Build') {
            steps {
                echo 'No build steps needed for static HTML'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying to local HTTP server...'
                sh 'cp index.html /var/www/html/index.html'
            }
        }
    }
}
