pipeline {
    agent any

    tools {
        maven 'Maven3'   // Name of Maven configured in Jenkins
        jdk 'JDK17'      // Name of JDK configured in Jenkins
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
                echo "Deploying application on Windows server..."
                // Example deploy: copy JAR to folder
                bat 'copy target\\*.jar C:\\deployments\\myapp\\'
            }
        }
    }
}

