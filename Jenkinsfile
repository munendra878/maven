pipeline {
    agent any

    tools {
        maven 'Maven3'   // Name as configured in Jenkins
        jdk 'jdk-17'     // Name as configured in Jenkins
    }

    stages {
        stage('Build') {
            steps {
                bat 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying application..."
                // Ensure the deploy folder exists
                bat 'if not exist C:\\deployments\\myapp mkdir C:\\deployments\\myapp'
                // Copy the JAR file
                bat 'copy target\\*.jar C:\\deployments\\myapp\\'
            }
        }
    }
}


