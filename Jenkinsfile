pipeline {
    agent any

    tools {
        maven 'Maven 3.8.6' // Set this in Jenkins Global Tools Configuration
        jdk 'JDK 11'        // Set this in Jenkins Global Tools Configuration
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }

        stage('Run') {
            steps {
                sh 'java -cp target/simple-java-app-1.0-SNAPSHOT.jar com.example.App'
            }
        }
    }
}
