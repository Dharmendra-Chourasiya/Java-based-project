pipeline {
    agent any

    environment {
        GIT_REPO_URL = 'https://github.com/Dharmendra-Chourasiya/Java-based-project.git'
        GIT_CREDENTIALS_ID = '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'
        GIT_EXECUTABLE = '/usr/bin/git' // The path determined earlier
    }

    tools {
        git "${GIT_EXECUTABLE}"
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: "${GIT_REPO_URL}", credentialsId: "${GIT_CREDENTIALS_ID}"
            }
        }

        stage('Build') {
            steps {
                echo 'Building...'
                // Your build steps
            }
        }

        stage('Test') {
            steps {
                echo 'Testing...'
                // Your test steps
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Your deploy steps
            }
        }
    }

    post {
        always {
            echo 'This will always run'
        }
    }
}
