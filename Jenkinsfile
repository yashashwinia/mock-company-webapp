pipeline {
    agent any
    
    stages {
        // Build Stage
        stage('Build') {
            steps {
                script {
                    // Run Gradle assemble to build the application
                    sh './gradlew assemble'
                }
            }
        }
        
        // Test Stage
        stage('Test') {
            steps {
                script {
                    // Run Gradle test to run all the unit tests
                    sh './gradlew test'
                }
            }
        }
    }

    post {
        success {
            echo 'Build and tests passed successfully!'
        }
        failure {
            echo 'Build or tests failed.'
        }
    }
}
