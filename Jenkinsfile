    pipeline {
    agent any

    tools {
        git 'Default Git' // Use the name given in the Git configuration
    }

    environment {
        GIT_REPO_URL = 'https://github.com/Dharmendra-Chourasiya/Java-based-project.git'
        GIT_CREDENTIALS_ID = 'github-cicd'
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: "${https://github.com/Dharmendra-Chourasiya/Java-based-project.git}", credentialsId: "${gitgub-cicd}"
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
    

   
  
