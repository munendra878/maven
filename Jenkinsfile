pipeline {
    agent any

   tools {
    maven 'Maven3'   // keep Maven name as configured
    jdk 'jdk-17'      // exact name from Global Tool Configuration
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

