pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code from Git...'
                git 'https://github.com/pavanmedapureddy/project.git'
            }
        }

        stage('Build') {
            steps {
                echo 'No build required for HTML. Just verifying files...'
                sh 'ls -R'
            }
        }

        stage('Archive') {
            steps {
                echo 'Archiving HTML project...'
                archiveArtifacts artifacts: '**/*', fingerprint: true
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying to server...'
                // Example: Copy to remote server
                // sh 'scp -r * user@server:/var/www/html/'
            }
        }
    }
}
