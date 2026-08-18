pipeline {
    agent any

    stages {

        stage('Start') {
            steps {
                echo "Build started..."
                echo "Job ID: ${env.BUILD_NUMBER}"
            }
        }

        stage('Execute Code') {
            steps {
                echo "Executing application code..."

                bat '''
                    echo Hello from Jenkins Pipeline
                    echo Current date and time:
                    date /T
                    time /T
                '''
            }
        }

        stage('Processing') {
            steps {
                echo "Processing for 30 seconds..."
                sleep 30
            }
        }

        stage('Finish') {
            steps {
                echo "Build ${env.BUILD_NUMBER} completed successfully!"
            }
        }
    }
}
