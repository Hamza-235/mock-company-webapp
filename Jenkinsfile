pipeline {
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    // Run the Gradle build step
                    sh './gradlew assemble'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    // Run the Gradle test step
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

}
