pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Clones the repository
                git branch: 'main', url: 'https://github.com/your-username/your-repository.git'
            }
        }
        
        stage('Build') {
            steps {
                // Compile or build the application
                sh 'mvn clean install'
            }
        }
        
        stage('Test') {
            steps {
                // Run unit tests
                sh 'mvn test'
            }
        }
        
        stage('Package') {
            steps {
                // Package the application
                sh 'mvn package'
            }
        }

        stage('Deploy') {
            steps {
                // Deploy (in this example, just a placeholder message)
                echo 'Deploying to staging server...'
                // You can add SCP/SSH commands to copy files to a server or deploy to a container
            }
        }
    }

    post {
        success {
            echo 'Build and Deploy successful!'
        }
        failure {
            echo 'Build failed. Check the console for errors.'
        }
    }
}
