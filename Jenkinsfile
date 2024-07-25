pipeline {
    agent any
    environment {
        MAVEN_HOME = tool 'Maven-3.9.0' 
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building the Java application...'
                sh 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                // Add your test commands here if you have tests
                sh 'mvn test'
            }
        }
    }
    post {
        success {
            echo 'Build and test succeeded!'
        }
        failure {
            echo 'Build or test failed!'
        }
    }
}
